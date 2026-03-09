## REAKTOR 404 — Cleaners Run

Top‑down arcade maze game where you guide a sentient radioactive blob through a reactor complex, dodging Cleaners, collecting SEALS, grabbing IsoSparks for brief invincibility, and sprinting for the exit. Designed to run as a fast, self‑contained HTML5 canvas game on the web (including GitHub Pages).

### Features

- **Arcade loop**: Collect SEALS, avoid Cleaners, reach the EXIT to climb reactor ranks.
- **IsoSpark power‑up**: Temporary invincibility with a distinctive blue glow and cabinet flare.
- **Hand‑rolled maze generator**: Deterministic per‑level maze layout with pellets, exits, and hazards.
- **Keyboard and touch**: WASD / arrow keys on desktop, tap‑to‑move and optional joystick on touch devices.
- **Accessibility touches**: ARIA live regions for score/status, readable overlays and pause/help screens.

### Controls

- **Desktop**
  - **Movement**: `WASD` or arrow keys.
  - **Start / restart**: `Enter`, `Space`, or click/tap the **Start** button.
  - **Map**: Click **Map** in the top bar.
  - **Pause / info**: Click **Pause/Info` in the top bar.
  - **Mute**: Click the speaker icon in the top bar.

- **Touch**
  - **Start**: Tap the **Start** button.
  - **Movement**: Tap near the blob in the direction you want to move.
  - **Map / help / mute**: Use the buttons in the header.

### Running locally

This is a static site (no build step). Any static file server or direct file open works:

- **Quickest**: Double‑click `index.html` and open it directly in a modern browser.
- **With a tiny dev server** (recommended for consistent behavior across browsers):

```bash
npx serve .
# or
python -m http.server 8000
```

Then open `http://localhost:3000` or `http://localhost:8000` depending on the tool.

### Deployment

The repo is set up to work well on **GitHub Pages**:

- The HTML references assets assuming it is hosted at `/reaktor404/` (e.g. favicons, manifest).
- To deploy or update:
  - Push the latest `main` branch to GitHub.
  - Use GitHub Pages (project site) with the root set to the repo’s default branch.

If you fork this and host it under a different path, update any `/reaktor404/...` URLs in `index.html` to match your new base path.

### Project structure

- **`index.html`**: Entire game — HTML shell, CSS, and JavaScript (canvas rendering, maze generation, input, audio).
- **`robots.txt`**: Basic search engine directives pointing at the main site sitemap.
- **`.gitattributes`**: Git text normalization.
- **`.gitignore`**: Ignores local/editor/OS junk and common build artifacts.

### Development notes

- The game logic is intentionally written in vanilla JavaScript and lives inline in `index.html` for portability.
- If you want a more modular layout, a good next refactor is to extract:
  - CSS into `style.css`.
  - Game code into `game.js` (plus `audio.js` / `maze.js` if you want further separation).

### Contributing

See `CONTRIBUTING.md` for contribution guidelines, issue/PR expectations, and code style notes.

