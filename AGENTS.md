# AGENTS.md

## Project

A one-page marketing/landing site for Constant Private, a Dubai family office. Static HTML/CSS/JS, deployed on Netlify with no build step.

## Architecture

Everything lives in `index.html`: markup, `<style>` block, and a small inline `<script>`. There is no bundler, no framework, and no package.json. `netlify.toml` sets `publish = "."` so Netlify serves the repo root as-is.

## Conventions

- CSS custom properties for the palette are defined once under `:root` (`--navy`, `--gold`, `--ivory`, `--slate`, etc.) — reuse these variables rather than hardcoding new colors.
- Typography pairs a serif display face (Fraunces) and an italic accent face (Cormorant Garamond) with a sans body face (Manrope) and a monospace label face (JetBrains Mono). Keep this pairing when adding sections.
- Scroll-in animations use the `.fade` class combined with the `IntersectionObserver` at the bottom of the file; add `.fade` to new elements that should animate in, don't write new observer logic.
- The site respects `prefers-reduced-motion` — any new animation should be covered by that media query too.
- No JavaScript framework, build tooling, or client-side routing has been introduced; keep additions dependency-free unless there's a concrete need (e.g., a real contact form) that would justify pulling in Netlify Forms or a function.

## Non-obvious decisions

- Contact is a `mailto:` link, not a form — there was no requirement for stored submissions, so no Netlify Forms setup or database was added. If a real contact form with stored/emailed submissions is needed later, add a `<form netlify>` per the Netlify Forms skill rather than wiring up a custom backend.
