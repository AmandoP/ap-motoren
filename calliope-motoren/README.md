# Calliope mini – Motoren & Stromversorgung

Interaktiver 3D-Prototyp: Servos und DC-Getriebemotoren am Calliope mini 3 anschließen, mit Strom versorgen und programmieren.
Reine statische Webseite (HTML + JSON + 3D-Modelle), kein Server und kein Build nötig.

## Online stellen mit GitHub Pages

1. Neues Repository anlegen, z. B. `calliope-motoren`.
2. Den Inhalt dieses Ordners hochladen (`index.html`, `motor.json`, `lessons.json`, Ordner `models/`).
3. *Settings → Pages → Branch: `main` / Ordner `/ (root)`* → Speichern.
4. Nach ca. einer Minute läuft die Seite unter `https://<github-name>.github.io/calliope-motoren/`.

Alternativ: Ordner auf <https://app.netlify.com/drop> ziehen oder auf den eigenen Webserver legen.

## Lokal ansehen

Die Seite lädt JSON- und Modelldateien und muss daher über einen Webserver laufen (nicht per Doppelklick):

```sh
cd calliope-motoren
python3 -m http.server 8000
# dann http://localhost:8000 im Browser öffnen
```

## Dateien

| Datei | Inhalt |
|---|---|
| `index.html` | Seite, 3D-Szene und Logik |
| `motor.json` | Inhalte und Einstellungen: Stromversorgungen, Positionen (`layout2`), Infotexte (`info`), Verbindungstexte (`connText`), MakeCode (`prog`, inkl. `shareLinks`) |
| `lessons.json` | Board-Einstellungen, Pinbelegung, Stile und Farben (`styles`) |
| `models/*.glb` | 3D-Modelle (Calliope mini 3, Servoboard, SG90, Getriebemotor, Batteriefächer, Kabel/Stecker) |

Die meisten Änderungen (Texte, Positionen, Farben, MakeCode-Links) gehen ohne Programmierung in den beiden JSON-Dateien.

## Externe Abhängigkeiten

- three.js 0.160.0 über `cdn.jsdelivr.net`
- Schriften (Roboto, Roboto Condensed u. a.) über Google Fonts

## Offene Punkte

- MakeCode: geteilte Projekte für weitere Motor-Kombinationen in `motor.json → prog.shareLinks` eintragen.
- MakeCode-Namen des Motor-Blocks und Servo-Pins (P1, C8–C15) prüfen.
