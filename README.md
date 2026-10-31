# Midnight Hide & Seek

A 2.5D single-player hide-and-seek game (Among Us-style characters, top-down with
depth-sorted walls). Built as one self-contained HTML file — no install, no dependencies.

**Play online:** https://itzduckguy1.github.io/midnight-hide-and-seek/

## Play

- Double-click **play.bat**, or just open **index.html** in a browser.
- Or serve it: `python -m http.server 8010` from this folder, then open http://127.0.0.1:8010
- **On phone:** open the same link — touch controls appear automatically.

## Controls

### Desktop
| Key | Action |
| --- | --- |
| WASD / Arrows | Move |
| Shift | Dash (dodge, brief invulnerability) |
| E | Hide in a locker / open the vent network |
| Ctrl (hold) | Sneak — quieter, harder to spot |
| Left mouse | Shoot / katana slash — **hold to keep firing** |
| Right mouse | Parry — only works if you're facing the seeker |
| R | Reload |
| Esc | Pause (or close the vent panel) |

### Mobile
| Control | Action |
| --- | --- |
| Left stick | Move (analog) |
| Right stick | Aim — push past halfway to fire |
| DASH / PARRY / USE | Dash, parry, hide or open vents |

## Goal

Survive **120 seconds**. The seeker patrols, hears gunshots, chases you, and searches
lockers. You can down it with lead or steel — it comes back after 6 seconds, angrier.

## Mechanics

- **Lockers** — press E to hide. The seeker searches one if it lingers beside it (0.9s).
- **Vents** — press E at a grate to open the **vent network**: pick any destination from a
  list (Cargo Bay, Med Bay, Reactor, Cafeteria, Storage, Admin, Engine). The game keeps
  running while you choose, so don't stand still too long.
- **Parry** — right-click with the katana, **facing** the seeker. A 0.16s window, 1.4s
  cooldown, stuns the seeker for 1.6s. Miss the window and you eat the hit.
- **Dash** — dodges through a strike and gives i-frames.
- **Ammo boxes** — walk over them for +4 ammo (respawn in 20s).
- **Darkness** — you only see the area around you plus a flashlight cone toward your cursor.

## Difficulty (current tuning)

- Seeker: 180 HP, 186 px/s chase speed, 400px sight, 28 damage, 0.8s attack cooldown,
  0.9s locker search, 6s respawn.
- Player: 200 px/s, dash 1.1s cooldown, parry 0.16s window / 1.4s cooldown.

## Files

- `index.html` — everything (map, AI, rendering, touch controls, audio)
- `play.bat` — opens the game
- `README.md` — this file
