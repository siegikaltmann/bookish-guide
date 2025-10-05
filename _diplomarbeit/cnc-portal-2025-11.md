---
title: CNC-Portal – Monatsupdate Nov 2025
date: 2025-11-01
project: CNC-Portal
cover: /assets/cover-diplomarbeit.jpg
---

## Fortschritt
- **Mechanik:** Portalrahmen konstruiert (Aluprofile 30×60), Linearführungen HGR15 ausgewählt.  
- **Antrieb:** Spindeln 1605, NEMA23 ausgelegt, Kupplungen geprüft.  
- **Elektrik:** Netzteil-Topologie festgelegt (48 V/10 A), Endschalterkonzept.

## Tests/Ergebnisse
- Torsionssteifigkeit via einfacher FEM-Vorschau: kritische Stelle an Y-Brücke erkannt → Rippen ergänzt.  
- Spiel der Mutter (1605) gemessen, Kompensation in Software geplant.

## Nächste Schritte
- **Z-Achse** komplettieren (Spindel + Spindelmutterhalter).  
- **Elektronikverdrahtung** (Treiber, Not-Aus, Endschalter).  
- **Firmware/Control:** GRBL bzw. Klipper vergleichen, Schrittauflösung und Max-F aufsetzen.

## Risiken/Blocker
- Lieferzeit Linearwagen (2–3 Wochen).  
- Spindelmuttern-Spiel größer als Datenblatt → Auswahl Alternativlieferant läuft.

## Artefakte
- CAD: STEP export in {{ '/assets/cnc-portal-v3.step' | absolute_url }} (Platzhalter).  
- Doku: Struktur angelegt (Abstract → Anforderungen → Umsetzung → Tests → Fazit).  
