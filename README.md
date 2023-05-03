# SYTPiHoleFuchs
Dokumentation zu meiner Installation von meinem PiHole

Raspberry Pi Debian image auf Micro SD-card  geflashed
Karte in Pi eingesteckt und Installation begonnen
Root Benutzer ausgewählt
Diverse packages installiert (curl, sudo, setupcon, wget, etc.)
Installationen wurden folgendermaßen durchgeführt
sudo apt-get update
sudo apt-get install *Paketname, (zum Beispiel Console-setup)*
Tastatursprache wurde mit dem BEfehl setupcon geändert
neuen User (eric) mithilfe von adduser erstellt und ein Passwort ausgewählt
Mit Github Anleitung pihole installiert
https://github.com/pi-hole/pi-hole/#one-step-automated-install
Installation mithilfe des Commands curl -sSL https://install.pi-hole.net | bash	
PUTTY installiert für einfachere Ansicht auf Windows PC, IP Adresse des Pi zur Verbindung angegeben und und mit pi user eingeloggt
![Bild1](https://user-images.githubusercontent.com/126173750/235847837-b6ecf242-3129-4dd9-b826-bd4f3bbf3168.png)
Mit dem Befehl su und dem passwort zu root user gewechselt, da dieser root Rechte hat um die temporäre IP Addresse zu einer permanenten zu ändern
![Bild2](https://user-images.githubusercontent.com/126173750/235847999-7db17ff2-c0df-4648-b5cd-7ffe3304d67e.png)
IP Adresse zu einer permanenten gewechselt, die nicht vom Router vergeben wird (192.168.176.2)
Netzwerk Service neu gestartet für Wirksamkeit mit folgendem Befehl sudo /etc/init.d/networking restart
NAMEN DER DATEI MIT NETZWERKDATEN UNABSICHTLICH GEÄNDERT=>kann nicht mehr darauf zugreifen+gemerkt dass ich Debian 12 installiert habe, wobei das Pi Hole nur mit Debian 11 kompatibel ist, also SD Karte entfernen
## 2.Versuch
Mithilfe des Raspberry Pi Imager und der Debian 11 Bullseye .xz Datei das Betriebssystem auf die Micro SD Karte flashen
Debian 11 installiert und mit root eingeloggt
User eric erstellt für Benutzung von Putty
![Bild3](https://user-images.githubusercontent.com/126173750/235848682-9da7b490-6c1b-45f2-90c1-c07dee85c3f3.png)
Tastatursprache geändert
Console-setup, keyboard-configuration und x11-xkb-utils installiert
Installation funktioniert immer mit: 
sudo apt-get update
sudo apt-get install *Paketname, (zum Beispiel Console-setup)*
und zum Schluss mit dem Befehl setupcon aktiviert
Mit Putty verbunden
Pi hole mithilfe von GitHub Anleitung installiert
![Github Installations Anleitung](https://github.com/pi-hole/pi-hole/#one-step-automated-install)
folgenden Befehl zu Installation der Applikation verwendet
curl -sSL https://install.pi-hole.net | bash
curl not found
sudo und curl packages installiert
curl -sSL https://install.pi-hole.net | bash
static IP address muss definiert werden um mit der Installation fortzufahren

IP Addresse mithilfe von vi so ändern, dass sie nicht vom Router vergeben wird
Gateway richtigstellen
![Bild4](https://user-images.githubusercontent.com/126173750/235849407-09c185df-d548-4e17-8e64-836b209feaca.png)
Einstellungen konfiguriert und Installation abgeschlossen
Admin Webpage login Passwort aufgeschreiben zum Abrufen der Webpage
Beim Router den Raspberry Pi als DNS Server ausgewählt
FERTIG
Mithilfe von WireShark eine VPN nach Hause eingerichtet damit auch unterwegs Werbung unterdrückt wird


Ergebnisse: Ca 3 Stunden nach der INstallation:
![Bild5](https://user-images.githubusercontent.com/126173750/235849787-f97ccefa-0d30-48db-aaf9-a49e85c6e504.png)

Ergebnisse Ca. 3 Tage nach der Installation
![Bild6](https://user-images.githubusercontent.com/126173750/235849995-87a1a9a6-d8c7-42eb-aca2-bd221ec3a311.jpg)
![Bild7](https://user-images.githubusercontent.com/126173750/235849998-0974063a-a6ea-4cc8-b5a0-2b464e016755.jpg)

Innerhalb der drei Tage ist ein Fehler passiert, bei dem eine Amazon URL unterdrückt wurde, die keine Werbung war.
