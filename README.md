OOT SAMMEL-CHECKLISTEN 2.7 - WINDOWS EDITION
================================================

Eine lokale Ocarina-of-Time-Sammelcheckliste fuer Windows mit insgesamt
224 abhakbaren Eintraegen.

ENTHALTEN
---------
- 36 Herzteile
- 100 Goldene Skulltulas
- 11 Schritte des Biggoron-Tauschgeschaefts
- 8 Masken
- 10 Nachtschwaermer
- 10 Wundererbsen
- 4 Flaschen
- 12 Ocarina-Lieder
- 23 Ausruestungsgegenstaende und Upgrades

Die Eintraege enthalten Fundorte, verstaendliche Beschreibungen,
Voraussetzungen wie Alter, Items, Lieder, Tageszeit und Questfortschritt,
Notizen, Such-/Filterfunktionen und Fortschrittsanzeigen.

SYSTEMVORAUSSETZUNGEN
---------------------
- Windows 10 oder Windows 11
- Python 3.8 oder neuer fuer die lokale App
- Ein aktueller Browser (Edge, Firefox, Chrome usw.)

Python bekommst du von:
https://www.python.org/downloads/windows/

Bei der Python-Installation am besten "Add python.exe to PATH" aktivieren.
Die App benutzt nur die Python-Standardbibliothek; pip-Pakete sind nicht
noetig.

INSTALLATION - EMPFOHLEN
------------------------
1. Das ZIP vollstaendig entpacken.
2. Doppelklick auf INSTALLIEREN-WINDOWS.cmd.
3. Danach findest du "OoT Sammel-Checklisten" im Windows-Startmenue.
4. Die Checkliste startet lokal und oeffnet sich in deinem Standardbrowser.

Die Programmdaten werden normalerweise installiert nach:
%LOCALAPPDATA%\Programs\OoT-Sammel-Checklisten

Der Spielstand liegt getrennt unter:
%LOCALAPPDATA%\OoT-Sammel-Checklisten\data

Dadurch bleibt dein Fortschritt bei einem Programm-Update erhalten.

PORTABLE STARTEN
----------------
Wenn du nichts installieren moechtest, kannst du im entpackten Ordner
STARTEN-WINDOWS.cmd doppelklicken.

OHNE PYTHON
-----------
DIREKTSTART.html laeuft ohne Python direkt im Browser. Diese Variante
speichert den Fortschritt im Browser und verwendet deshalb einen getrennten
Spielstand. Fuer Wechsel zwischen den Varianten am besten eine JSON-Sicherung
exportieren/importieren.

BEENDEN
-------
In der App: "Sichern & verwalten" > "App beenden".
Alternativ: STOPPEN-WINDOWS.cmd.

DIAGNOSE
--------
DIAGNOSE-WINDOWS.cmd erstellt eine Startdiagnose. Sie enthaelt keine
Haekchen, Notizen oder Sitzungstoken.

UPDATE
------
Eine neue Windows-Version wieder vollstaendig entpacken und
INSTALLIEREN-WINDOWS.cmd ausfuehren. Der vorhandene Spielstand im separaten
Datenordner bleibt bestehen.

DEINSTALLATION
--------------
Doppelklick auf DEINSTALLIEREN-WINDOWS.cmd entfernt das Programm und den
Startmenue-Eintrag. Der Spielstand bleibt standardmaessig erhalten.

WICHTIG
-------
Dies ist ein inoffizielles Fanprojekt und steht nicht mit Nintendo in
Verbindung. The Legend of Zelda, Ocarina of Time sowie zugehoerige Namen und
Marken gehoeren ihren jeweiligen Rechteinhabern. Siehe LIZENZ.txt und
QUELLEN.txt.

OOT SAMMEL-CHECKLISTEN 2.2 - NOBARA EDITION
========================================

NEU IN 2.5
----------
- Alle 224 Sammel-Eintraege besitzen jetzt eine sofort sichtbare Offline-Kurzbeschreibung.
- Die Beschreibungen funktionieren ohne Internet.
- Bilder & Texte laden kann weiterhin laengere Detailtexte von den hinterlegten Quellen nachladen.
- Bestehende Haken, Notizen und Sicherungen aus 2.2 bleiben kompatibel.
Lokale Linux-App fuer deine zehn Ocarina-of-Time-Checklisten.
Keine offizielle App von Nintendo, Nobara oder Zelda Chronicles.

