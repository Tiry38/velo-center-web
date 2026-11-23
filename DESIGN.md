# Velocenter-Design – verbindlich (Stand 23.11.2026)

**Diese Datei ist in allen drei Repos gleich:** `velocenter-ki-zentrale`, `Velocenter-Planer`, `velo-center-web`.
Wer „Velocenter-Design“, „unser Design“ oder „Design wie Homepage/Planer/Zentrale“ hört, nimmt **genau das hier**.
Ändert sich das Design, wird diese Datei in **allen drei** Repos gleich angepasst.

## 0. Das gilt NICHT mehr (altes Design bis 21.11.2026)

Nie wieder verwenden, auch wenn ältere Notizen in CLAUDE.md, VERLAUF.md oder Skills das noch beschreiben:

- Eis-Himmel-Verlauf als Hintergrund
- gebürsteter roter Metall-Keil oben rechts (`erx.png`, `--hp-metal`, `body::after`-Keil), weißes Chrom-Band
- graue/rote 115°-Striche, Riffelmuster `--hp-riff`, 45°-Kreuzmuster
- graue Navi, Goldring/Kupfer-Kringel am aktiven Reiter, rote Pille
- dunkles Design (Schwarz, Violett-Verläufe, roter Rauch `mail-smoke.png`, `app-smoke.webp`)
- Schwarz-Weiß-Grau

„Design A“ in alten Einträgen = dieses alte Design. **Aktuell ist „Herbstallee + Nebel-Glas“.**

## 1. Grundidee

**Echte Herbstallee (Foto) als Hintergrund, darüber helles Nebel-Glas.** Der Wald scheint überall dezent durch.
Hell, ruhig, hochwertig. Rot nur als Akzent (Logo, Titel, Hauptknöpfe).

## 2. Hintergrund „Herbstallee“

| Wo | Wie |
|---|---|
| Homepage, Planer, KI-Zentrale (Bildschirm) | WebGL-Ebene `#hg`, Shader „hg12“ aus `velo-center-web`: Laub fällt in 3D, Maus = Wind, Lichtstrahlen aus dem Nebel. Klassen: `html.hg3` = WebGL läuft, `html.hgS` = Rückfall stehendes Foto. |
| Leistungsmodus / „Animationen aus“ | dasselbe Bild **stehend** (keine eigene Grafik) |
| PDFs, Druck, Tablet, E-Mails, Checkliste, Wallpaper | **stehendes Foto** der Herbstallee, keine Blätter |

Bilddateien (nie neu erfinden, nie Stockfoto):
- Homepage: `img/hg12/herbst-2400.webp`, `herbst-1400.webp`, Tiefe `herbst-d.png`, Maske `herbst-m.png`
- Planer: `hg-herbst.webp`, `hg-herbst-d.png`, `hg-herbst-m.png` (Wurzelordner)
- KI-Zentrale: `app/bilder.json` b67 Foto, b68 Tiefe, b69 Maske, b70/b71 Mail-Kopf/-Fuß (Foto + Logo / Straße), b72 `hg-papier.jpg` (A4-Hintergrund), Tablet `app/hg-tablet-hoch.jpg` / `app/hg-tablet-quer.jpg`

Regeln: kein `background-attachment:fixed`, kein `backdrop-filter` (Leistung am Mini-PC). Bild nie feiner rechnen als die Foto-Auflösung.

## 3. Flächen = Nebel-Glas

- Tafeln, Karten, Listen, Kopfkästen: **Weiß 58 %** (`rgba(255,255,255,.58)`), zweite Ebene **50 %**
- innen liegende Teile: Weiß 30 %
- Eingabefelder, Suchfelder, helle Knöpfe: Weiß 55 %, Rand Weiß 90 %
- keine Riffel, keine Streifen, keine harten Schatten
- Vorlagen (PDF/Tablet/Druck): weiße Karten (Tablet 97 % deckend) mit **Kupfer-Strich #B87333**

