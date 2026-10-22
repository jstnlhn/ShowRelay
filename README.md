# ShowLink

**Live-Daten aus dem Pioneer Pro DJ Link Netzwerk – Waveforms, Timecode und Tempo-Sync für Licht, Video und Bühne.**

ShowLink verbindet sich mit DJM-Mixern und CDJ-Playern im Pro DJ Link Netzwerk und stellt alle Informationen der
laufenden Show in Echtzeit dar: Track, Tempo, Position, Waveform und On-Air-Status jedes Decks. Daraus erzeugt ShowLink
Timecode, MIDI Clock, OSC und Tempo-Sync für Lichtpulte – und bringt einen DJ-Timer fürs Tablet gleich mit.

[**→ Aktuelle Version herunterladen**](https://github.com/jstnlhn/ShowController/releases/latest)

---

## Funktionen

### Anzeige
- **Bis zu 6 Player** gleichzeitig, z. B. DJM-A9 mit CDJ-3000
- **Farbige Waveforms** (RGB wie am CDJ-3000, 3-Band oder Blau) mit Beat-Raster und Abspielposition
- **On-Air-Erkennung** direkt über die Kanalfader des Mixers
- **Tempo-Master, Sync, Pitch, Key, Restzeit** pro Deck; Restzeit-Warnung mit einstellbaren Schwellen
- Auch Tracks, die nicht mit rekordbox analysiert wurden: Die Waveform erscheint, sobald der CDJ die Analyse abgeschlossen hat

### Ansichten
| Ansicht | Inhalt |
|---|---|
| **DATA** | Netzwerk, Mixer, alle Geräte und Player-Daten in Tabellenform, automatische Tracklist |
| **VIEWER** | Alle Decks mit Waveform im Überblick |
| **LIVE** | Das Deck, das gerade läuft und on air ist – groß und gut lesbar |
| **MASTER** | Alle Decks übereinander, das führende Deck hervorgehoben |
| **OUTPUT** | Timecode-Quelle und alle Ausgänge |
| **REMOTE** | Web-Ansicht für Smartphone, Tablet oder Zweitrechner (mit QR-Code) |
| **TIMER** | Timetable und DJ-Timer für die Bühne |
| **SETUP** | Anzeige, Start, Sprache, Updates, Lizenz |

### Timecode
- **LTC** (SMPTE als Audiosignal) über jede Soundkarte
- **MTC** (MIDI Timecode)
- **Art-Net Timecode** (UDP 6454)
- 24, 25, 29,97 DF und 30 fps, frei einstellbarer Offset, Deck-Nummer als Stunde
- Folgt dem Tempo-Master, dem On-Air-Deck oder einem festen Deck – inklusive Pitch, Loops, Hot Cues und Scratching

### Weitere Ausgänge
- **MIDI Beat Clock** (24 PPQN) im Tempo des Decks, optional mit Start/Stopp
- **OSC** – BPM, Position, Beat, On-Air-Status und Track-Infos aller Decks
- **Web-Viewer und JSON-Schnittstelle** (`/data.json`) für Overlays und eigene Integrationen

### Tempo-Sync für grandMA2
- Übertragung per Telnet direkt an einen Speedmaster
- **BPM** setzen, **Tap (Learn)** im Takt des On-Air-Decks oder **Tap auf Kicks** anhand der Waveform
- Breakdown-Erkennung: In Passagen ohne Bass wird das Tempo automatisch geteilt
- Speed auf 0 bei Stopp oder wenn keine Kicks mehr kommen

### DJ-Timer
- Timetable mit Start- und Endzeiten, auch über Mitternacht
- **Stage-Ansicht fürs Tablet**: aktueller DJ, Countdown in Grün/Gelb/Rot, nächster DJ, Uhrzeit
- **Nachrichten an den DJ** („Letzter Track“, „Bitte zum Ende kommen“ …) mit einem Klick
- Verwaltung im Browser von jedem Gerät aus, passwortgeschützt

### Betrieb
- Vollbild auf beliebigem Monitor, Start mit Windows, Start direkt im Vollbild
- Oberfläche in **Deutsch, Englisch und Niederländisch**
- Automatische Updates – nur nach Bestätigung und nie während der Wiedergabe
- Firewall-Einrichtung für Pro DJ Link mit einem Klick

---

## Systemvoraussetzungen
- Windows 10 oder 11 (64 Bit)
- LAN-Verbindung zum Switch des Pro DJ Link Netzwerks
- Java ist im Setup enthalten, es muss nichts zusätzlich installiert werden

## Installation
1. `ShowLink-Setup-<Version>.exe` unter [Releases](https://github.com/jstnlhn/ShowController/releases/latest) herunterladen und ausführen.
2. Im Setup die Firewall-Freigabe aktiviert lassen.
3. ShowLink starten und oben rechts den Netzwerkadapter wählen, der mit dem Switch verbunden ist.

## Lizenz
ShowLink kann **14 Tage kostenlos getestet** werden. Danach ist ein Lizenzschlüssel erforderlich
(SETUP → LIZENZ). Nach der Aktivierung läuft ShowLink bis zu 30 Tage ohne Internetverbindung.
Lizenzen auf Anfrage.

---

Entwickelt von J.Lühn

<sub>CDJ, DJM, rekordbox und PRO DJ LINK sind Marken oder eingetragene Marken der AlphaTheta Corporation.
Pioneer DJ ist eine Marke der Pioneer Corporation und wird von AlphaTheta unter Lizenz verwendet.
grandMA2 ist eine Marke der MA Lighting International GmbH. ShowLink ist ein unabhängiges Produkt und wird von
AlphaTheta, Pioneer und MA Lighting weder hergestellt noch unterstützt.</sub>
