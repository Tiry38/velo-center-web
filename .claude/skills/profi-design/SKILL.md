---
name: profi-design
description: Pflicht vor JEDER visuellen Arbeit für Tiry/Velocenter – Schilder, Aushänge, Druck-Einlagen, Flyer, Social-Grafiken, Mockups, Vorher-nachher-Bilder, Raum-/Wand-Visualisierungen, Präsentationen. Legt fest, wie eine Top-Agentur denkt und liefert: echte Marken-Assets, echte Maße, Druck-Sicherheit, fotorealistische Visualisierung statt Clip-Art und ein hartes Qualitäts-Gate vor dem Senden.
---

# Profi-Design – so wird für Tiry gestaltet

Maßstab: **Würde eine gute Agentur das genau so beim Kunden abgeben?** Wenn nein, wird es nicht geschickt.
Tiry merkt sofort, wenn etwas billig, generisch oder halbfertig ist. Jede schwache Lieferung kostet Vertrauen.

## Fehler, die schon passiert sind (nie wieder)

| Fehler | Richtig |
|---|---|
| Generisches Template mit Fantasie-Farben und selbstgemalten Icons (Schild Rückwärtsgang, 1. Fassung) | Erst Marken-Assets holen: `DESIGN.md` (Herbstallee + Nebel-Glas), Logo, Homepage-Fotos, Schriften |
| Format gedreht, Maß vom Etikett blind übernommen (Zahlteller: 160×140 quer statt hochkant, echte Breite ~133 mm) | Ausrichtung und Innenmaß vor dem Layout klären, Foto mit Referenzmaß nachrechnen |
| Text mit `background-clip:text` → im Druck komplett verschwunden | Druck-Texte nur in Vollfarbe, PDF vor dem Senden rastern und ansehen |
| Wand-„Mockups“ aus CSS-Kästen, aufgemalten Rillen, Icon-Steckdosen, Schatten-Flecken | Fotorealistisch (KI-Bildbearbeitung mit dem echten Foto) oder echte Referenzfotos – nie Clip-Art für reale Dinge |
| Zierlinien laufen durch Text | Nichts kreuzt Text. Nie. |
| Links aus der Websuche ungeprüft geschickt, einer tot (404), bei Tiry ging keiner auf (Spacewall-Beispiele) | Keine Links als Lieferung. Inhalt als Screenshot/Datei per `SendUserFile`. Ein Link nur zusätzlich und nur nach `curl -L` = 200 **und** geprüftem Seitentitel |

## Ablauf (immer in dieser Reihenfolge)

1. **Auftrag verstehen:** Wofür, wo hängt/liegt es, wer sieht es, aus welcher Entfernung? Was soll der Betrachter tun?
2. **Echte Fakten:** Maße (Innenmaß, Ausrichtung), Material, Druckweg (Laser A4? Druckerei?). Unklar → aus Foto mit Referenz rechnen und Unsicherheit offen sagen, oder Tiry nach **einer** Zahl fragen.
3. **Marken-Assets holen, nie erfinden:**
   - **Design = `DESIGN.md` im Repo-Wurzelordner (gleich in KI-Zentrale, Planer, Homepage). Zuerst lesen.** Herbstallee-Foto als Hintergrund, helles Nebel-Glas (Weiß 58/50 %), Rot `#C8102E` als Akzent, Kupfer `#B87333`, Kopf von Vorlagen ohne roten Keil.
   - **Altes Design nie verwenden:** Eis-Himmel, gebürsteter roter Keil, 115°-Striche, Goldring, dunkles Design, Schwarz-Weiß-Grau.
   - Logo: `velo-center-web/img/velocenter-logo.svg`, Markenlogos `img/marke-*.svg`, Herbstallee `img/hg12/herbst-2400.webp`, Produktfotos `img/p-*.webp`, `img/show/*.webp`.
   - Schriften: Outfit (Headlines 800–900), Sora (Text), aus `velo-center-web/fonts/`.
4. **Layout:** klare Hierarchie (1 Hauptaussage, 1 Nebenaussage, Absender). Raster, gleiche Ränder, Sicherheitsabstand ≥ 8 mm zum Schnitt. Text nie über unruhigem Grund. Echte Fotos statt Icons, wo es um reale Dinge geht.
5. **Visualisierung realer Räume/Objekte** (Wand, Laden, Einbau):
   - **Erste Wahl:** KI-Bildbearbeitung mit dem echten Foto als Referenz (Canva `generate-image` mit `imageReferences`, Foto vorher hochladen). Perspektive, Licht und Schatten bleiben echt.
   - **Zweite Wahl:** echte Referenzfotos von Herstellern/Händlern als Links zeigen.
   - **Nie:** CSS/SVG-Nachbauten von Steckdosen, Paneelen, Möbeln. Das sieht immer billig aus.
   - Immer sagen, dass es eine Visualisierung ist, und welche Annahmen drin stecken.
6. **Druck-Sicherheit:** nur Vollfarben für Text, keine Blend-/Clip-Effekte, Schnittmarken, „Tatsächliche Größe“ im Hinweis, PDF mit `pdftoppm` rastern und **ansehen**, bevor es rausgeht.
7. **Qualitäts-Gate (Pflicht vor jedem Senden):** Screenshot in voller Größe ansehen und jeden Punkt abhaken:
   - [ ] Sieht aus wie Agentur-Arbeit, nicht wie Vorlage oder Baukasten
   - [ ] Marke sofort erkennbar (Herbstallee + Nebel-Glas laut `DESIGN.md`, Logo, Farben exakt)
   - [ ] Maße und Ausrichtung stimmen mit dem echten Objekt
   - [ ] Nichts kreuzt Text, nichts angeschnitten, keine Lücken/Streifen am Rand
   - [ ] Hierarchie klar, aus 2–3 m lesbar (bei Aushängen)
   - [ ] Reale Dinge fotorealistisch oder als echtes Foto
   - [ ] Gedrucktes PDF gerastert und geprüft
   - [ ] Jeder Link einzeln aufgerufen (Status 200, richtiger Inhalt) – besser: Inhalt als Bild/Datei statt Link
   - Fällt ein Punkt durch: selbst verbessern, nicht schicken. Mindestens eine eigene Verbesserungsrunde.
8. **Ehrlichkeit:** Wenn das Werkzeug keine Profi-Qualität schafft, das sagen und den richtigen Weg nennen. Lieber eine Lieferung weniger als eine schlechte.

## Lieferung an Tiry

- Kurz: was es ist, Maß/Format, wie drucken, was geprüft werden muss (offene Annahmen).
- Dateien per `SendUserFile`: Druck-PDF + PNG-Vorschau.
- Ton nach CLAUDE.md: direkt, ohne Floskeln, Fettdruck für Kernbotschaften.
