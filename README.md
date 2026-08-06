# Constant Private — Landing Page

A single-page marketing site for Constant Private, a Dubai-based family office focused on distressed and off-market real estate, hospitality assets, and private capital across the UAE and Gulf.

## Tech

Plain static HTML, CSS, and vanilla JavaScript — no build step, no framework, no dependencies. Fonts (Fraunces, Cormorant Garamond, Manrope, JetBrains Mono) are loaded from Google Fonts. A small `IntersectionObserver` script drives the on-scroll fade-in animations.

## Structure

- `index.html` — the entire site (markup, styles, and script in one file)
- `netlify.toml` — publishes the project root as the site

## Running locally

No build tools are required. Either:

- Open `index.html` directly in a browser, or
- Serve it locally with the Netlify CLI: `netlify dev --port 8889`, then visit `http://localhost:8889`
