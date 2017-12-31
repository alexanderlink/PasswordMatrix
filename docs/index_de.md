<div style="text-align:right">
    <a href="/"><img class="emojione" src="https://cdn.jsdelivr.net/emojione/assets/svg/1f1ec-1f1e7.svg" title="Switch to English"> switch to English &nbsp; </a>
</div>

# ALX Passwort Matrix

ALX Passwort Matrix ist ein Werkzeug um Passwort Matrizen zu generieren und anzuzeigen. Diese können dann in Passwort Managern verwendet werden, um Passwörter nicht im Klartext abzulegen.

!!! hint "Los geht's..."

    <a class="button" href="../PasswordMatrix.htm"><b>Password Matrix verwenden</b></a>
    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Hier finden Sie eine <a href="/tutorial/PasswordMatrix_1_de/"><b>Anleitung zur Verwendung</b></a>.

## Problemstellung

Das Problem bei üblichen **Passwort Managern** ist, dass der Passwort Container geknackt werden kann (z.B. Phising, Key Logger, unsicherer Passwort Manager) und damit alle Passwörter im Klartext &ndash; direkt verwendbar &ndash; dem Angreifer zur Verfügung stehen.

Eine **Passwort Matrix** ermöglicht, die Passwörter nicht im Freitext im Passwort Manager abzulegen, sondern pro Passwort eine Matrix aus Zeichen. Das konkrete Passwort lässt sich über ein Schema/einen Pfad, den nur der Eigentümer kennt im Kopf reproduzieren. Selbst wenn die Matrix gestohlen wird, kann der Angreifer nichts damit anfangen kann, weil er den "Pfad" nicht kennt. Die möglichen Kombinationen sind zu groß, um das Passwort (in absehbarer Zeit) rekonstruieren und ausnutzen zu können.

**Vorteile einer Password Matrix:**

- Es werden keine Freitext-Passwörter gespeichert.
    - :white_check_mark: Ein Angreifer kann mit der Matrix nichts anfangen
- Zufällig generierte Passwörter...
    - :white_check_mark: sind schwerer zu knacken, als von Menschen erdachte Passwörter
    - :white_check_mark: Es wird einfach, regelmäßig Passwörter zu ändern

!!! warning
    Password Matrix sollte **immer** in Verbindung mit einem Passwort Manager oder verschlüsseltem Container verwendet werden! Nur so wird die erhöhte Sicherheit erreicht.

<br>

### Generelles zu Passwörtern

Passwörter müssen **sicher** sein und **regelmäßig geändert** werden, um ein Ausnutzen im Fall eines Angriffs zu vermeiden.

