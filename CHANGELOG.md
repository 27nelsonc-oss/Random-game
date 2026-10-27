# Changelog

## 0.1.8 — Mobile touch movement
- Added an invisible touch joystick: touch and drag anywhere on the arena to move, release to stop.
- Disabled touch scrolling on the arena and allowed a tap on the game-over screen to restart.
- Preserved keyboard controls, enemy, HP, and damage mechanics.

## 0.1.7 — Contact damage cooldown
- Replaced one-hit-per-contact behavior with a 0.1-second damage cooldown after each hit.
- Staying inside the enemy continues to deal 1 HP damage whenever the cooldown expires.
- Restart resets the cooldown.

## 0.1.6 — Game over and restart
- At zero HP, movement stops and a Game Over message prompts the player to press any key.
- Any key resets player position, HP to 10, and collision state without changing the enemy or arena.

## 0.1.5 — Player HP and contact damage
- Player starts with 10 HP, displayed below the arena.
- Each new collision with the stationary red enemy removes 1 HP; remaining in contact does not repeatedly drain HP.
- HP stops at zero.

## 0.1.4 — Stationary red enemy
- Added one stationary red circular enemy matching the player's size.
- Added a small black direction dot that always points toward the player as the player moves.
- The enemy has no movement or AI.

## 0.1.3 — Explicit flat white circle
- Redrew the player explicitly as a flat, solid white circle with no visible outline or shadow, and increased its size slightly for visibility.
- Kept the grey grid arena and existing movement behavior.

## 0.1.2 — Grey arena and white player
- Changed the ground to grey with a simple darker grey grid.
- Changed the player to a plain white circle, representing a cylinder viewed directly from above.
- Kept WASD/arrow-key movement and arena boundaries.

## 0.1.1 — Movement foundation
- Simplified the game to a single arena platform and one player character.
- Added WASD and arrow-key movement with diagonal speed normalization and arena boundaries.
- Removed enemies, combat, XP, upgrades, HUD, and run menus for now; these can be added back in later milestones.

## 0.1.0 — First playable prototype
- Added a browser-playable top-down arena.
- Added WASD/arrow-key movement, enemy waves, automatic targeting and shooting, health, XP drops, and level-up choices.
- Added eight run upgrades, pause/restart controls, a run HUD, and responsive layout.
- Established the project development rules and development log.
