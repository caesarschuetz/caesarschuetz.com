# caesarschuetz.com

Persönliche Seite. Astro, statisch, kein JavaScript im Auslieferungszustand.

## Lokal starten

```bash
npm install
npm run dev
```

Läuft dann auf http://localhost:4321

## Aufbau

```
src/
  layouts/Base.astro       Rahmen, Navigation, Footer, Schriften
  pages/index.astro        Startseite (aktuell Blanko: Name, Positionierung, Links)
  styles/global.css        Farben und Typografie
```

## Brand

| Zweck | Wert |
|---|---|
| Basis, Hintergrund | `#121110` |
| Schrift auf dunkel | `#F7F5F1` |
| Akzent | `#00A6B8` |
| Akzent als Schrift auf hell | `#076B78` |
| Schrift | Archivo 400 / 600 / 700 |
| Labels, Zahlen, Daten | JetBrains Mono 400 / 500 |

Ein Akzentelement pro Abschnitt. Kein Logo, keine Rahmen, keine Farbflächen.

## Neuen Text anlegen

Neue Datei in `src/content/writing/`, Frontmatter kopieren aus
`beispiel-post.md`. Erscheint automatisch auf `/writing/`.

## Presse-Eintrag anlegen

In `src/pages/press.astro` das Array `items` füllen:

```js
const items = [
  { date: "2026-11-02", outlet: "Name des Mediums", title: "Titel", url: "https://…" },
];
```

## Vor dem Livegang

Diese Platzhalter stehen noch in den Dateien und müssen raus:

- `index.astro`: Rolle und Status bei tecis, Zahl bei VerbraucherCheck, Abschlussdatum Studium
- `impressum.astro`: Anschrift und E-Mail, dazu die Pflichtangaben für die Vermittlertätigkeit, falls zutreffend

Die drei Angaben in `index.astro` sind dieselben, die im CV noch offen sind.
Sie müssen auf Seite, CV und Profilen identisch stehen.

Keine Formulierung, die nahelegt, dass du in den USA lebst oder arbeitest.

## Deploy

Repo auf GitHub, dann bei Vercel importieren. Astro wird automatisch erkannt,
Build `npm run build`, Output `dist`. Domain danach in den Projekteinstellungen
verbinden.
