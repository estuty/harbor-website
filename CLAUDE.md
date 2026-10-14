# Harbor website

Static marketing site for the Harbor control panel (the app lives in a separate repository,
https://github.com/estuty/HARBOR). No framework and no build step; keep it that way.

- `index.html` (home), `docs.html` (generated, don't edit by hand: run `python3 build_docs.py [path/to/HARBOR/README.md]`).
- `styles.css`: design tokens at the top (`--night` navy bands, `--paper` light pages, `--tide` teal accent, same as the panel).
  Light and dark themes via `prefers-color-scheme` plus `data-theme`. Fonts are self-hosted in `assets/fonts/`.
- `site.js`: mobile menu, accessible screen tabs (arrow keys), and the depth-contour canvas behind navy bands.
- Only state what Harbor actually does; check claims against the app's README or code. Screens must be real captures.
- Check changes at 1440, 820 and 390 px wide: no horizontal scrolling, links and anchors resolve.

Preview: `python3 -m http.server 8000`.
