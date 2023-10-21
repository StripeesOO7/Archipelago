# Anleitung für die Nutzung von Archipelago auf macOS 
Archipelago hat aktuell keine compilierte/ausführbare Version für macOS. Es ist jedoch möglich, wie auf jedem anderen Betriebssystem, den Quellkcode direkt auszuführen.
Diese Anleitung erwartet ein wenig Vorerfarhrung darin Programme über die Kommandozeile/das Terminal zu starten.

## Software Vorausetzungen
Hier ist eine Liste an zuinstallierender Software und Quellcode zum herunterladen.
1. Python 3.11 "universal2" oder neuer vom [Python.org's macOS Downloadverzeichnis](https://www.python.org/downloads/macos/).
   **Python 3.12 is not supported yet.**
2. Xcode aus dem [macOS App Store](https://apps.apple.com/us/app/xcode/id497799835).
3. Den Quellcode der aktuellen [Archipelago Version](https://github.com/ArchipelagoMW/Archipelago/releases). `Source code (zip)`
4. die Grafiken mit "darwin" im Namen aus dem [SNI Github Verzeichnis](https://github.com/alttpo/sni/releases).
5. Falls du local (nicht über die Webseite) Gegner zufällig vertilen möchtest (Enemizer), wird "EnemizerCLI" aus dem Enemizer [Github Verzeichnis](https://github.com/Ijwu/Enemizer/releases) benötigt.
6. Einen Emulator falls du dich dazu entscheidest ROM basierte Spiele zu spielen. Für GB/GBA und SNES Spiele empfieht es sich RetroArch zu benutzten, da dies am einfachsten einzureichten ist unter macOS. [RetroArch](https://www.retroarch.com/?page=platforms) kann hier heruntergeladen werden.
## Das Archipelago Verzeichnis extrahieren
1. Doppel Klicke das .zip Archive des Archipelago Quellcode um es in einen Ordner names "Archipelago" zu extrahieren.
2. Verschiebe den Archipelago Ordner an einen Ort außerhalb des Downloads Verzeichnisses.
3. Öffne das Terminal und navigiere zum Archipelago Ordner oder rechts-klicke den Archipelago Ordner und ganz unten im Kontextmenü sollte "Neues Terminal beim Ordner" erscheinen
## Eine Virtual Umgebung anlegen
Um verschiedene die Pakete von verschienen Python-Projekten nicht mit einander zu mischen und in Versionskonflikte zu laufen empfiehlt es sich für jedes Pytohn-Prjekt eine vitruelle Umgebung (Virtual environment) anzulegen. Wenn Archipelago die einzige dirtekt aus dem Quellcode ausgeführte Python Anwendung ist, ist dies nicht zwingen nötig aber dennoch empfohlen. 
1. Öffne das Terminal und navigiere zum Archipelago Ordner oder alternaitv rechts-klicke den Archipelago Ordner und ganz unten im Kontextmenü sollte "Neues Terminal beim Ordner" erscheinen.
2. Führe den Befehl `python3 -m venv venv` aus um eine vitruelle Umgebung zu namens "venv" zu erstellen. Dieser Befehl erzeugt einen neuen Ordner im aktuellen Verzeichnis. Stelle sicher das nicht bereits ein Ordner mit diesem namen im aktuellen/angegebene Verzeichnis existiert.
3. Führe den Befehl `source venv/bin/activate` aus um die virtuelle Umgebung zu aktivieren.
4. Um die virtual Umgebung zu verlassen, führe `deactivate` aus.
## Schritte um die Clients auszuführen
1.  Wenn dein ausgewähltes Spiel keine patch-Datei benötigt, führe den Befehl `python3 SNIClient.py` aus. Ändere den namen des Clients im Befehl abhängig vom Spiel oder nutze den allgemeinen `ArchipealgoTextClient` sollte es keinen speziellen Client geben.
2. Wenn dein Spiel eine patch-datei benötigt, kopiere die ROM des Spiels in das Archipelago Verzeichnis und führe den Befehl `python3 SNIClient.py 'patchfile'` mit dem entsprechenden Clientnamen und der korrekten Patchdatei mit den Dateiendungen apsm, aplttp, apsmz3, etc. aus.
Beispiel: `python3 SNIClient.py 'AP_..._{playername}.aplttp'`
3. Der entsprechende Client sollte nun geöffnet sein und wenn vorhanden eine gepatchte ROM des Spiels erstellt worden sein.
## Zusätzliche schritte für SNES Spiele
1. Wenn RetroArch verwendet wird, ist eine Setup Anleitung  [hier im 'the Link to the Past' setup guide](https://archipelago.gg/tutorial/A%20Link%20to%20the%20Past/multiworld/en) zu finden die ebenfalls auf macOS funktioniert.
2. Entpacke das SNI tar.gz-Archiv in einen Ordner der `SNI` heißt.
3. Verschiebe den entpackten SNI-Ordner in die oberste ebene des weiter oben erstellte Archipelago-Verzeichnisses.
4. Wenn alles korrekt benannt ist und im Archipelago Verzeichnis liegt solltes SNES Spiele automatisch SNI starten. Wenn nicht kann man die im SNI-Ordner befindliche SNI-Anwenudng auch manuell starten.
5. Wenn Enemizer benutzt werden soll entpacke den Download von weiter oben und bennen ihn in `EnemizerCLI` um.
6. Verschiebe das eben entpackte Verzeichnis neben SNI in di oberste ebene des Archipelago Verzeichnisses und es für lokales Generieren nutzen zu können.  
7. Jetzt da SNI, der Client und der Emulator gestartet sind sollte alles bereit sein.
