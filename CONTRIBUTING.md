## Contributing to REAKTOR 404

Thanks for your interest in improving **REAKTOR 404 — Cleaners Run**.

### How to propose changes

- **Issues**: If you’ve found a bug or have a feature idea, open a GitHub issue with:
  - A clear description of the problem or enhancement.
  - Steps to reproduce (for bugs) and your browser/OS if relevant.
  - Screenshots or short clips are very helpful for gameplay / UX issues.

- **Pull requests**:
  - Fork the repo and create a feature branch from `main`.
  - Keep changes focused and cohesive (one feature or fix per PR when possible).
  - Update or add inline comments only where intent is non‑obvious (avoid narrating code).
  - Test in at least one desktop browser; if your change affects touch, test on a phone or simulator as well.

### Code style and structure

- The project is currently a **single‑file HTML5 game**:
  - `index.html` contains the markup, styles, and JavaScript.
  - JavaScript is written in modern, framework‑free ES6+.
  - CSS favors utility‑style, component‑scoped classes over global resets.
- Match existing patterns:
  - Prefer small, single‑purpose helper functions over deeply nested logic.
  - Keep naming descriptive (`audio`, `mapModal`, `RADIO_LEVELS`, etc.).
  - Avoid introducing heavy dependencies or build systems unless there’s a clear payoff.

If you intend a larger refactor (e.g. extracting `style.css` and `game.js`, or introducing a bundler), please open an issue first so direction and scope can be agreed on.

### Performance and UX

- Aim to keep the game:
  - **Responsive** on both desktop and mobile.
  - **Fast to load** (minimize asset size and network requests).
  - **Keyboard and touch friendly**.
- Changes that might affect difficulty (enemy AI, maze generation, power‑up balance) should mention the intended effect on game feel in the PR description.

