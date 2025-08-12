# Pocket Realm (PWA)
A tiny, iPad-friendly web game inspired by classic castle-management vibes. Runs as a Progressive Web App (PWA): installable, offline-capable, and touch-first.

## Quick Start (GitHub Pages)
1. Create a new repo on GitHub (public is fine).
2. Upload **all** files from this folder (keep `index.html`, `manifest.webmanifest`, `sw.js`, and `icons/` at the repo root).
3. In **Settings → Pages**, set:
   - **Source:** Deploy from a branch
   - **Branch:** `main` (or `master`) / **Root**
4. Wait for the green checkmark. Your game will be available at:
   - `https://<your-user>.github.io/<your-repo>/`
5. Open the URL in Safari on iPad → Share → **Add to Home Screen**.

### Updating
- After changes, push/commit again. The service worker caches files; open the site once in Safari to refresh. If you changed game files and Safari still shows an old version, bump `CACHE_NAME` in `sw.js` (e.g., `pocket-realm-v2`) and reload once.

### Making More Games
- Use this repo as a template (**Settings → General → Template repository**) or click **Use this template** when creating a new project.
- Keep the same structure. Only `index.html` + assets change.
- `manifest.webmanifest` uses relative paths and `start_url: "."` so it works under the GitHub Pages subpath.

## Files
- `index.html` – game & UI (all inline CSS/JS)
- `manifest.webmanifest` – PWA metadata & app icons
- `sw.js` – service worker for offline caching
- `icons/` – PNG icons referenced by manifest
- `.nojekyll` – disables Jekyll on GitHub Pages so files/folders starting with `_` (not used here) would still serve
- `LICENSE` – MIT

## License
MIT © 2025 Your Name
