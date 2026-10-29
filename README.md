# MazaoCheck

A free, single-page web tool that shows Kenyan farmers the official government reference price for a crop next to the typical broker price — closing the **Price Truth Gap** so a fair price can fund healthier soil, animals, and families.

**Live:** https://geraldkombo.github.io/mazaocheck/

## Features
- 29 crops & animal products, including 9 indigenous varieties (managu, terere, kunde, mrenda, saga, ndengu, cassava, arrow roots, sweet potatoes)
- Red broker price vs green government price, with the loss in KES and %
- Agroecology tip and One Health line per crop
- Bilingual (English + Swahili), works on any phone, no install
- Farmer price reports across all 47 counties (stored on-device), with CSV export
- Optional Supabase sync for multi-device report pooling (unconfigured by default)

## Price data & sourcing
- **Government prices:** official references from KNBS Statistical Releases and AFA market bulletins.
- **Broker prices:** farmer-reported field quotes, growing as more farmers report. No fabricated numbers.
- **As of:** 29 October 2026 — shown in the app header and under the price grid, driven by `PRICES.lastUpdated`. Categories without a newer official release retain their June 2026 values.
- All prices are hardcoded in the `PRICES` constant in `index.html`. To refresh: edit the values there and bump `lastUpdated`.

## Run / edit
No build step, no dependencies. Open `index.html` in a browser, or serve the folder:

```bash
python3 -m http.server 8000
```

Deployed via GitHub Pages from the `main` branch (root directory).

## Files
- `index.html` — the entire web app (single file: markup, styles, logic, price data)
- `assets/logo.svg` — project logo
- `assets/share-card.svg` — social share image (`og:image`)
- `LICENSE` — MIT license
- `.github/workflows/ci.yml` — CI check: `index.html` exists and every file referenced from `index.html` / `README.md` exists

## Background
Built for the 3rd Kenya National Agroecology Symposium — Call for Innovations: Scaling Agroecological Solutions for One Health Approach. Aligned with Kenya's National Agroecology Strategy (2024–2033). Built independently by Gerald Kombo, Nairobi.

## License
MIT © 2026 Gerald Kombo — see [LICENSE](LICENSE).
