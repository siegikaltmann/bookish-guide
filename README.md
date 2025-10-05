# bookish-guide

## Dateien - wie einbinden als Assets (Vorschaubilder)
Lade die Dateien in deinem Repo in den Ordner assets/ hoch.
Die vorhandenen Verweise im Setup passen ideal:
Start-Kacheln greifen auf:
assets/cover-lab.jpg
assets/cover-mb.jpg
assets/cover-diplomarbeit.jpg

In Beiträgen/Seiten kannst du so verlinken:

```markdown
Markdown

[Labor-Kurzleitfaden (PDF)]({{ '/assets/labor-kurzleitfaden.pdf' | relative_url }})
```

```yaml
yaml

cover: /assets/cover-lab.jpg
```
## Neue Einträge – so schnell geht’s
Wöchentlicher Labor-Eintrag: neue Datei unter _lab/YYYY-MM-DD-kurzer-titel.md mit date + Inhalt.

Neues Kapitel (Maschinenbau): Datei unter _maschinenbau/kapitel-NN-titel.md mit weight.

Monatliches Diplom-Update: Datei unter _diplomarbeit/projektname-YYYY-MM.md mit date + project: Projektname.

Damit bleiben alle Listen automatisch aktuell – die Startseite verlinkt sauber über die Kacheln.

## 🚥 Allgemein (gilt für alle)
- Dateinamen: nur Kleinbuchstaben, `-` statt Leerzeichen.
- Datum: `YYYY-MM-DD` im Front-Matter und im Dateinamen, wenn es chronologisch sortiert werden soll.
- Bilder/PDFs: in `assets/` ablegen und so verlinken:
`{{ '/assets/datei.png' | absolute_url }}` oder `relative_url` – du nutzt `absolute_url`.
- Cover-Bild (optional): Front-Matter `cover: /assets/dein-bild.jpg` (ideal 1200×630).

1. ## 🧪 _lab — „Wöchentlicher Fortschritt“
- Ordner: `_lab/`
- Listen-Seite: `lab/index.md` (nutzt `layout: list`)
- So legst du eine Woche an
-- Dateiname: `_lab/2025-10-12-woche-02.md`

```
---
title: Woche 02 – PWM & Servo
date: 2025-10-12
cover: /assets/cover-lab.jpg
excerpt: "PWM-Grundlagen, Servo ansteuern, sanfter Start."
tags: [pwm, servo, micropython]
---

## Ziele
- PWM verstehen (Frequenz, Duty).
- Servo an GP15 mit 50 Hz bewegen.

## Code (MicroPython)
```python
from machine import Pin, PWM
import time
servo = PWM(Pin(15)); servo.freq(50)
def angle(a):
    us = 500 + (2000*a/180); duty = int(us/20000*65535); servo.duty_u16(duty)
for a in range(0,181,15):
    angle(a); time.sleep(0.2)
```

## Aufgaben
1. Sweep 20°↔160° mit 2°-Schritten.
2. Button = Positionssprung (0°/90°/180°).

```Yaml
**Tipps**
- Jede Woche = **eine Datei** mit `date:`.  
- Bilder: `![Aufbau]({{ '/assets/w02-aufbau.jpg' | absolute_url }})`  
- PDF-Beilage: `[Handout]({{ '/assets/labor-kurzleitfaden.pdf' | absolute_url }})`
```
---

2. ## ⚙️ _maschinenbau — „Kapitel & Übungen“
**Ordner:** `_maschinenbau/`  
**Listen-Seite:** `maschinenbau/index.md` (sortiert nach `weight`)

## Neues Kapitel
**Dateiname:** `_maschinenbau/kapitel-03-kinematik.md`
```markdown
---
title: Kapitel 3 – Kinematik
weight: 3
---

### Lernziele
- Weg, Geschwindigkeit, Beschleunigung.

### Formeln
- v = s / t  
- a = Δv / Δt

### Übung
1) Ein Wagen legt 24 m in 3 s zurück. v = ?  
2) v steigt von 2→8 m/s in 4 s. a = ?
```

## Tipps
- Reihenfolge nur über `weight` steuern.
- Math: Kramdown/KaTeX-Style geht mit Inline-$…$ und Block-Formeln (einfach halten).




