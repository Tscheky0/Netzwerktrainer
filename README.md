# Netzwerk-Trainer 3D

Lernspiel für Netzwerktechnik als 3D Korridor im Browser. Du stehst vor vier Türen, über den Türen steht die Frage, die richtige Tür bringt dich einen Raum weiter, eine falsche wirft dich zurück. Am Ende wartet das Ziel.

Eine einzige HTML Datei, kein Build, keine Installation, kein Server. Three.js ist direkt eingebettet, die Datei läuft deshalb auch komplett offline.

## Starten

Datei `Netzwerk-Trainer.html` herunterladen und im Browser öffnen. Fertig.

Für GitHub Pages die Datei in `index.html` umbenennen und unter Settings, Pages den Branch `main` aktivieren.

## Inhalt

16 Themen, 1185 Fragen, 3 Schwierigkeitsstufen (leicht, mittel, schwer). Subnetting Aufgaben werden zusätzlich deterministisch generiert, der Rechenweg in der Erklärung stimmt dadurch immer.

| Thema | Fragen |
|---|---|
| Subnetting | 291 |
| Ports | 84 |
| OSI | 79 |
| TCP/UDP | 69 |
| DNS | 65 |
| Switches | 63 |
| Router | 63 |
| Kabel | 59 |
| Netz-Typen | 58 |
| DHCP | 58 |
| Frames | 58 |
| Sicherheit | 52 |
| Praxis | 51 |
| IPv6 | 47 |
| Cisco CLI | 46 |
| WLAN | 42 |

Neben Multiple Choice gibt es Eingabefragen, bei denen Netz-ID oder Broadcast selbst getippt werden.

## Spielmodi

| Modus | Regel |
|---|---|
| Klassisch | falsch bedeutet ein Raum zurück |
| Lernmodus | kein Zurück, Erklärung ohne Countdown |
| Prüfung | Auflösung erst am Ende |
| Blitz | 7 Sekunden pro Frage, immer vorwärts |
| Sudden Death | ein Fehler beendet die Runde |
| Fehler-Training | nur Fragen, die früher falsch waren |

Zusätzlich einzeln zuschaltbar: Zeitdruck (20 Sekunden pro Frage), 3 Leben statt Zurücksetzen und Sound.

## Funktionen

* Auswahl nach Thema und Schwierigkeit, Anzahl der Fragen bis 200 per Regler
* Nach jeder Antwort bleibt die Erklärung 12 Sekunden stehen, mit Countdown und Weiter Button
* Live Uhr pro Frage, Gesamtzeit am Ende
* Serie: nach 5 richtigen Antworten in Folge wird der nächste Raum übersprungen
* Spaced Repetition: falsch beantwortete Fragen werden in späteren Runden bevorzugt gezogen
* Statistik mit Fehlerquote pro Thema über alle Runden
* Rekord pro Auswahl aus Thema, Stufe, Anzahl und Modus
* Review am Ende mit allen falschen Fragen und der richtigen Antwort
* Seed Feld: gleicher Seed ergibt dieselben Fragen in derselben Reihenfolge, zum Vergleichen mit anderen
* Abschlussbewertung in vier Stufen mit Prozentring

## Bedienung

Per Maus oder Touch auf die richtige Tür gehen. Bei Eingabefragen die Adresse eintippen und mit Enter bestätigen.

## Daten

Alles bleibt im Browser (`localStorage`). Es werden keine Daten gesendet und es gibt keine externen Anfragen. Statistik, Fehlerpool und Rekorde lassen sich im Statistik Screen zurücksetzen.

## Technik

HTML, CSS und JavaScript in einer Datei, Rendering mit Three.js (r160, MIT Lizenz), Sound über Web Audio API, Oberfläche im Glas Stil mit `backdrop-filter`.
