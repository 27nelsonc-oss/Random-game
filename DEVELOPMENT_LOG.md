## 2026-10-29 — Slash projectile parry
- Extended Slash upgrade 3 (larger swing) to parry ranged-enemy projectiles while the sword arc is active, on outbound and return swings. Updated the card description and used projectile-path collision checks. Both HTML copies updated identically; JavaScript syntax and source checks performed, not browser-tested.

## 2026-10-29 — Escape pause
- Added an Esc-controlled pause overlay and Resume button. Switched gameplay timing to an accumulated active-play clock so cooldowns and animation states do not advance during pause or level-up choices. Both HTML copies updated identically; JavaScript syntax checked, no real-browser test.

## 2026-10-28 — Ranged enemies
- Added a 4-HP purple ranged enemy starting at wave 7, moving at the normal enemy's speed. It fires 1-damage projectiles every 1.6 seconds when the player is within 360 units and tries to maintain 255–325 units of distance. Projectiles move at 300 units/second and use the existing player damage cooldown.
- Wave 7 guarantees one ranged spawn, with the guarantee increasing by one every five waves; additional eligible spawns have a 15% chance to be ranged. Added projectile visuals and cleanup on wave transitions/restart while preserving existing enemy types. Both HTML copies updated identically. JavaScript syntax and source-level checks only; real-browser gameplay not tested.

## 2026-10-28 — Tank durability
- Increased tank enemy maximum health from 5 to 20 HP while preserving normal enemies at 5 HP, small enemies at 3 HP, and all other tank behavior. Updated both HTML copies identically. JavaScript syntax and source-level checks performed; real-browser gameplay not tested.

## 2026-10-28 — Tank enemies
- Added a larger, dark-red tank enemy starting at wave 10. It keeps 5 HP, moves at 165 versus the normal enemy's 180, and deals 2 damage per contact hit.
- Guaranteed tank spawns start at 2 on wave 10 and increase by one every five waves; other eligible spawns have a 15% tank chance. Preserved the existing small-enemy system, applying tank selection before small-enemy random rolls and keeping both guarantee counters per wave. Updated both HTML copies identically. Source-level checks only; real-browser gameplay not tested.

## 2026-10-28 — Small enemies
- Added a smaller enemy type from wave 5 onward with 3 HP and 275 movement speed versus the player's 250. Wave 5 guarantees two small-enemy spawns, increasing by one every five waves; other spawns have a 20% small-enemy chance.
- Applied the selection rules to both initial wave spawns and respawns, added smaller enemy visuals/health bars, and reset the small-enemy counter on each new wave and restart. Updated both HTML copies identically. Source-level checks only; real-browser gameplay not tested.

## 2026-10-28 — Slash upgrades
- Added four Slash upgrades: half-second cooldown reduction (3.0s to 2.5s); an outward-and-returning swing; slightly increased radius, thickness, and attack range; and a small outward knockback on the second hit from the return swing.
- Updated Slash card text, level display, and hide-at-max behavior; restart resets its upgrade level. Both HTML files updated identically. Source-level checks only; real-browser gameplay not tested.

## 2026-10-28 — Smite upgrades
- Added four Smite upgrade levels: reload reduced from 5 seconds to 3.5 seconds; beam pierces enemies and ends at the arena boundary; beam width increases to hit more enemies; and the beam lasts 1 second, dealing a hit every 0.25 seconds to enemies that remain inside it.
- Updated Smite's level-up card text and hide-at-max behavior; restart resets its upgrade level. Both HTML copies updated. Source-level verification only; real-browser gameplay not tested.

## 2026-10-28 — Fix startup freeze
- Diagnosed the startup freeze by executing a simulated first animation frame: the game loop called `updateSlash` and `updateSmite`, but both function definitions had been accidentally removed. Restored both functions from the last known version that contained them, preserving their existing cooldowns, damage, visuals, and defeat handling.
- JavaScript syntax and a simulated first animation frame passed after the fix. Browser gameplay still needs a real-browser check.

## 2026-10-28 — Yoyo upgrades
- Added four Yoyo upgrades: second Yoyo with a distinct initial target, cooldown reduced from 1.8s to 1.2s at upgrade 2, speed increased from 650 to 850 at upgrade 3, and a damaging connector rope at upgrade 4. Both Yoyos wait until fully extended before returning together so the triangle-shaped rope can appear without changing their travel paths.
- Updated both HTML copies and project logs. Source checks only; browser gameplay not tested.

