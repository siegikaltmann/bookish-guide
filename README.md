# bookish-guide

## Dateien:
Wie einbinden:
Lade die Dateien in deinem Repo in den Ordner assets/ hoch.
Die vorhandenen Verweise im Setup passen ideal:
Start-Kacheln greifen auf:
assets/cover-lab.jpg
assets/cover-mb.jpg
assets/cover-diplomarbeit.jpg

In Beiträgen/Seiten kannst du so verlinken:

```markdown
[Labor-Kurzleitfaden (PDF)]({{ '/assets/labor-kurzleitfaden.pdf' | relative_url }})
```

```yaml
cover: /assets/cover-lab.jpg
```
