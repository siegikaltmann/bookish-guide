---
title: Kapitel 4 – Statik: Kräfte & Momente
weight: 4 # Nummerierung
---

## Lernziele
- Freikörperbild (Free Body Diagram, FBD) erstellen.
- Gleichgewichtsbedingungen anwenden: $\sum F = 0$, $\sum M = 0$.
- Resultierende & Moment berechnen.

## Begriffe
- **Kraft** $\\vec F$ in N, **Moment** $M = F \\cdot r_\\perp$ in N·m  
- **Gleichgewicht in der Ebene:**  
  $\\sum F_x = 0,\\ \\sum F_y = 0,\\ \\sum M_Z = 0$

## Vorgehen (FBD)
1. Körper **frei schneiden** (Lager, Kontakte ersetzen durch Reaktionskräfte).  
2. **Alle Kräfte** eintragen (Gewicht, Zug/Druck, Reibung, Reaktionskräfte).  
3. **Bezugspunkt** wählen (für Momente).  
4. Gleichungen aufstellen, **unbekannte Reaktionen** lösen.

## Beispiel
Ein Balken (Länge $L=2\\,\\mathrm{m}$) ist links **fest gelagert** (A) und rechts **loslager** (B). In der Mitte wirkt $F=200\\,\\mathrm{N}$ nach unten.  
Gesucht: Auflagerreaktionen $A_x, A_y, M_A$ und $B_y$.

**Lösungsskizze:** (FBD)  
- Kräfte: $A_x, A_y, B_y$, Last $F$ in der Mitte.  
- Momente um A: $\\sum M_A = 0 = -F\\cdot L/2 + B_y\\cdot L \\Rightarrow B_y = F/2 = 100\\,\\mathrm{N}$  
- Vertikal: $\\sum F_y = 0 = A_y + B_y - F \\Rightarrow A_y = F - B_y = 100\\,\\mathrm{N}$  
- Horizontal: keine äußeren $\\Rightarrow A_x = 0$  
- Festlager-Moment $M_A = 0$ (hier keine Exzenterlasten) → bei reiner vertikaler Last in der Mitte und Stütze rechts ergibt sich kein zusätzliches Einspannmoment.

> Hinweis: Je nach Lagerung/Modellierung kann $M_A$ ungleich 0 sein (z. B. nur ein Einzellager ohne Gegenstütze). Skizze präzise halten!

## Übungen
1) **Einzellast exzentrisch:** Wie oben, aber $F=150\\,\\mathrm{N}$ bei $x=0{,}5\\,\\mathrm{m}$ (von A aus). Bestimme $A_y, B_y$.  
2) **Zwei Lasten:** $F_1=80\\,\\mathrm{N}$ bei $x=0{,}6\\,\\mathrm{m}$, $F_2=120\\,\\mathrm{N}$ bei $x=1{,}6\\,\\mathrm{m}$. Reaktionen?  
3) **Momentenwaage:** Punktlast $F=40\\,\\mathrm{N}$ bei $x=0{,}3\\,\\mathrm{m}$, welcher $B_y$ ist nötig, damit $A_y=0$?

## Hinweise
- Einheiten konsequent angeben (N, m, N·m).  
- Rundungsregeln (signifikante Stellen) beachten.  
- Saubere Skizze = halbe Miete.
