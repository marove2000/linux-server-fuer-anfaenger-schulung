# Die Befehle

## Aufbau von Befehlen

> BEFEHL [Optionale weitere Befehle] -[Parameter] -[Parameter] -[Parameter]

Beispiel:

> ssh ansilbe@s00.linux.lff.bybn.de -v -oPubkeyAuthentication=no

- Befehl: ssh
- Benutzer: ansilbe
- Server: s00.linux.lff.bybn.de
- Parameter: -v -> verbose (ausführlich, zeigt viel mehr Informationen an. Hilfreich bei debugging)
- Parameter: -o -> option (Verschiedene Optionen die dem SSH-Komando mitgegeben werden können. Im Beispiel: Benutze keine SSH-Keys)

## Hilfe für Befehle (man pages)

> man [BEFEHL]

Beispiel:

> man ssh

* Suche innerhalb von man mit "/[SUCHWORT]"
* Springe zum nächsten Fundort: "n"-Taste

## History
* Die 500 letzten Befehle werden in der History gespeichert
* Gespeichert in der Datei: ~/.bash_history
* Befehl "history" zeigt die letzten Befehle
* Auch erreichbar unter [STR]+r

## Nützliche allgemeine Befehle
> exit

Schließt die aktuelle Sitzung

> clear

Löscht alles auf dem Bildschirm, es geht nichts verloren, es wird lediglich der bildschrim aufgeräumt

> grep

Durchsuchen von Textdateien (siehe Pipes). Achtung: Case-Sensitive

> find

Suche nach Dateien (dazu später mehr)

## Es wird schwieriger: Pipes

Pipes ( | ) sind mit [ALT]+[>] erreichbar. Damit können Ausgaben an weitere Befehle weitergeleitet werden.

Beispiel:
> man ssh | grep Verbose

Ausgabe: Die Zeile (oder Zeilen) in denen das Wort vokommtq

>      -v      Verbose mode.  Causes ssh to print debugging messages about its progress.  This is helpful in debugging connection, authentication, and configuration problems.  Multiple -v options increase the verbosity.  The maximum is 3.



## Tipps und Tricks
- Die [TAB]-Taste ist dein Freund! Es werden mögliche Befehle angezeigt und automatisch ausgefüllt/erweitert
- man-Pages sind am Anfang extrem wichtig, diese gibt es auch online (Google: "man ssh")
- History 