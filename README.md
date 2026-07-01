# Karter Riggs — Portfolio

A single-page nature-themed portfolio site. No build step — it's plain static files.

## Files
- `index.html` — the whole site (markup + logic live inside the `<x-dc>` tag)
- `support.js` — the runtime that renders the page (loads React from a CDN at runtime)
- `image-slot.js` — drag-and-drop image component
- `logo.png` — pine-badge logo (nav + footer)
- `painted-meadow.png` — hero background image

## Deploy to GitHub Pages
1. Create a new GitHub repo (e.g. `karter-portfolio`).
2. Upload **all files in this folder** to the repo root (keep them side by side — the paths are relative).
3. In the repo: **Settings → Pages → Build and deployment → Source: "Deploy from a branch"**, branch `main`, folder `/ (root)`, then **Save**.
4. Wait ~1 minute. Your site will be live at `https://<your-username>.github.io/<repo-name>/`.

> Requires an internet connection when viewed — the runtime fetches React from a CDN. GitHub Pages is online, so this is fine.

## Editing with Claude Code
Open the repo folder in Claude Code and edit `index.html`. Everything you'll want to change lives inside the `<x-dc>` block:
- **Content** (your experience, projects, education, skills) is in the `class Component` logic near the bottom of the file, in `renderVals()`.
- **Layout & styling** is the inline-styled HTML inside `<x-dc>` above the script.
- To swap the hero image or logo, replace `painted-meadow.png` / `logo.png` (keep the same filenames), or point the `src` attributes at new files.

Tip for Claude Code: tell it "this is a Design Component — the page is defined inside the `<x-dc>` tag and rendered by `support.js`; edit the template markup and the `renderVals()` method."
