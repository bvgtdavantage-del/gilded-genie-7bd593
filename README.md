# Constant Private — Landing Page

[![Netlify Status](https://api.netlify.com/api/v1/badges/dbd3dcad-97f0-4b6b-a41e-e3c8b5532bd8/deploy-status)](https://app.netlify.com/projects/benableaicom/deploys)

A single-page marketing site for Constant Private, a Dubai-based family office focused on distressed and off-market real estate, hospitality assets, and private capital across the UAE and Gulf.

## Tech

Plain static HTML, CSS, and vanilla JavaScript — no build step, no framework, no dependencies. Fonts (Fraunces, Cormorant Garamond, Manrope, JetBrains Mono) are loaded from Google Fonts. A small `IntersectionObserver` script drives the on-scroll fade-in animations.

## Structure

- `index.html` — the entire site (markup, styles, and script in one file)
- `academy/` — the benable ai academy training app, served at `/academy`
- `netlify.toml` — publishes the project root as the site

## Running locally

No build tools are required. Either:

- Open `index.html` directly in a browser, or
- Serve it locally with the Netlify CLI: `netlify dev --port 8889`, then visit `http://localhost:8889`
