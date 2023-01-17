# Ubi Erat Lupa: Technische Dokumentation

Willkommen zur technischen Dokumentation der archäologischen Datenbank *Ubi Erat Lupa*.

## Wichtige Links

- Offizielle Webseite der Datenbank: [lupa.at](http://lupa.at/)
- Datenbank-Export: [github.com/ubieratlupa/database](https://github.com/ubieratlupa/database)
- Quellcode von lupa.at: [github.com/ubieratlupa/lupa.at](https://github.com/ubieratlupa/lupa.at)

## Mitarbeit an Ubi Erat Lupa

### Dateneingabe

Lupa verwendet eine PostgreSQL-Datenbank. Um Daten in Lupa einzugeben, benötigen Sie einen PostgreSQL-Client.
Wir empfehlen folgende Programme:

#### Postico (nur für macOS)

Wenn du einen Mac hast, empfehle ich Postico zur Dateneingabe. 

1. Gehe zur [Postico Webseite](https://eggerapps.at/postico/) und lade die neueste Version
2. Gib folgende Verbindungseinstellungen ein:
   - **Database:** lupa_production
   - **User:** *dein Benutzername*
   - **Passwort:** *dein Passwort*
   - **Connect via SSH Tunnel:** Ja
   - **Host:** lupa.at
   - **Fingerprint:** SHA256:TuLAFXYhglgQ5+caR2xX08iwJM+XEsdM+mUzEYlKyag
   - **User:** *nocheinmal dein Benutzername*
   - **Passwort:** *nocheinmal dein Passwort*
3. Klicke auf "Test Connection" um die Verbindung zu überprüfen.
4. Wenn keine Fehlermeldung kommt, kannst du danach auf "Connect" klicken.


#### DBeaver (alle Betriebssysteme)

1. Lade die Community Edition von der [DBeaver Download Seite](https://dbeaver.io/download/)
2. Beim ersten starten fragt DBeaver ob du eine Datenbank erstellen willst -> Nein
3. Füge eine Verbindung zum PostgreSQL Server hinzu. Klicke falls notwendig auf das Icon links oben (Stecker mit Plus)
4. Wähle PostgreSQL (blauer Elephant)
5. Fülle zuerst die Felder im Reiter **Allgemein** aus:
   - **Datenbank:** lupa_production
   - **Benutzername:** *dein Benutzername*
   - **Passwort:** *dein Passwort*
6. Wechsle dann auf den Reiter **SSH**:
   - **Verwende SSH-Tunnel**: Ja
   - **Host/IP:** lupa.at
   - Benutzer: *nocheinmal dein Benutzername*
   - Passwort: *nocheinmal dein Passwort*
7. Überprüfe ob alles funktioniert mit dem Button "Verbindung testen…" (links unten). Wahrscheinlich müssen beim ersten Mal noch Treiber geladen werden.
8. Wenn alles funktiniert, klicke "Fertigstellen"
9. Nun findest du die neue Verbindung in der Seitenleiste. Um zu den Steindenkmälern zu gelangen, folge diesem Pfad in der Seitenleiste:
   - lupa_production
   - Datenbanken
   - lupa_production
   - Schemata
   - public
   - Tabellen
   - monuments
10. Wechsle in den Reiter "Daten" um den Inhalt der Tabelle anzuzeigen
