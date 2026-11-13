# Lunar Indicator

Browser-only app (plain HTML + JavaScript). No Node.js, no backend, no build step.

## Run locally
Open `index.html` in any browser.

## Publish on GitHub Pages
1. Upload `index.html`, `.nojekyll`, `README.md` to a repo.
2. Settings -> Pages -> Deploy from a branch -> `main` / `(root)`.
3. Site: `https://<username>.github.io/<repo>/`

## Live NASA cross-check (Predict & Explore)
After you evaluate a site the page asks NASA from your browser:
- LOLA elevation + terrain view: NASA Moon Trek
- Sun and Earth elevation (midpoint + share above 1.5 deg): JPL Horizons, compared with the built-in model

JPL Horizons sends no CORS headers, so browsers block direct calls. The page tries direct first, then public
relays (corsproxy.io, allorigins, codetabs). Relays are third-party services and can be slow or down.
If everything fails the card says so and gives a link to run the Horizons query yourself.
