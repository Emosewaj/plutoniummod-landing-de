# Controller-Unterstützung

<Alert variant="warning">

Du solltest Steams Controller-Unterstützung deaktivieren (oder Steam schließen) bevor du versuchst Controller in Plutonium zu verwenden.
Gehe einfach zu den Steam Einstellungen -> Controller -> Allgemeine Controllereinstellungen und entferne die Häkchen wie unten gezeigt.

![disablesteamcontroller](/images/docs/controllers/U1bs5Z9.png)

</Alert>

## Xbox Controller

Xbox Controller sollten plug-and-play für unsere Spiele sein. Schließe einfach deinen Controller an deinen PC und öffne Plutonium.

## PS4 & PS5 Controller

PS4 und PS5 Controller erfordern eine zusätzliche Software, um außerhalb von Steam unter Windows zu funktionieren.

1\. Lade dir [DS4Windows](https://github.com/Ryochan7/DS4Windows/releases/latest) herunter. Wir empfehlen den Download von `DS4Windows_VERSION_x64.zip`.

2\. Öffne die heruntergeladene zip-Datei und kopiere den `DS4Windows` Ordner in einen sicheren Ort, etwa deinem Dokumenten Ordner.

3\. Öffne den extrahierten Ordner und starte `DS4Windows`

![img](/images/docs/controllers/sxik1Bs.png)

4\. Falls du eine Nachricht wie diese erhältst, klicke auf `Ja`.

![error](/images/docs/controllers/BEqRTW4.png)

4a\. Dein Browser sollte sich nun öffnen und du lädst die Windows x64 Version herunter.

![img](/images/docs/controllers/s2FRt73.png)

4b\. Öffne & installiere .NET.

5\. Versuche es nach der Installation erneut mit DS4Windows.

6\. Wähle `Appdata` als deinen SaveWhere-Pfad.

![img](/images/docs/controllers/3EJ1wzA.png)

7\. Installiere die ViGEmBus Treiber.

![img](/images/docs/controllers/RHrY0Wu.png)

8\. Verbinde deinen PS4 Controller mit deinem PC. Solltest du Bluetooth verwenden, folge den Anweisungen in DS4Windows

9\. Sobald die Verbindung hergestellt ist, klicke auf finish

10\. Konfiguriere deinen Controller und starte DS4Windows im Haupt-Fenster

11\. Gehe ins Spiel und prüfe ob dein Controller funktioniert

Beachte, dass DS4Windows laufen muss damit dein Controller erkannt wird, also stelle sicher, dass "Run At Startup" in den Einstellungen aktiviert ist.

![img](/images/docs/controllers/ps4-final.png)

## PS3 Controllers

Ebenso wie die anderen Playstation Controller erfordern PS3 Controller eine zusätzliche Software, um außerhalb von Steam unter Windows zu funktionieren.
Es gibt dafür mehrere Programme die du benutzen kannst um deinen PS3 Controller zu verbinden, wir werden in diesem Guide ScpToolkit verwenden.

1\. Lade dir [ScpToolkit](https://github.com/nefarius/ScpToolkit/releases/download/v1.7.277.16103-BETA/ScpToolkit_Setup.exe) herunter.

2\. Öffne das heruntergeladene Setup und klicke auf Next ohne Eine Einstellung zu ändern. Klicke am Ende auf `Run Driver Installer`

3\. Befolge alle Anweisungen auf dem Bildschirm und stelle sicher, dass du alles liest (initialisiere den Dualshock-Controller und installiere die erforderlichen Treiber). Durch das Klicken von `Next` wird nichts installiert, du musst auf die auf dem Bildschirm angezeigten Installations-Buttons klicken, wie im Screenshot unten. Du kannstt die Installationen überspringen, die du nicht benötigst, z. B. Bluetooth.

![img](/images/docs/controllers/ps3-1.png)

Falls dein Controller immer noch nicht funktioniert, kannst du `ScpServer application` öffnen (im ScpToolkit Ordner) und es manuell starten. 
Über `ScpSettings application` kannst du Einstellungen, etwa das Aktivieren / Deaktivieren der Vibration, das Ändern der Deadzone der Sticks und andere Dinge ändern.


## Ändern der Nachlade-Aktion

Controller-Benutzer sind es gewohnt, dass die X / Viereck-Taste zum Nachladen verwendet wird, aber auch gedrückt gehalten wird, um die Aktion "Benutzen" auszuführen.
Auf der Tastatur werden dafür auf 2 separate Tasten vertauscht, standardmäßig R zum Nachladen und F zum benutzen.

Um dies zu ändern, tue folgendes:

1. [Öffne die Konsole](/docs/opening-console)
2. Gebe folgendes ein:
```cs
bind r +usereload
```
R sollte nun auf +usereload statt +reload umgetauscht werden. Stelle sicher, dass dein Controller der R-Taste zugeordnet ist und es sollte nun funktionieren.

## Tauschen der Trigger/Bumper

You can switch the triggers and bumpers around by [opening the console](/docs/opening-console) and pasting this in:
Du kannst die Trigger / Bumper wechseln, indem du die [Konsole öffnest](/docs/opening-console) und folgendes einfügst:

```cs
bind BUTTON_LSHLDR "+speed_throw"; bind BUTTON_RSHLDR "+attack"; bind BUTTON_LTRIG "+smoke"; bind BUTTON_RTRIG "+frag"
```
