
# Unifi SSH Tools

**_ACHTUNG:_** Das Tools Kit basiert auf `plink`. `plink` ist ein Programm aus der Putty-Suite. Für eine Reibungslose Funktion muss die Putty-Suite auf dem Gerät installiert sein!


Das Unifi SSH Tools Kit ermöglicht es Unifi Geräte in Masse zu verwalten und Commands auf dem Gerät auszuführen. Der Ursprüngliche einsatzzweck war es eine Masse an Access Points zurück zu setzen.

# Installation

1. Lade unter Releases die neueste Version als .zip Datei herunter. [Letzer Release](https://github.com/zipposativ/unifi-ssh-tool/releases/latest)
2. Enpacke das Verzeichnis. Im Verzeichnis liegen die `unifi-devices.csv` & die `unifi-ssh-tools-kit.exe`. 

## Beispiel: unifi-devices.csv

```csv
ipv4
10.20.255.1
10.20.255.2
10.20.255.3
```
# SSH Zugangsdaten ermitteln
Nachdem man sich bei dem Network Manager angemeldet hat wählt man seine Site aus. Hier Navigiert man bei der Unifi UDM oder Network Appliance zu `Settings > System > Advanced`. Findet man den Punkt: `Device Authentication` und dort sind die SSH Zugangsdaten aufgeführt.

# Das Programm Ausführen
1. Die `unifi-ssh-tools-kit.exe` muss ausgeführt werden.
2. Im selben Verzeichnis muss die `unifi-devices.csv` liegen!
3. Im Bereich Commands muss aus dem Select der passende Command ausgewählt werden. Wird der Command `set-inform` ausgewählt muss die IPv4 der UDM oder der Network Appliance angegeben werden.
4. Im Bereich Login werden die SSH-Zugangsdaten angegeben.
5. Es muss der `Ausfuehren` Button gedrückt werden, damit die Aktion gestartet werden. Es wird eine Statusanzeige in einem PopUp Fenster angezeigt.

# Commands-Liste

| Command | Beschreibung |
| -------- | ------- |
| info |  Zeigt eine Liste an Information zu dem Gerät |
| uptime | Zeigt an wie lange das Gerät auf dem Status ON steht |
|poweroff|Schaltet das Gerät aus (Muss manuell gestartet werden [Bei PoE Geräten= PoE Cycle]|
|reboot|Startet das Gerät von Grundauf neu|
|syswrapper.sh restore-default|Setzt das Gerät auf Werkseinstellung zurück|
|set-inform + IPv4|Stellt eine Adopt Anfrage an die UDM oder Network Appliance|
|ip-a|Listet alle Netzwerk Interfaces mit MAC-Address, IPv4, IPv6 & State auf|