!!! hint "Hinweis"
    Hier finden Sie Empfehlungen des BSI zum [Umgang mit Passwörtern](https://www.bsi-fuer-buerger.de/BSIFB/DE/Empfehlungen/Passwoerter/Umgang/umgang_node.html) und zu [sicheren Passwörtern](https://www.bsi-fuer-buerger.de/BSIFB/DE/Empfehlungen/Passwoerter/passwoerter_node.html).

Es gibt viele Möglichkeiten Passwörter zu verwalten, mit allen Vor- und Nachteilen.

- **Im Kopf** &ndash; Passwörter im Kopf merken führt meistens dazu, dass die Passwörter zu einfach sind und auch noch für viele Seiten identisch. Das regelmäßige Ändern von Passwörtern stellt eine weitere Herausforderung dar, da neue Passwörter möglichst nichts mit alten Passwörtern zu tun haben dürfen.
- **Notizzettel** &ndash; Im einfachsten Fall schreibt man ein Klartext-Passwort auf einen Zettel. Jeder der den Zettel findet kann das Passwort ausnutzen.
- **Text-Datei** &ndash; Eine Text-Datei mit dem Klartext-Passwort ist ähnlich unsicher wie ein Zettel. Ist der Computer ans Internet angeschlossen kann die Datei online erbeutet und das Passwort vom Angreifer direkt verwendet werden.
- **Passwort Manager** &ndash; Ein Passwort Manager legt Passwörter verschlüsselt ab. Öffnen lässt er sich mit einem (möglichst sicheren) Master Passwort. Wird der Passwort Container erbeutet muss der Angreifer zusätzlich den Container knacken, um an das (Klartext) Passwort zu kommen.


### Vergleich der Methoden

<img title="" alt="✅" class="emojione" src="https://cdn.jsdelivr.net/emojione/assets/svg/2705.svg"> sicher | <img title="" alt="❎" class="emojione" src="https://cdn.jsdelivr.net/emojione/assets/svg/274e.svg"> unsicher | 
<img title="" alt="⚠️" class="emojione" src="https://cdn.jsdelivr.net/emojione/assets/svg/26a0.svg"> eingeschränkt sicher

<table>
    <tr>
        <th></th>
        <th>Zettel</th>
        <th>Text-Datei </th>
        <th>Passwort Manager</th>
        <th>Passwort Matrix<br>+ Text-Datei </th>
        <th>Passwort Matrix<br>+ Passwort Manager</th>
    </tr>
    <tr>
        <td title="Ist die Art der Ablage sicher?">Sichere Ablage</td>
        <td><img title="Ein Zettel ist nicht unbedingt unsicher, z.B. wenn er in einem Safe gelagert wird" alt="⚠️" class="emojione" src="https://cdn.jsdelivr.net/emojione/assets/svg/26a0.svg"></td>
        <td><img title="Eine Text-Datei kann direkt gelesen werden" alt="❎" class="emojione" src="https://cdn.jsdelivr.net/emojione/assets/svg/274e.svg"></td>
        <td><img title="Ein Passwort Manager legt die Passwörter verschlüsselt ab" alt="✅" class="emojione" src="https://cdn.jsdelivr.net/emojione/assets/svg/2705.svg"></td>
        <td><img title="Eine Text-Datei kann direkt gelesen werden. Mit der Passwort Matrix kann das Passwort allerdings nicht direkt verwendet werden."alt="⚠️" class="emojione" src="https://cdn.jsdelivr.net/emojione/assets/svg/26a0.svg"></td>
        <td><img title="Ein Passwort Manager legt die Passwörter verschlüsselt ab" alt="✅" class="emojione" src="https://cdn.jsdelivr.net/emojione/assets/svg/2705.svg"></td>
    </tr>
    <tr>
        <td title="">Sichere gegen Online Angriffe</td>
        <td><img title="Da die Daten nicht auf dem Computer liegen ist ein Online Angriff unmöglich" alt="✅" class="emojione" src="https://cdn.jsdelivr.net/emojione/assets/svg/2705.svg"></td>
        <td><img title="Ist der Computer mit dem Internet verbunden können die Passwörter bei einem Angriff direkt aus der Datei gelesen werden." alt="❎" class="emojione" src="https://cdn.jsdelivr.net/emojione/assets/svg/274e.svg"></td>
        <td><img title="Der Passwort Container kann zwar zugegriffen werden, die Daten sind allerdings verschlüsselt. Die Verschlüsselung muss separat geknackt werden." alt="⚠️" class="emojione" src="https://cdn.jsdelivr.net/emojione/assets/svg/26a0.svg"></td>
        <td><img title="Ist der Computer mit dem Internet verbunden können die Passwörter bei einem Angriff direkt aus der Datei gelesen werden. Mit der Passwort Matrix kann das Passwort allerdings nicht direkt verwendet werden." alt="⚠️" class="emojione" src="https://cdn.jsdelivr.net/emojione/assets/svg/26a0.svg"></td>
        <td><img title="Der Passwort Container kann zwar zugegriffen werden, die Daten sind allerdings verschlüsselt. Die Verschlüsselung muss separat geknackt werden. Mit der Passwort Matrix kann das Passwort allerdings nicht direkt verwendet werden." alt="⚠️" class="emojione" src="https://cdn.jsdelivr.net/emojione/assets/svg/26a0.svg"></td>
    </tr>
    <tr>
        <td title="">Passwörter nicht verwendbar nach Knacken der Ablage</td>
        <td><img title="Klartext Passwörter können direkt verwendet werden" alt="❎" class="emojione" src="https://cdn.jsdelivr.net/emojione/assets/svg/274e.svg"></td>
        <td><img title="Klartext Passwörter können direkt verwendet werden" alt="❎" class="emojione" src="https://cdn.jsdelivr.net/emojione/assets/svg/274e.svg"></td>
        <td><img title="Klartext Passwörter können direkt verwendet werden" alt="❎" class="emojione" src="https://cdn.jsdelivr.net/emojione/assets/svg/274e.svg"></td>
        <td><img title="Mit der Passwort Matrix kann das Passwort nicht direkt verwendet werden" alt="✅" class="emojione" src="https://cdn.jsdelivr.net/emojione/assets/svg/2705.svg"></td>
        <td><img title="Mit der Passwort Matrix kann das Passwort nicht direkt verwendet werden" alt="✅" class="emojione" src="https://cdn.jsdelivr.net/emojione/assets/svg/2705.svg"></td>
    </tr>
</table>

## Passwort Matrix Beispiel
Der gelbe Pfad existiert nur im Kopf des Eigentümers. Sollte die Matrix in falsche Hände fallen, kann der Angreifer das Passwort ohne den Pfad nicht rekonstruieren.
<img src="/tutorial/images/passwordMatrix_anim.gif" width="50%">