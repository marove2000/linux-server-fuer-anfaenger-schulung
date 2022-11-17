# Die Konsole

Wir arbeiten bei Linux ausschließlich in der Konsole. Die Vorteile:

- Vollständige Konfigurationsmöglichkeiten
- Kennenlernen der wichtigsten Befehle
- Sicher -> Weniger Software installiert
- Grafische Oberfläche für Webserver nicht nötig.

## Welches Tools um sich auf den Server zu verbinden

- Unter Windows: **Putty**
- Unter Linux: **Terminal**

## SSH: Secury Shell

- Netzwerkprotokoll um sich mit entfernten Servern zu verbinden
- Auf nahezu jedem Linux-Server installiert
- Dazu nötig:
    - **Benutzername**
    - **Passwort** oder **SSH-Key**
    - **IP-Adresse** des entfernten Server-Systems
- Befehl auf Linux
> ssh BENUTZERNAME@SERVER-IP
- Mit Windows verwenden wir **putty**: IP-Adresse bei "Host Name (or IP address) eingeben. Restliche Daten werden abgefragt.

    ![](images/putty.png)

Screenshot der PuTTY Eingabemaske

## Einschub: Statt Passwörter besser SSH-Keys verwenden

- Basiert auf Public-Key-Kryptographie
- Sehr viel sicherer als Passwort-Authentifizierung

    ![](images/Public-key-cryptography.svg)
    Private und öffentliche Schlüssel¹

- Beispiel für Private-Key:
    > -----BEGIN OPENSSH PRIVATE KEY-----
    >
    > b3BlbnNzaC1rZXktdjEAAAAABG5vbmUAAAAEbm9uZQAAAAAAAAABAAAAMwAAAAtzc2gtZW
    QyNTUxOQAAACBg5948Lfd3btzKUJkLRfZC9F8oR4Bsqtts/0i6+NEGSAAAAJgMGCOoDBgj
    qAAAAAtzc2gtZWQyNTUxOQAAACBg5948Lfd3btzKUJkLRfZC9F8oR4Bsqtts/0i6+NEGSA
    AAAED841ZSuOfn3jx241Qp6dmNkOMcOsb96r4NATGlhtVY52Dn3jwt93du3MpQmQtF9kL0
    XyhHgGyq22z/SLr40QZIAAAAEnRpbW9AdGhpbmtwYWQtdGltbwECAw==
    > 
    >-----END OPENSSH PRIVATE KEY-----

- Dazugehörige Public-Key:
    > ssh-ed25519 AAAAC3NzaC1lZDI1NTE5AAAAIGDn3jwt93du3MpQmQtF9kL0XyhHgGyq22z/SLr40QZI timo@thinkpad-timo

- Wir kommen später nochmal darauf zurück!

## Tipps & Tricks

- Linux führt Buch über eingegebene Befehle
- Zu finden in der Datei: /home/[user]/.bash_history
- Durchsuchen mit 
  > [STR] + r
- Befehl eingeben nach dem man sucht
- Mit erneutem "[STR] + r" zum nächsten Vorkommen springen

------
¹Quelle: https://de.wikipedia.org/wiki/Asymmetrisches_Kryptosystem#/media/Datei:Orange_blue_public_private_keygeneration_de.svg