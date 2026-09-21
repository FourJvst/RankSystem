# Ranks

Paper-Plugin fuer die Verwaltung von Team-Raengen auf einem Minecraft-Server.
Spieler koennen als Admin, Moderator oder Helfer eingestuft werden und ihre
Team-Rechte mit `/aduty` aktivieren.

## Voraussetzungen

- Java 21 oder neuer
- Maven 3.9 oder neuer
- Paper 1.21.8 oder eine kompatible Version

## Bauen

Im Projektverzeichnis ausfuehren:

```bash
mvn package
```

Die fertige Plugin-Datei wird als `target/Ranks.jar` erzeugt. Kopiere sie in den
`plugins`-Ordner deines Paper-Servers und starte den Server anschliessend neu.

## Befehle

- `/rank <Spieler> admin|moderator|helfer|none` setzt den Rang (nur Operatoren)
- `/aduty` aktiviert oder deaktiviert den Rangmodus
- `/fly` aktiviert oder deaktiviert das Fliegen fuer Teammitglieder
- `/teamchat <Nachricht>` oder `/tc <Nachricht>` sendet eine Nachricht im Teamchat

## Rangverhalten

- Admins erhalten Operator-Rechte.
- Moderatoren erhalten Zugriff auf `/kick` und `/ban`.
- Im aktiven Rangmodus erscheinen `[A]`, `[M]` oder `[H]` im Tab.
- Moderator- und Helfer-Rechte sind nur im aktiven Rangmodus verfuegbar.
- Teammitglieder sind im aktiven Rangmodus unverwundbar.
- Beim Aktivieren von `/aduty` wird eine Servermeldung ausgegeben.
