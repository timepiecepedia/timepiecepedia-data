# Timepiecepedia — Free Watch Database

> **48,658 watch references across 224 brands** — a free, open dataset of luxury and mechanical watches with full specifications, movements, materials, and imagery.

Curated by [timepiecepedia.com](https://timepiecepedia.com), the free online encyclopedia of horology. Updated automatically every few hours as new brands and references are catalogued.

_Last updated: 2026-05-14T00:10:02.453Z_

## What's inside

| File | Format | Records |
|------|--------|---------|
| `references.csv` | Flat CSV, 11 columns | 48,603 watches |
| `catalog/` | Nested JSON per brand/family | 224 brands |
| `brands.json` | Brand metadata (name, country, founded, tier, summary) | 224 brands |
| `glossary.json` | Watchmaking terminology | 1,701 terms |

## Dataset highlights

- **48,658** individual watch references catalogued
- **224** brands indexed (224 with full reference data, more being added continuously)
- **1,701** horology terms defined
- Imagery URLs, technical specs (movement, materials, diameter, water resistance), collection/family grouping
- Multilingual: English + French (386 editorial articles)

## CSV schema (`references.csv`)

```
brand, family, reference, name, movement, material, diameter_mm,
water_resistance, year_produced, image_url, url
```

## JSON schema (`catalog/<brand>/<family>.json`)

Each file contains a collection object with a `references` array:

```json
{
  "name": "Datejust 31",
  "slug": "datejust-31",
  "references": [
    {
      "slug": "178274-0043",
      "url": "/rolex/datejust-31/178274-0043",
      "title": "Rolex - Datejust 31 Stainless Steel / Pink MOP Diamond",
      "specs": {
        "Brand": "Rolex",
        "Family": "Datejust 31",
        "Reference": "178274-0043",
        "Movement": "Rolex caliber 2235",
        "Materials": "White Gold, Stainless Steel",
        "Diameter": "31.00 mm",
        "W/R": "100.00 m",
        "Glass": "Sapphire"
      },
      "image_url": "https://cdn.watchbase.com/watch/lg/..."
    }
  ]
}
```

## Use cases

- Training ML models for watch recognition / recommendation
- Building watch comparison tools, price trackers, collector apps
- Academic research in horology, design, materials
- Reference in blog posts, tutorials, YouTube videos

## License

**CC0 1.0 Universal (Public Domain Dedication)** — use commercially, remix, redistribute, no attribution required (though appreciated).

## Attribution (appreciated, not required)

If you build something cool with this, link back to [timepiecepedia.com](https://timepiecepedia.com). We'd love to see it.

## Contribute / report issues

Spotted a wrong spec or missing reference? Open an issue or PR.

## Updates

This repo is **auto-synced** with timepiecepedia.com. The scraper continuously adds new brands and references, and this dataset is regenerated and pushed every few hours. Watch/star the repo to be notified.

---

⭐ **Star this repo** if you find it useful — it helps others discover free open watch data.
