# Development Log

## 2026-10-27 — Simplify to movement foundation
- Replaced the first survival prototype with only a bounded platform, a simple visible player character, and WASD/arrow-key movement.
- Removed combat, enemies, XP, upgrades, and run UI as requested so the game can be built from scratch in small steps.
- Validation: reviewed the HTML and JavaScript structure after the edit. No browser execution was performed, so hands-on movement testing is still needed.

## 2026-10-27 — Project setup and prototype 0.1
- Created the `game-development` branch from `main`; `main` remains unchanged.
- Inspected the repository before editing. It initially contained only `README.md`.
- Added the first self-contained HTML prototype: movement, chasing enemies, automatic attacks, XP gems, level-up choices, upgrades, health, waves, pause, and restart.
- Added `DEVELOPMENT_RULES.md` and `CHANGELOG.md`.
- Validation performed: reviewed the source structure and game-loop flow. No real browser execution or automated browser test was available during this edit, so hands-on gameplay testing remains the next step.
- Next: play-test movement/combat/level-ups, fix any reported issues, then add between-wave materials/shop and more weapons.
