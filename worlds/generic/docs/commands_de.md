# Hilfereiche Befehle

Befehle (Commands) werden in Zwei Kategorien aufgeteilt: Client- und Serverbefehle. Clientbefehle werden vom
Client/Spiel lokal ausgeführt und haben keinen einfluss auf die Archipelago Sitzung. Serverbefehle hingegen werden
serverseitig von Archipelago ausgeführt und haben einen einfluss auf die aktuelle Sitzung oder stellen zusätzliche
Informationen bereit.

Clientbefehle werden lokal, auch ohne Verbindung zum Server, innerhalb des Clients ausgeführt. Clientspezifische/Lokale
Befehle werden mit einem forward slash `/` begonnen. 

Serverbefehle werden immer an den Server gesendet und immer mit einem Ausrufezeichen `!` begonnen. <br/>

# Serverbefehle

Serverbefehle können von jedem Client/Spiel gesendet werden, welcher es erlaubt Textnachrichten an den Server zu senden.
Wenn der Client/das Spiel keine möglichkeit bietet Textnachrichten and er Server zu senden empfiehlt es sich sich
zusätzlich über den in der Archipelago installation enthaltenen TextClient mit seinen Slotnamen Anzumelden. Um einen
Befehl anzuschicken reicht es aus diesen, beginnent mit einem Ausrufezeichen, als Textnachricht abzuschicken.

### Allgemeine Befehle
- `!help` Listet alle verfügbaren Befehle auf.
- `!license` Listet die Software Lizensinformation auf.
- `!options` Listet die aktuellen Serveroptionen, inclusive dem serverpasswort im Klartext, auf.
- `!players` Listet informationen über alle nicht-/verbundenen Spieler auf.
- `!status` Listet Informationen über den den Verbindungsstatus und die Anzahl der bisher erledigten Checks für jeden
  Spieler auf. <br /> (Optional kann ein Tag angegeben werden und für alle Speielr wird dann aufgelistet ob sie den
  jeweiligen Tag zuordnet werden konnten. Bsp: `!status DeathLink`)


### Nützliches
- `!countdown <number of seconds>` Startete einen Countdown startend beid er angegebenen Zahl in Sekunden. Nützlich wenn
  man koordiniert gleichzeitig starten möchte. Standardwert ist 10 Sekunden wenn kein Wert mitgegeben wird.
- `!alias <alias>` Setzt einen Alias, sodass es möglich ist Befehle mit dieses Alias anstatt dem angegebene Slotnamen
  auszuführen.
- `!admin <command>` Führt einen Befehl so aus als wäre er direkt in der Server-Befehlszeile eingegeben worden.
  Fernadministrierung muss vorher aktiviert worden sein.

### Informationen
- `!remaining` Listet die Items auf die noch in deiner Welt übrig sind, jedoch nicht wo diese zu finden sind und für
  welchen Speieler diese sind.
- `!missing` Listet die Locations, aus Sicht des Servers, auf die noch nicht in deiner Welt abgearbeitet/gechecked
  wurden.
- `!checked` Listet die Locations, aus Sicht des Servers, auf die bereits in deiner Welt abgearbeitet/gechecked wurden.

### Hinweise
- `!hint` Listet alle bereits aufgedeckten Hinweise für Items die in deiner Welt liegen auf, sowie die aktuelle Anzahl
  an Hinweispunkten und wie viel ein Hinweis kostet.
- `!hint <item name>` Zeigt die die Welt und den Ort innerhalb dieser Welt an in der das gesucht Item liegt. Verbraucht
  Punkte die durch das abarbeiten/checken von Locations "erarbeitet" wurden.
- `!hint_location <location>` Zeigt das Item auf welches in der angefragten Location zu finden sit. Verbraucht Punkte
  die durch das abarbeiten/checken von Locations "erarbeitet" wurden.

### Collect/Release
- `!collect` Sammelt alle Items die zu deinem Spiel/deiner Welt gehören aus allen anderen Welten ein. Wird normalerweise
  nach erreichen des Ziels für das eigene Spiel benutzt.
- `!release` Sendet alle nicht eingesammelte Items aus deiner Welt zu den jeweiligen Spielern/Welten. Wird normalerweise
  nach erreichen des Ziels für das eigene Spiel automatisch vom Server ausgeführt, kann jedoch auch angepast werden.

### Cheats
- `!getitem <item>` Erzeugt ein gecheatetes extra Item für den ausführenden Spieler, falls dies auf dem Server erlaubt
  wurde.


