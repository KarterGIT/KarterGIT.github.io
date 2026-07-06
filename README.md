# Karter Riggs — Portfolio

A single-page, nature-themed portfolio site. Plain static HTML/CSS/JS — no build step, no runtime, no dependencies.

🌐 **Live:** https://kartergit.github.io

## Files
- `index.html` — the entire site (markup, inline styles, and a small vanilla-JS script)
- `logo.png` — pine-badge logo (nav, about panel, footer)
- `painted-meadow.png` — hero background image

## Editing
Everything lives in `index.html`:
- **Content** (experience, education, projects, skills) is the markup inside each `<section>`.
- **Styling** is inline on the elements, plus a small `<style>` block in `<head>` for hover states, the scroll-reveal animation, and responsive stacking.
- **Behavior** (sticky-nav shading + reveal-on-scroll) is the vanilla-JS `<script>` at the bottom.
- To swap the hero image or logo, replace `painted-meadow.png` / `logo.png` (keep the same filenames).

## Hosting
Served by GitHub Pages from the `main` branch. Push to `main` and it redeploys automatically.
