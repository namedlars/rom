# Rom-Reiseplan – Deployment

Statische Single-Page (eine `index.html`, alles inline). Keine Build-Schritte nötig.

## Warum es vorher nicht ging
Vercel zeigt auf der Root-URL (`https://dein-projekt.vercel.app/`) standardmäßig die Datei **`index.html`**.
Die Datei hieß vorher `rom-reiseplan.html` → die Startseite war leer / 404.
Deshalb liegt sie hier als **`index.html`**.

## Variante A — Drag & Drop (am einfachsten)
1. Diesen **Ordner** (nicht die einzelne Datei) entpacken.
2. Auf https://vercel.com einloggen → **Add New… → Project**.
3. Den Ordner `rom-dashboard` ins Fenster ziehen (oder „Deploy" → Ordner auswählen).
4. **Deploy** klicken. Nach ~10 Sek bekommst du eine Live-URL.

> Noch schneller ohne Account-Setup: https://app.netlify.com/drop — Ordner reinziehen, fertig.

## Variante B — Vercel CLI
```bash
npm i -g vercel
cd rom-dashboard
vercel        # einmal einloggen, Fragen mit Enter bestätigen
vercel --prod # finale Live-URL
```

## Inhalt
- `index.html` – das komplette Dashboard (Live-Timeline, Karten-Routen, Buchungslinks, mobil-optimiert)
- `vercel.json` – kleine Konfig (saubere URLs)

## Hinweis
Die Live-„Jetzt"-Anzeige nutzt die Echtzeit des Geräts und rechnet auf Rom-Zeit um —
funktioniert automatisch, sobald die Seite online (oder lokal) geöffnet ist.
