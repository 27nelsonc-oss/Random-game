# Development Log

## 2026-10-27 — Retry enemy respawn fix
- Replaced the animation timestamp deadline with a two-second countdown that decreases by frame delta while the enemy is defeated.
- At zero, the enemy returns to its start position with full health; the next automatic shot is delayed by one second.
- Source and JavaScript syntax checked; browser gameplay was not tested.

## 2026-10-27 — Enemy respawn
- Added a two-second respawn delay after the enemy is defeated; it returns to its starting position with full 5 HP.
- Delayed the next automatic shot by one second after respawn so the player gets a moment before firing again.
- Re-fetched and checked the source; browser gameplay was not tested.

## 2026-10-27 — Automatic shooting and enemy health bar
- Added a visible projectile fired once per second toward the living enemy.
- Projectiles travel in a straight line and deal 1 damage on collision; the enemy has 5 HP.
- Added a health bar above the enemy and hide/stop the enemy at 0 HP.
- Restart restores the enemy's starting position and full health and clears active projectiles.
- Verified the updated source on GitHub; browser gameplay was not tested.

## 2026-10-27 — Retry enemy chase fix
- Increased the enemy's chase speed to 180 canvas units per second for visibly stronger pursuit.
- Reworked the movement step to cap travel at the remaining distance to the player, avoiding overshoot near the target.
- Updated the source on `game-development`; browser gameplay was not available to test directly.

## 2026-10-27 — Enemy movement
- Made the red enemy slowly pursue the player at 105 units per second, compared with the player's 250.
- Kept the enemy within arena bounds and its direction marker aimed at the player.
- Source was checked on GitHub; gameplay was not browser-tested.

## 2026-10-27 — Damage invincibility balance
- Changed the existing next-damage timestamp offset from 100 ms to 750 ms without altering collision, health, restart, or mobile controls.
- Verified the updated source on GitHub; browser gameplay was not tested.

## 2026-10-27 — Mobile controls
- Added touch/pen pointer capture on the arena with movement direction and short drag distance for full speed; no visible joystick.
- Release, cancellation, and window blur clear touch movement. A tap while defeated restarts and updates the game-over prompt.
- Source inspected after editing; no actual phone or browser gameplay test was performed.

## 2026-10-27 — Continuous contact damage with cooldown
- Replaced the contact-entry latch with a 100 ms next-damage timestamp based on the animation frame time.
- Continuous overlap can cause another hit after cooldown; leaving and re-entering does not bypass the cooldown.
- Restart clears the cooldown. Source checked; browser gameplay not tested.

## 2026-10-27 — Restart after zero HP
- Added a game-over overlay and halted movement at zero HP.
- A keydown while defeated restores 10 HP, the initial player position, and clears held keys/contact state.
- Source reviewed after editing; browser gameplay was not tested.

## 2026-10-27 — Player HP and collision damage
- Added visible player HP starting at 10 / 10.
- Added circle overlap detection and a contact latch: one damage on contact entry, requiring separation before another hit.
- HP cannot go below zero. Source verification performed; no browser test.

## 2026-10-27 — Added red target circle
- Added a stationary red circle matching the player's size.
- Added a small black dot that points toward the player's current position.
- Checked the source after editing; no browser test was performed.


## 2026-10-27 — Reapply unmistakable flat white player
- Replaced the player draw statement with an explicit solid white fill, disabled shadow/outline effects, and increased the circle radius from 17px to 22px.
- Left movement logic, grey arena, and grid spacing unchanged.
- Validation: re-fetched the updated file and checked the drawing code; browser gameplay was not tested.

## 2026-10-27 — Grey ground and top-down white player
- Changed the ground to neutral grey and kept a simple darker grey grid.
- Replaced the stylized character drawing with a plain white circle, representing a cylinder viewed directly from above.
- Kept movement and arena-edge constraints unchanged.
- Validation: reviewed the updated HTML source; browser gameplay was not tested.

## 2026-10-27 — Simplify to movement foundation
- Replaced the first survival prototype with only a bounded platform, a simple visible player character, and WASD/arrow-key movement.
- Removed combat, enemies, XP, upgrades, and run UI as requested.
- Validation: reviewed the HTML and JavaScript structure. No browser execution was performed.

## 2026-10-27 — Project setup and prototype 0.1
- Created the `game-development` branch from `main`; `main` remains unchanged.
- Inspected the repository before editing. It initially contained only `README.md`.
- Added the first self-contained HTML prototype: movement, chasing enemies, automatic attacks, XP gems, level-up choices, upgrades, health, waves, pause, and restart.
- Added `DEVELOPMENT_RULES.md` and `CHANGELOG.md`.
- Validation performed: reviewed the source structure and game-loop flow. No real browser execution or automated browser test was available during this edit.