## Host only (auf Archipelago.gg oder innerhalb der eigenen Server-Befehlszeile)

### Allgemein
- `/help` Listet alle verfügbaren Befehle auf.
- `/license` Listet die Software Lizensinformation auf.
- `/options` Listet die aktuellen Serveroptionen, inclusive dem serverpasswort im Klartext, auf.
- `/players` Listet informationen über alle nicht-/verbundenen Spieler auf.
- `/save` Speichert den aktuellen Stand der Multiworld-Sitzung. Hinweis: der Server speichert automatisch jede Minute.
- `/exit` Fahre den Server herunter.

### Nützliches
- `/countdown <number of seconds>` Startete einen Countdown startend beid er angegebenen Zahl in Sekunden. Nützlich wenn
  man koordiniert gleichzeitig starten möchte. Standardwert ist 10 Sekunden wenn kein Wert mitgegeben wird.
- `/option <option name> <option value>` Änderet eine Serveroption. Für eine Liste aller Optionen führe den Befehl
  `/options` aus.
- `/alias <player name> <alias name>` Weise einem Slotnamen eine Alias zu. Ermöglicht es diesen Alias anstatt des
  Slotnamens für Befehle zu verwenden.

### Collect/Release
- `/collect <player name>` Sammelt alle noch nicht gefundenen Items aus allen Welten ein die zu der Welt gehören. 
- `/release <player name>` Sendet alle noch nicht eingesammelten Items aus der angegeben Welt in die jeweils zugehörige
  Welt. Dies pasiert unabhängig von Server Einstellungen und ob das Ziel erreicht wurde oder nicht
- `/allow_release <player name>` Erlaubt es dem angegebenen Spieler den `!release` Befehl zu benutzen.
- `/forbid_release <player name>` Verbietet es dem angegeben Spieler den `!release` Befehl zu benutzen.

### Cheats
- `/send <player name> <item name>` Erzeugt eine zusätzliche Version/Instanz des angegeben Items und sendet es an den
  angegeben Spieler.
- `/send_multiple <amount> <player name> <item name>` Erzeugt die angegeben Menge an zusätzlichen Versionen/Instanzen
  des angegeben Items und sendet es an den angegeben Spieler.
- `/send_location <player name> <location name>` Sendet das Item in der angegben Location aus der angegeben Welt zum
  Spieler/zur Welt in die das item eigentlich gehört als wäre es nornmal eingesammelt worden.
- `/hint <player name> <item or location name>` Zeigt einen Hinweis für das Item/die Location der angegeben Welt. Dieser
  Hinweis kostet keine Punkte.

<br/> <br/>

# Lokale Befehle

Dies ist eine Liste an lokalen Befehlen welche dir, abhängig vom verwendeten Archipelago Client, zur verfügung stehen
können. Diese Befehle können innerhlab des Clients (ohne Serververbindung) direkt ausgeführt werden.

Die folgende Liste an Befehlen steht dir zur verfügung wenn der Clientt auf dem "CommonClient" aufbaut. Beispiele dafür
sind: TextClient, SNIClient, etc.

- `/connect <address:port>` Verbinde den Client mit dem Multiworld Server unter der angegeben Adressse.
- `/disconnect` Trenne die Verbindung zur aktuellen Multiworldsitzung.
- `/help` Listet alle verfügbaren Befehle auf.
- `/license` Listet die Software Lizensinformation auf.
- `/received` Listet alle Items auf die du von anderen Spielen gesendet bekommen oder selbst gefunden hast.
- `/missing` Listet die Locations, aus Sicht des Servers, auf die noch nicht in deiner Welt abgearbeitet/gechecked
  wurden.
- `/items` Listet die Namen aller Items für das aktuelle Spiel auf.
- `/locations`  Listet die Namen aller Locations für das aktuelle Spiel auf.
- `/ready` Sendet einen Status an den Server, dass der Spieler "bereit" ist.
- Alle Nachrichten die nicht mit einem `/` beginnen werden als normale Nachrichten an alle Spieler gesendet.

## SNIClient Only

die folgenden Befehle stehen nur innerhalb des `SNIClient` für SNES Spiele zu verfügung.

- `/snes` Versucht eine verbindung zum SNES über SNI aufzubauen.
- `/snes_close` Schließt die aktuelle Verbindung zum SNES.
- `/slow_mode` Schaltet den "slow mode" and oder aus, welcher die geschwindigkeit limitiert mit der Items empfangen
  werden.
