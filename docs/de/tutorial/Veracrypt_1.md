<a class="nav-button pull-left" href="../KeePass_4">zurück</a>
<br>

# Veracrypt - Verschlüsselte Container

!!! warning "Fortgeschrittene Verwendung"

Wenn ein Passwort Manager wie [KeePass](KeePass_1.md) geknackt wird, hat der Angreifer Zugriff auf alle Passworteinträge. Unter Verwendung von [ALX Password Matrix](PasswordMatrix_1.md) ist das Problem etwas entschärft, da die Passwörter nicht im Klartext im Passwort Manager stehen, die folgenden Seiten beschreiben, wie sich das Sicherheitsmaß weiter steigern lässt.

1. Separate Passwort Container pro Password (mit unterschiedlichen Master Passwörtern).
2. Speichern der Passwort Container in einem zusätzlich verschlüsselten Veracrypt (früher Truecrypt) Container.