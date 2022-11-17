# Debugging und Fehlersuche

Nicht immer läuft es so gut. Linux hat den großen Vorteil, meistens genau zu sagen, was schief gelaufen ist. Dazu helfen die geschriebenen Logs.

## Logverzeichnis

Lost meist in

>/var/log

Dort kann mit 

>tail -f

bereits viel erreicht werden. Logmeldungen am besten in Suchmaschinen suchen. Stackoverflow ist euer Freund.

## journalctl

Der Große Log: Das Journal

- Vergleichbar mit dem Windows event-log
- Werden sehr viele Meldungen geschrieben
- Kann automatisiert an andere (externe) Systeme weitergegeben werden

Erreichbar mit 

> journalctl

Meistens sind nur die aktuellsten Meldungen interessant:

> journalctl -f

Wenn man mehr als 10 Meldungen möchte:

> journalctl -f -n1000

Das Journal reicht in der Regel sehr weit zurück. Eine Liste der letzten boots:

> journalctl --list-boots

Anzeige der Logs der letzten boots z.B.

> journalctl -b -1