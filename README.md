# Harbor website

The public website for [Harbor](https://github.com/estuty/HARBOR), the self-hosted hosting control panel.
A static site with no build step: plain HTML, CSS, a little JavaScript and images.

| File | What |
|---|---|
| `index.html` | Home page: product screens, features, cPanel map, how it works, technical details |
| `docs.html` | Documentation, generated from the Harbor app's `README.md` |
| `styles.css`, `site.js` | Shared styles (light and dark) and the script for the menu, screen tabs and contour background |
| `assets/screens/` | Screenshots of the real panel (light and dark), WebP |
| `assets/fonts/` | Schibsted Grotesk, Public Sans, JetBrains Mono (latin, variable), SIL OFL 1.1, see `OFL.txt` |
| `assets/og.png` | Social preview image, rendered from `og-source.html` at 1200×630 |
| `favicon.svg` | The panel's anchor mark |

## Preview

```bash
python3 -m http.server 8000    # then open http://localhost:8000
```

## Publish

Any static host. Cloudflare Pages or Netlify: connect this repository, no build command, output directory `/`
(the repository root). Every push to `main` then updates the live site.

## Keep it current

- Documentation: with the app cloned next to this repository (`../HARBOR`), run
  `pip install markdown && python3 build_docs.py`.
- New screenshots: capture the panel at 1440×900 (2× pixel density), save as WebP at 1600 px wide
  (1920 for the dashboard), as `name-light.webp` and `name-dark.webp` in `assets/screens/`.
- Screens come from a test server with example domains.
