# Midnight Hide & Seek

A 2.5D single-player hide-and-seek game (Among Us-style characters, top-down with
depth-sorted walls). Built as one self-contained HTML file — no install, no dependencies.

## Play

- Double-click **play.bat**, or just open **index.html** in a browser.
- Or serve it: `python -m http.server 8010` from this folder, then open http://127.0.0.1:8010

## Controls

| Key | Action |
| --- | --- |
| WASD / Arrows | Move |
| Shift | Dash (dodge, brief invulnerability) |
| E | Hide in a locker / take a vent |
| Ctrl (hold) | Sneak — quieter, harder to spot |
| Left mouse | Shoot (if ammo) / katana slash (if empty) |
| Right mouse | Parry (katana) — negates a hit and stuns the seeker |
| R | Reload |
| Esc | Pause |

## Goal

Survive **120 seconds**. The seeker patrols, hears gunshots, chases you, and searches
lockers. You can down it with lead or steel — it respawns after 8 seconds.

## Mechanics

- **Lockers** — press E to hide. The seeker can still search one if it lingers beside it.
- **Vents** — press E to instantly jump to the next vent in the network (5 uses of chain).
- **Parry** — right-click inside the wind-up ring; a successful parry stuns the seeker ~3s.
- **Dash** — dodges through a strike and gives i-frames.
- **Ammo boxes** — walk over them for +4 ammo (respawn in 20s).
- **Darkness** — you only see the area around you plus a flashlight cone toward the cursor.

## Files

- `index.html` — everything (map, AI, rendering, audio)
- `play.bat` — opens the game

## Notes

Single-player prototype. Multiplayer (2–8 players, one seeker) could be layered on the
existing `../hide-and-seek/server.py` websocket server next.
