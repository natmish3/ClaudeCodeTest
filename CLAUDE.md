# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project

Static browser games — single `.html` files with all HTML, CSS, and JS inline. No build step, no dependencies, no package manager. Open any file directly in a browser.

## Architecture

Each game is a self-contained file:

- **`shooter.html`** — Top-down retro shooter. Canvas 800×600, `requestAnimationFrame` game loop. State machine (`MENU → PLAY → LEVEL_END → GAMEOVER/WIN`). Sprite drawing is procedural (canvas 2D rectangles/arcs, no images). Three enemy types (`grunt`, `runner`, `tank`), 5 levels with wave configs defined as arrays of enemy type strings. High score persisted via `localStorage`.

- **`tictactoe.html`** — 2-player tic-tac-toe. Pure DOM, no canvas. Score tracked in JS variables, no persistence.

## Workflow

Commit and push to `origin/main` frequently — after every meaningful change, not just at the end. This ensures work is never lost and the repo always reflects the current state.

```bash
git add <file>
git commit -m "short, descriptive message"
git push
```

Commit messages should be specific (e.g. `"Add Tank enemy type with HP bar"`, not `"update"`). Commit at logical checkpoints: after adding a feature, fixing a bug, or making a structural change.
