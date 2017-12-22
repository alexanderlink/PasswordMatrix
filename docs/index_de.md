# ALX Passwort Matrix

Das Problem bei üblichen Passwort Managern ist, dass wenn der Passwort Container gehackt wird, alle Passwörter im Freitext &ndash; direkt verwendbar &ndash; dem Angreifer zur Verfügung stehen.

`ALX Passwort Matrix` ermöglicht, die Passwörter nicht im Freitext im Passwort Manager abzulegen, sondern pro Passwort eine Matrix aus Zeichen. Das konkrete Passwort lässt sich über ein Schema/einen Pfad, den nur der Eigentümer kennt im Kopf reproduzieren. Selbst wenn die Matrix gestohlen wird, kann der Angreifer nichts damit anfangen kann, weil er den "Pfad" nicht kennt. Die möglichen Kombinationen sind zu groß, um das Passwort (in absehbarer Zeit) rekonstruieren und ausnutzen zu können.

!!! warning
    Password Matrix sollte **immer** in Verbindung mit einem Passwort Manager oder verschlüsseltem Container verwendet werden! Nur wird die erhöhte Sicherheit erreicht.

## Vorteile
- Keine Freitext-Passwörter gespeichert
    - Angreifer kann mit Matrix nichts anfangen
- Zufällig generierte Passwörter
    - Schwerer zu knacken, als von Menschen erdachte Passwörter
    - Es wird einfach, regelmäßig Passwörter zu ändern

## Beispiel
Der gelbe Pfad existiert nur im Kopf des Eigentümers. Sollte die Matrix in falsche Hände fallen, kann der Angreifer das Passwort ohne den Pfad nicht rekonstruieren.
<img src="/tutorial/images/passwordMatrix_anim.gif" width="50%">