DER EINFACHSTE WEG: EINZELDATEI-INSTALLER
--------------------------------------
Die Datei OoT-Nobara-Installieren.run herunterladen und im Ordner mit
DIESER Datei ein Terminal oeffnen. Dann:

    sh OoT-Nobara-Installieren.run

Nicht mit sudo ausfuehren. Kein chmod und kein manuelles Entpacken noetig.
Der Installer entpackt voruebergehend, installiert im eigenen Benutzerkonto
und startet anschliessend die installierte Kopie. Der temporaere Ordner
wird danach aufgeraeumt. Die installierte App ist davon unabhaengig.

DANACH: Im App-Menue nach "OoT Sammel-Checklisten" suchen.
Das Programm oeffnet sich im Browser, laeuft aber lokal auf deinem Rechner.
Ein Terminal muss dabei nicht offen bleiben. Es gibt kein Online-Konto.
Dies ist eine lokale Browser-App, kein Qt-Fenster und keine Flatpak-Datei.

UPDATE: Offene Notizen zuerst speichern. Eine laufende alte App unter
"Sichern & verwalten > App beenden" schliessen. Nur den Tab zu schliessen
beendet den lokalen Server nicht. Der Installer beendet keine laufende
Version ungefragt. Nach dem Speichern ist alternativ moeglich:

    sh OoT-Nobara-Installieren.run --restart

Nur installieren, noch nicht starten:

    sh OoT-Nobara-Installieren.run --install-only

Installation und Start ohne Internetabruf oder Browseroeffnung:

    sh OoT-Nobara-Installieren.run --no-download --no-browser

ALTERNATIV: DAS ZIP-ARCHIV
-------------------------
Das GANZE ZIP entpacken. Im Ordner "oot-checkliste-nobara" ein Terminal
(Nobara KDE: Konsole) oeffnen. Installieren UND starten:

    sh NOBARA-INSTALLIEREN.sh

Nur starten, ohne Installation:

    sh STARTEN.sh

Nur ins Benutzerkonto installieren:

    sh INSTALLIEREN.sh

Startdiagnose:

    sh DIAGNOSE.sh

Nach dem Speichern der Notizen den Server beenden:

    sh STOPPEN.sh

WAS FUER NOBARA ANGEPASST WURDE
------------------------------
- Der Starter bevorzugt /usr/bin/python3 und verwendet den isolierten
  Python-Modus. Fremde PYTHONHOME/PYTHONPATH- und Benutzer-Pakete sollen
  den Start nicht stoeren. Keine pip-Installation erforderlich.
- Kein Wine, kein FUSE/AppImage und keine zusaetzliche GUI-Bibliothek.
- Browseroeffnung ueber den Desktop (xdg-open/gio); native Browser und
  gaengige installierte Flatpak-Browser dienen als weitere Startwege.
- Wayland bleibt aktiv. Kein Erzwingen von X11 oder Grafiktreiber-Flags.
- Der App-Menue-Eintrag startet ohne Terminal. Fehler erscheinen mit
  kdialog/zenity, wenn verfuegbar, alternativ als Protokoll/Meldung.
- Installation braucht kein Root. Sicherheitsdienste, Firewall,
  Browserprofile, Standardbrowser und Systempakete werden NICHT geaendert.
- Programmdateien werden zuerst in einem Zwischenordner vorbereitet.
  Bei einem Installationsfehler wird die vorherige Programmkopie
  wiederhergestellt. Alte Programmdateien bleiben zusaetzlich erhalten.
- Startprotokoll und Diagnose sind lokal. Es gibt keine Telemetrie.

VORAUSSETZUNGEN / FEHLENDE PAKETE
-------------------------------
Python 3.8+ und ein aktueller Browser. Der normale Nobara-Systeminterpreter
ist vorgesehen; die tatsaechlich installierte Python-Version wird erkannt.
Der Installer laedt KEINE Abhaengigkeiten automatisch nach.
Wenn Python oder der Desktop-Browser-Oeffner fehlen, kann man auf Nobara
gezielt nachinstallieren:

    sudo dnf install python3 xdg-utils

Nur dieser Paketverwaltungsbefehl benoetigt sudo, NICHT unsere App.
Bei fehlendem Standardbrowser einen vorhandenen Browser normal in den
Systemeinstellungen auswaehlen. Alternativ die angezeigte lokale
Browser-Adresse aus dem Terminal kopieren. Im Programmordner entsteht
auch APP_IM_BROWSER.html mit einem Link zur laufenden Sitzung.
Die Meldung "Browser-Anfrage uebergeben" bedeutet, dass der Oeffner die
Anfrage angenommen hat; sie ist kein Beweis fuer ein sichtbares Fenster.

