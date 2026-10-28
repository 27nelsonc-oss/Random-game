## 0.3.25 — Yoyo upgrades
- Added four Yoyo upgrades after the initial purchase: a second Yoyo targeting a different enemy, reduced cooldown, increased travel speed, and a damaging rope between both Yoyos once both reach full extension.
- The two Yoyos wait at full extension until both are extended, then return together; the connecting rope does not affect movement. The Yoyo card updates per level and disappears at max level.

## 0.3.24 — Ball upgrades
- Added four Ball upgrades after the initial purchase. Each upgrade adds one guaranteed enemy to its bounce chain, progressing from 2 to 6 guaranteed targets.
- Upgrade 3 adds a 25% chance to continue bouncing after the guaranteed chain (each extra bounce rolls again) and reduces the cooldown from 5 seconds to 2.5 seconds. Upgrade 4 raises the repeat-bounce chance to 50% and keeps damage at 2 on every hit. The Ball card updates its description and disappears when fully upgraded.

## 0.3.23 — Four Sword Ring upgrades
- Sword Ring now has four upgrade picks after its initial purchase. Upgrades add swords: 2 total after upgrade 1, 3 after upgrade 2, 4 after upgrade 3, and 5 after upgrade 4.
- Upgrade 2 makes each activation complete two revolutions; upgrade 3 reduces the cooldown to 2 seconds; upgrade 4 removes the cooldown for continuous activations. Each enemy can be hit once per revolution. The upgrade card disappears once fully upgraded.

## 0.3.22 — Sword Ring
- Added Sword Ring as a fifth possible level-up ability. Each selection still displays three distinct randomly chosen cards.
- The owned sword completes one orbit around the moving player in 1.2 seconds, dealing 2 damage once per enemy per orbit, then disappears for 3 seconds before returning. Defeats use the existing drop system; restart clears the ability.

## 0.3.21 — Rare XP magnet pickup
- Defeated enemies have a 1-in-50 chance to drop a red cube in addition to normal XP and possible healing cubes.
- Collecting the red cube attracts every existing XP cube toward the player for normal XP collection. Restart clears red pickups.

## 0.3.20 — Fullscreen and wave announcements
- Added a Fullscreen / Exit Fullscreen button for the game area, with the level-up selection and HP/XP/wave HUD retained inside fullscreen mode.
- Display a centered WAVE number announcement for two seconds at the start of wave 1 and each subsequent wave; restarting restores the first-wave announcement.

## 0.3.19 — Scaling simultaneous enemies
- The simultaneous enemy limit now increases by one every two waves: 2 on waves 1–2, 3 on waves 3–4, 4 on waves 5–6, and so on, never exceeding that wave's defeat target.
- Additional enemies use the same chase, health, random-edge spawn, combat, and drops as existing enemies. The three-second grace period removes all remaining enemies, and restart restores the initial two-enemy setup.

## 0.3.18 — Enemy waves
- Wave 1 requires four enemy defeats. Each following wave requires one more defeat (5, 6, 7, ...), with up to two enemies active at a time and replacements spawning from random arena edges until the wave quota is met.
- Clearing a wave gives a three-second enemy-free grace period, displays wave progress/countdown, and starts the next wave automatically. XP and healing drops remain available between waves; restart returns to wave 1.

## 0.3.17 — Randomized level-up cards
- Level-up choices now show three randomly selected abilities from Yoyo, Ball, Slash, and Smite. Each ability has a 3-in-4 (75%) chance to appear in a level-up selection, with no duplicate cards in the same selection.
- When multiple level-ups are pending, each new choice screen rerolls the available cards. Existing ability effects and cooldowns are unchanged.

## 0.3.16 — Smite ability
- Added Smite as a fourth level-up choice. Once selected, it fires a brief visible beam at a randomly chosen living enemy every 5 seconds, dealing 5 damage; defeating an enemy uses the existing XP and healing-drop behavior.

## 0.3.15 — Level-up healing and health drops
- Restored the player to full HP whenever they gain a level.
- Added a green healing cube with a 10% drop chance when an enemy is defeated; collecting it restores 3 HP without exceeding maximum health.

## 0.3.14 — Slash ability
- Added Slash as the third level-up card. Once selected, the player automatically sweeps a close-range sword arc toward the mouse aim every 3 seconds, dealing 3 damage to each enemy hit once per swing.

