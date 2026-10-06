# CoffeeConnects

Coming-soon page using static HTML and compiled Tailwind CSS. Contact and location are taken from the supplied CoffeeConnects BRD. No launch date is asserted.

## Local development

Run `npm ci`, then `npm run build`. Serve `site/` using any static HTTP server. Edit `site/index.html` and `src/styles.css`.

## Publishing

Push to `main` to run `.github/workflows/pages.yml`. The workflow builds Tailwind and uploads only `site/`. GitHub repository Settings → Pages should use **GitHub Actions** if automatic enablement is unavailable.

Fonts: Bricolage Grotesque and Manrope, self-hosted under their SIL Open Font Licenses. The cup symbol is an original geometric icon; the wordmark is typeset, not a supplied brand logo.
