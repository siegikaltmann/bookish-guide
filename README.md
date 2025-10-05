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
- Dateinamen: nur Kleinbuchstaben, - statt Leerzeichen.
- Datum: YYYY-MM-DD im Front-Matter und im Dateinamen, wenn es chronologisch sortiert werden soll.
- Bilder/PDFs: in assets/ ablegen und so verlinken:
{{ '/assets/datei.png' | absolute_url }} oder relative_url – du nutzt absolute_url.
- Cover-Bild (optional): Front-Matter cover: /assets/dein-bild.jpg (ideal 1200×630).