## 0.3.13 — Larger arena and random-edge enemy spawns
- Expanded the game arena from 960×600 to 1440×900 and increased its maximum displayed width.
- Both enemies now start at randomly selected points along the arena border and enter by chasing the player. Each respawn also chooses a fresh random border location.

## 0.3.12 — Mouse-facing player eyes
- Added two small black eyes to the white player; the pair turns toward the mouse pointer to show the player's facing direction.

## 0.3.11 — Ball upgrade and second enemy
- Added a Ball level-up choice. Once selected, a small ball launches automatically every 5 seconds toward the nearest living enemy, deals 2 damage on contact, then bounces to the closest other living enemy for 1 damage before disappearing.
- Added a second chasing enemy with its own health and respawn timer; automatic shots and the Yoyo can target either living enemy.

# Changelog

## 0.3.10 — Reliable Yoyo return
- Made the Yoyo's return phase explicitly track its state and snap the head to the player's current position when it reaches them, before starting the recovery cooldown.
- Preserved the live player-anchored string and existing damage behavior.

## 0.3.9 — Player-attached Yoyo tether
- The string now stays anchored to the player's current position as the player moves.
- The yo-yo head returns directly toward the moving player and the attack only resets after it reaches the player.

## 0.3.8 — Yoyo upgrade
- Added Yoyo as the first level-up card. Choosing it enables an automatic yo-yo attack aimed toward the farthest living enemy.
- The visible tether and ball travel outward and retract; the attack deals 1 damage to each enemy intersecting its line once on the outward leg and once on the return leg, without a target-count cap.
- The attack repeats automatically after a short recovery. Restart resets the selected upgrade for the new run.


## 0.3.7 — Standalone named HTML copy
- Added `Random_Game.html` as an exact copy of the current game for separate testing, retaining `index.html` unchanged.


## 0.3.6 — Level-up card selection
- When a player levels up, gameplay pauses and a centered overlay presents three blank, clickable cards; choosing one dismisses the choice and resumes play.
- Each level-up requires a separate card selection, including when XP carries over multiple level thresholds.
- Restart closes any open selection overlay and resets its state.


## 0.3.5 — Cube XP and leveling
- Collecting each yellow cube grants 1 XP; the HUD shows the current level and progress toward the next level.
- Level 1 requires 3 cubes, level 2 requires 5 additional cubes, then each later level costs 2 more cubes than the previous level.
- Restart resets level and XP along with the existing run state.


## 0.3.4 — Cloudflare Pages deployment readiness
- Added Cloudflare Pages Git-integration setup instructions to the README for this root-level static HTML game.
- Documented `game-development` as the intended production branch and the root directory as the static output.
- No game mechanics or gameplay files were changed in this setup-only update.

## 0.3.3 — Yellow enemy drops
- Each defeated enemy drops a small yellow cube at its defeat location.
- The player can collect the cube by moving into it; collected cubes disappear.
- Restart clears any uncollected cubes.

## 0.3.2 — Reliable enemy respawn timer
- Replaced the respawn deadline check with a frame-based two-second countdown after the enemy is defeated.
- The countdown restores the enemy to its starting position with full HP.

## 0.3.1 — Enemy respawn
- A defeated enemy respawns at its starting position with full 5 HP after 2 seconds.
- The player waits one second after the respawn before the next automatic shot.

## 0.3.0 — Automatic projectiles and enemy health
- The player automatically fires a visible projectile toward the enemy every second.
- Each projectile deals 1 damage; the enemy starts with 5 HP and displays a health bar above it.
- The enemy disappears and stops chasing when defeated; restarting after Game Over restores the enemy and clears projectiles.

## 0.2.1 — Stronger enemy pursuit
- Increased enemy chase speed from 105 to 180 canvas units per second so movement is easier to notice.
- Made each chase step explicitly stop at the player's position rather than overshooting it.

## 0.2.0 — Slow chasing enemy
- The red enemy now moves toward the player continuously at 105 canvas units per second, slower than the player's 250.
- Enemy stays inside arena boundaries; its direction dot continues to face the player.

## 0.1.9 — Longer damage invincibility
- Increased the post-hit invincibility period from 0.1 seconds to 0.75 seconds.
- Continued enemy contact still deals 1 damage each time invincibility expires.

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
