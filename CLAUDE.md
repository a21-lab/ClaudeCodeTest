# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project

Single-file web game (`tictactoe.html`) — all HTML, CSS, and JavaScript lives in one file with no build step, dependencies, or package manager.

## Running the project

Open `tictactoe.html` directly in a browser:

```bash
open tictactoe.html
```

## Architecture

Everything is in `tictactoe.html`:

- **Game state** — `board` (9-element array), `current` (active player), `gameOver`, `mode` (`pvp` or `pvc`)
- **AI** — minimax in `minimax()` / `bestMove()`; called with a 250ms delay after the human move so it feels responsive
- **Rendering** — direct DOM manipulation on `.cell` elements; win cells get the `.win` class for animation
- **Scores** — tracked in the `scores` object (`{ X, O, D }`) and written to the scoreboard on each game end

## Git workflow

Commit and push to `origin/main` (https://github.com/a21-lab/ClaudeCodeTest) after every meaningful change.
