# Word-Hunter
# Wordhunter

A themed word puzzle game. Each puzzle gives you a set of clues — solve them by dragging word-piece tiles into the right slots.

## How it works

- Every puzzle has a **theme** (e.g. "Ocean Life") and a handful of **clues**.
- Each clue's answer is broken into 2–3 pieces (e.g. DOLPHIN → "dol" + "phin").
- All the pieces from every clue are mixed together in one shared pool at the bottom.
- Drag pieces from the pool into the empty slots above each clue.
- You won't know if a piece is right or wrong until **every slot on the board is filled** — then it checks everything at once. Correct pieces lock in place; wrong ones bounce back to the pool so you can try again.
- A timer tracks how long you take, and a streak counter tracks daily play.

## Files in this project

| File | What it is |
|---|---|
| `wordhunter-demo.html` | The game itself. Open it in a browser to play. |
| `puzzle-generator.html` | A tool for creating new puzzles — pulls words for a theme, checks they're real, writes clues, and splits them into pieces. |
| `OceanLife.json` | A sample puzzle you can load into the game. |
| `Architecture.json` | A sample puzzle you can load into the game. |
| `Coffee.json` | A sample puzzle you can load into the game. |
| `Music.json` | A sample puzzle you can load into the game. |
| `OSpace.json` | A sample puzzle you can load into the game. |
| `wordgame-architecture.md` | The full plan for turning this into a real app (accounts, daily puzzle, leaderboard, versus mode). |

## Running the game

1. Put `wordhunter-demo.html` and a puzzle JSON file (like `OceanLife.json`) in the same folder.
2. Don't just double-click the HTML file — browsers block it from loading the JSON that way.
3. Instead, run a local server from that folder:
   ```
   python3 -m http.server
   ```
4. Open `http://localhost:8000/wordhunter-demo.html` in your browser.

## Making new puzzles

1. Open `puzzle-generator.html` in a browser (same local-server rule applies).
2. Type in a theme and click **Discover words**.
3. Review the suggested clues and word pieces — edit anything that looks off.
4. Select the words you want, click **Build puzzle**, and download the JSON.
5. Drop that file next to the game to play it.

## Current status

This is an early prototype. It works fully in the browser with no backend — nothing is saved between sessions yet. Accounts, a real daily puzzle, leaderboards, and versus mode are planned but not built (see `wordgame-architecture.md` for the full roadmap). 
