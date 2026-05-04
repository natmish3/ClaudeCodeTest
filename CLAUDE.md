# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project

Static browser games — single `.html` files with all HTML, CSS, and JS inline. No build step, no dependencies, no package manager. Open any file directly in a browser.

## Architecture

Each game is a self-contained file:

- **`shooter.html`** — Top-down retro shooter. Canvas 800×600, `requestAnimationFrame` game loop. State machine (`MENU → PLAY → LEVEL_END → GAMEOVER/WIN`). Sprite drawing is procedural (canvas 2D rectangles/arcs, no images). Three enemy types (`grunt`, `runner`, `tank`), 5 levels with wave configs defined as arrays of enemy type strings. High score persisted via `localStorage`.

- **`tictactoe.html`** — 2-player tic-tac-toe. Pure DOM, no canvas. Score tracked in JS variables, no persistence.

## Workflow

After any change: commit with a descriptive message and push to `origin/main`.

```bash
git add <file>
git commit -m "description of change"
git push
```