## 2026-10-28 — Ball upgrades
- Added four upgrade levels after the initial Ball purchase. Each upgrade adds one guaranteed target; upgrade 3 adds recursive 25% bonus-bounce chances and halves the cooldown, while upgrade 4 raises the chance to 50% and removes bounce damage reduction.
- Ball upgrade card text updates by level and is hidden at max level. Restart clears Ball ownership and upgrade progress. Both HTML copies updated; source checks only, browser gameplay not tested.

## 2026-10-28 — Sword Ring upgrades
- Added four selectable upgrades after the initial Sword Ring purchase. Sword count progresses from 1 to 5; the second upgrade adds a second revolution, the third reduces cooldown to 2 seconds, and the fourth removes cooldown.
- Level-up choices update their Sword Ring label/description and stop offering it after max level. Restart clears Sword Ring and upgrade progress. Updated both HTML copies; source checks only, browser gameplay not tested.

## 2026-10-28 — Sword Ring
- Added a fifth level-up option and changed the card roll to choose three distinct options from five.
- Added a moving-player orbit attack with one hit per enemy per orbit, a three-second cooldown after a complete rotation, and restart reset. Updated both HTML copies. Source inspection only; browser gameplay not tested.

## 2026-10-28 — Fullscreen and wave announcements
- Wrapped the arena, upgrade overlay, and HUD in a fullscreen-capable game shell with a toggle button; fullscreen CSS scales the arena to fit the viewport while retaining the overlay and status displays.
- Added a two-second canvas wave announcement on initial play, each wave transition, and restart. Updated both HTML copies and changelog; source-level checks only, browser fullscreen/gameplay not tested.

## 2026-10-28 — Scaling simultaneous enemies
- Expanded the existing enemy array dynamically at wave transitions; active limit rises by one every two waves, capped by the wave defeat target. Existing combat systems iterate the same array.
- Clear all surviving enemies at wave completion, preserve the three-second grace period, and trim the array back to two on restart. Updated both HTML copies and changelog; source-level verification only, no browser gameplay test.

## 2026-10-28 — Enemy waves
- Added a four-defeat first wave, increasing the defeat target by one per wave, using the existing two enemy slots and random-edge respawns. Centralized enemy defeat accounting for projectiles, Yoyo, Ball, Slash, and Smite.
- Added a three-second enemy-free interval, wave HUD, and wave-state reset on restart. Existing XP/healing pickups persist through wave transitions. Source-level checks only; browser gameplay not tested.

## 2026-10-27 — Randomized level-up cards
- Changed level-up card presentation to show three of the four abilities, randomly hiding one each time. Each ability therefore has a 75% chance to appear in a given selection, with no duplicates.
- Rerolls the three visible choices for each pending level-up and prevents hidden cards from being selected. Preserved the four abilities and their effects; returned the wide-screen grid to three columns.
- Updated both HTML copies and the changelog. Source-level checks only; browser gameplay was not tested.

## 2026-10-27 — Smite ability
- Added Smite as a fourth level-up card while preserving Yoyo, Ball, and Slash. Once selected, Smite chooses a random living enemy every 5 seconds, deals 5 damage, and displays a brief bright beam from the player to the target.
- Smite defeats use the existing enemy respawn, XP-drop, and 10% healing-drop behavior. Restart clears Smite ownership, beam state, and cooldown; level-up cards use four columns on wider screens and two columns on narrow screens.
- Updated both HTML copies and the changelog. Source-level checks only; browser gameplay was not tested.

## 2026-10-27 — Level-up healing and health drops
- Restore player HP to the maximum whenever a level is gained, and update the HP display immediately.
- Added a separate green healing cube drop with a 1-in-10 chance for each enemy defeat from automatic shots, Yoyo, Ball, or Slash. Collecting it restores 3 HP, capped at maximum health; restarting clears uncollected healing cubes.
- Updated both HTML copies and the changelog. Source-level checks only; browser gameplay was not tested.

## 2026-10-27 — Slash ability
- Replaced the third blank level-up card with Slash. When selected, the player performs an automatic close-range sweep aimed toward the mouse every 3 seconds; each enemy can take 3 damage once per swing.
- Added a visible curved slash effect and included defeated-enemy XP drops using the existing defeat flow. Restart clears Slash ownership, animation, and cooldown state.
- Updated both HTML copies and the changelog. Source-level checks only; browser gameplay was not tested.

