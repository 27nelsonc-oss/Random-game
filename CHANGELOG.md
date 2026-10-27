# Changelog

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