DEINE HAEKCHEN BLEIBEN ERHALTEN
----------------------------
Datenformat und Standard-Speicherordner sind gleich wie in Version 2/2.1:

    ~/.local/share/oot-herzteil-checkliste/fortschritt-v2.json

Notizen und lokale Bilder werden mit weiterverwendet. Bei der Installation
werden vorhandene Fortschrittsdateien zusaetzlich als *-vor-nobara-*.json
kopiert. V1-Herzteile koennen weiterhin automatisch uebernommen werden.
Voraussetzung: gleiches Linux-Benutzerkonto, gleicher Datenordner und
lesbare Dateien. XDG_DATA_HOME und OOT_CHECKLIST_DATA_DIR werden beachtet.

WICHTIG BEI DER FRUEHEREN DIREKTSTART-HTML:
Deren Browser-Spielstand ist getrennt. Dort "Sicherung speichern" verwenden
und in der Nobara-App "Sichern & verwalten > Sicherung laden" waehlen.
Eine JSON-Sicherung aus Version 2 ersetzt den gesamten Listenfortschritt;
vorher wird der aktuelle Stand gesichert. Eine V1-Sicherung betrifft nur
Herzteile. Browserdaten koennen nicht ungefragt automatisch gelesen werden.
Die enthaltene DIREKTSTART.html ist die unveraenderte Notfallvariante 2.1.

CHECKLISTEN UND BILDER
---------------------
 36 Herzteile                  100 Goldene Skulltulas
 11 Tauschgeschaeft               8 Maskenhandel
 10 Nachtschwaermer              10 Feen und Feenquellen
 10 Wundererbsen                  4 Flaschen
 12 Ocarina-Lieder               23 Ausruestung und Upgrades
224 separat abhakbare Listenpunkte, unveraendert aus deiner Version 2.1.
Das ist kein offizieller 100%-Spielwert. Ueberlappende Belohnungen werden
in unterschiedlichen Listen weiterhin getrennt abgehaekt.

Die Bildzuordnungen und Galerien sind erhalten. Die 273 hinterlegten
Bildadressen sind KEINE eingebetteten Originalbilddateien. Der erste
Download von Zelda Chronicles braucht Internet; erfolgreich gespeicherte
Bilder bleiben lokal verfuegbar. "Sichern & verwalten > Alle Bilder & Texte
laden" startet das Laden erneut. Weitere Galeriebilder koennen aus den
Originalseiten erkannt werden. Die App funktioniert auch ohne Bilddownload.

Ohne Netzwerkzugriff starten (vorher laufende App beenden):

    sh STARTEN.sh --no-download

Eine bereits laufende Sitzung behaelt ihren bestehenden Netzwerkmodus.
Der Live-Download der Originalbilder war im Erstellungsumfeld wegen
fehlender DNS-Aufloesung nicht pruefbar. Keine falschen Ersatzbilder.

DIAGNOSE BEI STARTPROBLEMEN
-------------------------
Im Programmordner: sh DIAGNOSE.sh
Oder im App-Menue Rechtsklick auf die App > Startdiagnose anzeigen.
Oder in der App: Sichern & verwalten > Diagnose-Datei speichern.

Die Datei OoT-Nobara-Diagnose.txt nennt Desktop, Sitzungstyp, Python,
Programmdateien, Schreibtest und lokalen Porttest. Sie fuehrt KEINEN
Internettest aus und enthaelt keine Notizen/Haekchen/Sitzungstoken.
Bitte trotzdem vor dem Teilen durchsehen.

Standardpfade:
Programm:  ~/.local/share/oot-herzteil-checkliste-programm/
Daten:     ~/.local/share/oot-herzteil-checkliste/
Startlog:  ~/.local/state/oot-checklisten/letzter-start.log
Serverlog: ~/.local/share/oot-herzteil-checkliste/programm-v2.log

Alle Listenpunkte werden sofort als Dateien gespeichert, nicht in einem
Browserprofil. Nach einem Neustart der App bitte den neuen Browser-Tab
benutzen: alte Sitzungstoken werden aus Sicherheitsgruenden ungueltig.

TESTGRENZEN
-----------
Funktionstests wurden in einer Linux-Testumgebung ausgefuehrt, nicht auf
einem echten Nobara-Desktop. Siehe TESTBERICHT.txt im Archiv. Ein Test
ersetzt nicht die Pruefung auf deinem konkreten KDE/GNOME-System.