## 2026-10-27 — Larger arena and random-edge enemy spawns
- Increased the arena's internal dimensions to 1440×900 and raised the responsive CSS width cap to 1200px.
- Added a random-edge spawn helper; both enemies begin on a randomly selected border and use their existing chase AI to walk inward. Every respawn chooses a new random edge and position.
- Updated both HTML copies and the change logs. Source-level checks only; browser gameplay was not tested.

## 2026-10-27 — Mouse-facing player eyes
- Added two small black eyes to the player, arranged side-by-side perpendicular to the facing direction and positioned toward the mouse.
- Added canvas-scaled mouse-coordinate tracking so the eyes follow the pointer correctly when the game is resized.
- Updated both HTML copies and the change logs. Source-level checks only; browser gameplay was not tested.

## 2026-10-27 — Ball upgrade and second enemy
- Added Ball as the second level-up card. After selection, it launches every 5 seconds, seeks the nearest living enemy for 2 damage, then bounces to the nearest other living enemy for 1 damage and disappears.
- Added a second chasing enemy with independent position, health, and two-second respawn countdown. Player auto-shots choose the nearest living enemy; Yoyo line checks can hit either enemy.
- Updated both HTML files and documented the change. Source-level checks only; browser gameplay was not tested.

# Development Log

## 2026-10-27 — Retry Yoyo tether and return fix
- Reworked the Yoyo's return phase to explicitly track whether it is returning, home toward the player's live coordinates, snap to the player when within one movement step, and only then begin its recovery cooldown.
- Kept the string drawn from the player's current position to the moving Yoyo head and preserved existing damage checks.
- Re-fetched both HTML files and checked JavaScript syntax; browser gameplay was not tested.

## 2026-10-27 — Yoyo tether follows player
- Changed the visible string to render from the player's live position to the yo-yo head, so movement no longer leaves the string anchored at the throw location.
- The returning yo-yo now homes toward the player's current position and finishes its return before starting the next attack cooldown.
- Kept the existing launch direction, attack speed, line collision damage, and per-leg hit tracking. Source-level checks only; browser gameplay was not tested.

## 2026-10-27 — Yoyo upgrade
- Replaced the first blank level-up card with Yoyo; the other two cards remain blank. Selecting Yoyo enables an automatic 1-damage yo-yo with a visible tether and circular head, aimed at the farthest living enemy.
- Collision checks cover the whole tether line, allowing multiple enemies to be hit without a target-count cap; each target can be hit once outbound and once on return. Attack repeats after recovery; restart clears the upgrade and its state.
- Source-level verification planned; browser gameplay and multi-enemy behavior were not tested.


## 2026-10-27 — Standalone named HTML copy
- Copied current `index.html` byte-for-byte into root-level `Random_Game.html` on `game-development` without changing the original game entry point or `main`.
- Verified the copied source against the original after committing; no browser or Cloudflare deployment test was performed.


## 2026-10-27 — Level-up card selection
- Added a responsive modal overlay with three intentionally blank buttons. A level-up pauses arena simulation until the player selects one card; the selection has no upgrade effect yet.
- XP carryover can trigger multiple level-ups; each one requires its own choice before gameplay resumes. Restart clears pending choices and closes the overlay.
- Source-level checks planned after commit; actual browser interaction was not tested.


## 2026-10-27 — Cube XP and leveling
- Added a compact level/XP readout beneath HP. Collecting a yellow cube grants 1 XP; 3 XP reaches level 1, then 5 additional XP reaches level 2, with the next requirement increasing by 2 each level (7, 9, 11, ...).
- Any XP beyond a level threshold carries forward. Restart resets level, XP, and the next-level requirement to their starting values.
- Reviewed the modified pickup and restart logic; browser gameplay was not tested.


## 2026-10-27 — Cloudflare Pages preparation
- Added deployment instructions to the README for linking the repository to Cloudflare Pages through Git integration.
- Confirmed the game entry point is the top-level `index.html`; no build tool, dependencies, or environment variables are needed.
- Recommended `game-development` as the Pages production branch so `main` remains unchanged. Deployment itself must be completed in the Cloudflare dashboard; it was not run or tested here.

## 2026-10-27 — Yellow pickup drops
- Added a small yellow square collectible at the enemy's location whenever it is defeated.
- The player collects it by moving close enough; the collectible disappears on pickup.
- Restart clears uncollected drops. Source-level checks only; browser gameplay was not tested.

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
