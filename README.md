# Shoalwood

A responsive, self-contained website for Shoalwood Family LLC. Plain HTML, CSS, and JavaScript; no build step, package installation, tracking, or external font/image requests.

## Preview

From this directory:

```sh
python3 -m http.server 4173 --bind 127.0.0.1
```

Open http://127.0.0.1:4173. You can also open `index.html` directly.

## Customize before publication

- **Contact:** `contact@shoalwoodpartners.com` is connected through a standard email link. To change it, update `site-config.js` and the two fallback links in `index.html` (so contact also works without JavaScript). No submissions are collected.
- **Copy:** the positioning and principles in `index.html` are proposed brand copy for review. No assets under management, performance, named team, portfolio, or specific asset classes have been invented. Confirm the legal name, philosophy, and wording before launch.
- **Brand:** colors and typography are defined at the top of `styles.css`. The pine-and-water SVG mark is extracted from the supplied logo concept sheet; the original sheet is preserved in `assets/shoalwood-brand-original.svg`.
- **Hosting:** all paths are relative, including the favicon, so the site supports both a root domain and a GitHub Pages repository subpath. Once the final domain is known, add its canonical URL and absolute social image metadata to `index.html` if desired.

## Repository and deployment

Source repository: https://github.com/parksandrec03/shoalwoodpartners

The website files live at the repository root. There is no build step. Uploading source does not publish the website.

For GitHub Pages, choose **GitHub Actions** under the repository's **Settings → Pages → Build and deployment**. The included workflow deploys only when manually run from **Actions → Deploy Shoalwood to GitHub Pages → Run workflow**. Select `main` for the deployment. Other static hosts can serve `index.html`, `styles.css`, `script.js`, `site-config.js`, and the three deployed assets directly.

## Files

- `index.html`: page structure and proposed copy
- `styles.css`: responsive layout, brand styling, reduced-motion support
- `script.js`: accessible mobile navigation and configurable contact email
- `site-config.js`: public contact configuration (never place secrets here)
- `assets/`: local brand and landscape assets
- `.github/workflows/pages.yml`: optional GitHub Pages deployment
- `ASSETS.md`: asset provenance and image-generation prompt

The layout includes keyboard-accessible navigation, native disclosure panels, visible focus styles, a skip link, and small-screen layouts. No contact backend or investor portal is implied.

## Validation

Reviewed in Chrome at desktop, 768 px tablet, and 390 px and 320 px phone widths. Confirmed mobile menu opening, Escape dismissal, closing after navigation, native disclosure expansion, contact destinations, and no horizontal overflow at the tested phone/tablet widths. No browser warnings or errors were observed during interaction checks. Local assets and section anchors pass a static link check. Hosting deployment has not been run.
