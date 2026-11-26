# Populate the Stars – Promo-Seite

Statische Seite zum Spiel ([../sol](../sol)). Kein Build, keine Cookies, kein Tracking. CSS, JavaScript und Schrift stehen inline im HTML, separat liegen nur Bilder.

Live: <https://www.populate-the-stars.com/> – Deploy per GitHub Actions bei jedem Push auf `main` ([deploy.yml](.github/workflows/deploy.yml)).

| Datei | Inhalt |
| --- | --- |
| `index.html` | Promo-Seite |
| `legal.html` | Impressum + Datenschutz, `?lang=de` · `en` · `fr` · `es` · `pt` · `pt-BR` (sonst Browsersprache) |
| `assets/` | Icon, App-Store-Badge, `og-image.jpg` (1200 × 630, Vorschau für Social Media) |
| `screenshots/` | Originale für die Lightbox (aus `sol/screenshots/out-iphone/en`, 6,3″, verkleinert auf 1080 × 2348), `small/` Vorschauen: `sips --resampleWidth 400 -s format jpeg -s formatOptions 82 01-solar-system.jpg --out small/01-solar-system.jpg` |

## Generierte Teile

Aus dem Spiel erzeugt, nicht von Hand ändern. Im Spiel-Ordner:

```sh
npm run export:legal   # Rechtstexte → legal.html (legal-texts:begin/end)
```