## 4. Navi = Nebelschleier

Links dichter, nach rechts weich auslaufend, ohne Kante und Schatten, Wald läuft durch:

```css
background:radial-gradient(140% 22% at 0% 0%,rgba(255,255,255,.45),rgba(255,255,255,0) 70%),
 radial-gradient(120% 20% at 0% 55%,rgba(255,255,255,.22),transparent 70%),
 radial-gradient(120% 22% at 0% 100%,rgba(255,255,255,.30),transparent 70%),
 linear-gradient(90deg,rgba(241,245,250,.74) 0%,rgba(239,243,248,.62) 55%,rgba(237,241,247,.44) 86%,rgba(236,240,246,.16) 100%);
border:0;box-shadow:none;
```

Dunkle Schrift. **Aktiver Reiter = Glas-Pille mit rotem Schein**, Hover = Glasblase.

## 5. Kopf von Vorlagen (PDF, Mail, Tablet, Checkliste)

Foto deckungsgleich, **weißer Nebel links, weich nach rechts auslaufend**, Logo links. **Kein roter Keil, kein Rot im rechten Bereich** (Tiry 23.11.2026). Rote Linie unter dem Kopf. Druck = gleiches Foto-Design wie digital.

## 6. Farben

| Rolle | Wert |
|---|---|
| Hauptrot (Titel, Hauptknöpfe, Linien) | `#C8102E` (Verlauf Knopf `#C8102E → #E2232D`) |
| Logo-Rot | `#CF1A2C` |
| Kupfer (Striche, Rahmen) | `#B87333` |
| Text | `#1B1E25` |
| Grün (OK) / Blau (Info) | `#1F9765` / `#2F5BD8` |
| Nebelton außen (Mail) | `#E9E3DC` |
| Schlicht hell ohne Foto | `#F3F5F8` bzw. Verlauf `#F6F8FB → #E8EDF3 → #F1E9E9` |

## 7. Schrift und Logo

- **Outfit** für Überschriften, Zahlen, Navi (800–900 für Headlines), **Sora** für Fließtext. Dateien: `velo-center-web/fonts/outfit-latin.woff2`, `sora-latin.woff2`.
- Logo: `velo-center-web/img/velocenter-logo.svg` (KI-Zentrale `app/vendor/logo.svg`), **immer Originalfarben Rot/Grau, freigestellt**, nie auf dunkler Plakette, nie umgefärbt.
- Markenlogos: `velo-center-web/img/marke-*.svg` (KTM, Gudereit, Velo de Ville, i:SY, QiO, Van Raam, Victoria, Stevens). Auf hellem Grund im Original, auf dunklem Foto-Grund weiß.

## 8. Referenz-Umsetzungen (beim Nachbauen hier nachsehen)

- KI-Zentrale: `app/index.html` Block `<style id="designA">` (Name historisch, Inhalt = Herbstallee + Nebel), `#hg`-Skript, `app/design_a.js` (`foto()`, `kopf()` für PDFs), `app/tablet.js`, `vcMail`
- Planer: `src/theme_hp.css` (Ende: Herbstallee, Nebel-Glas, Navi-Schleier, 1.11.18–1.11.26), Shader am Ende von `src/body_fb.html`
- Homepage: `index.html` (hg12), Quellcode im Repo `Tiry38/Tiry`, Ordner `velocenter-homepage`
- Beispiel Werbegrafik: 4K-Wallpaper (23.11.2026) = Herbstallee-Foto, Lichtschein im Nebel am Fluchtpunkt, großes Logo mittig, Claim in Outfit-Versalien zwischen roten Linien, weiße Markenleiste auf dem Asphalt

## 9. Für jede neue Gestaltung

1. Diese Datei lesen. Alte Beschreibungen (Abschnitt 0) ignorieren.
2. Echte Assets aus Abschnitt 2 und 7 nehmen, nichts nachmalen.
3. Skill `profi-design` (Qualitäts-Gate) abhaken.
