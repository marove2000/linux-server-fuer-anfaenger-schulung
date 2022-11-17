# Programme installieren

## Paketmanager

Linux verwendet für die Installation Paketmanager, die bereits eine vielzahl von Programmen zur Verfügung stellen kann. Auf Ubuntu: apt

Vorteile:

- Installieren mit nur einem Befehl
- Installation ist auf das Betriebssystem abgestimmt
- Alle nötigen Grundkonfigurationen werden bereits angelegt
- Update aller Pakete mit nur einem Befehl
- Automatische Updates möglich

> sudo apt update

Updated das Paket-Repository (Den Paketkatalog).

> sudo apt upgrade

Bringt alle Pakete auf den neusten Stand.

### Beispiel: Installation von "btop"

Hinweis: Wir benötigen hier den Befehl "sudo" (Eselsbrücke "Super-Do"). Danach kommt eine Passwortabfrage. Dazu später mehr.

> sudo apt search btop

Sucht im Paketkatalog nach allen Paketen mit diesem Namen.

> sudo apt show btop

Gibt weiter Informationen, wie Version, Beschreibung und Download-Size von "btop" wieder.

> sudo apt install btop

Installiert btop und alle nötigen Abhänigkeiten.

## Programme (Auto-)Starten, Neustarten und Beenden


### Was ist Systemd?

systemd istt ein System- und Sitzungs-Manager (Init-System), der für die Verwaltung aller auf dem System laufenden Dienste über die gesamte Betriebszeit des Rechners, vom Startvorgang bis zum Herunterfahren, zuständig ist.

> sudo systemctl list-units

Liste aller möglichen Programme die gerade laufen oder gestartet werden können.

> sudo systemctl list-timers

Liste der automatisch ablaufenden Jobs und wann diese zuletzt liefen und demnächst wieder laufen werden.

> sudo systemctl status ssh

Status des Service ssh

### Enable

Die meisten Programme werden automatisch in den autostart gelegt. Manchmal muss dies aber noch erledigt werden:

> sudo systemctl enable [SERVICE].service

Start und Stop einfach über den Befehl "start" bzw. "stop

> sudo systemctl start [SERVICE]

> sudo systemctl stop [SERVICE]

> sudo systemctl restart [SERVICE]
