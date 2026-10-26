HACK THE SYSTEM — Static Edition

A fully static, single-player logic puzzle game. It runs from `index.html` by double-clicking it or can be hosted on GitHub Pages. No Python, server, API, build step, or external network request is required.

## Run locally

Open `index.html` in a modern browser. JavaScript must be enabled.

## Publish with GitHub Pages

1. Create a GitHub repository and upload `index.html` plus the `static/` folder to the repository root.
2. Open **Settings → Pages**.
3. Under **Build and deployment**, select **Deploy from a branch**, choose your default branch and `/(root)`, then save.
4. Wait for the Pages deployment and open the URL GitHub provides.

## Game rules

- Clear 10 puzzles in order before the 10-minute timer expires.
- Correct answer: +100 credits.
- Incorrect answer: -10 credits, never below zero; streak resets.
- First hint on a level costs 25 credits.
- Victory time bonus: one point per five seconds remaining.
- Best score is saved in the current browser using `localStorage`.

## Static-site trade-off

Answer validation, hints, explanations, puzzle data, and scoring run in the browser. Anyone can inspect the JavaScript source and find the solutions. This is appropriate for a casual single-player puzzle, but it is not suitable for secret answers, secure leaderboards, or tamper-proof scoring. High scores are local to each browser and can be edited by the player.

## Files

- `index.html` — page markup
- `static/css/style.css` — styling
- `static/js/game-logic.js` — scoring, timer, progression
- `static/js/levels.js` — puzzle data, local validation, hints, explanations, visuals
- `static/js/game.js` — user interface and event handling
