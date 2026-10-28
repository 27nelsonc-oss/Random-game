# Random Game — Arena Survivor

A browser-based top-down arena survival roguelite prototype inspired by the general Brotato-style genre.

## Play
Open `index.html` in a modern browser. No build step or external libraries are required.

## Controls
- **WASD / Arrow keys:** Move
- **Space:** Pause / resume
- **Attacks:** Automatically target the nearest enemy in range

## Current prototype
- Enemy waves and chasing enemies
- Automatic shooting and health/damage
- XP gems and three-choice level-up upgrades
- Run upgrades, pause/restart, and responsive HUD

## Deploy with Cloudflare Pages

This is a plain static HTML game; it does not need a framework, package installation, or build step. The playable entry file, `index.html`, is at the repository root.

When connecting this GitHub repository to Cloudflare Pages, use these settings:

- **Production branch:** `game-development` (keeps deployment tied to the development branch; `main` remains untouched)
- **Framework preset:** `None` / no framework
- **Build command:** leave blank
- **Build output directory:** `.` (the repository root, where `index.html` lives)
- **Root directory:** leave blank / repository root
- **Environment variables:** none required

Cloudflare Pages setup starts at [Workers & Pages](https://dash.cloudflare.com/) → **Create application** → **Pages** → **Connect to Git**. Authorize GitHub, select `27nelsonc-oss/Random-game`, enter the settings above, then deploy. Afterward, new commits pushed to `game-development` can trigger automatic deployments. See the [official Cloudflare Pages Git integration guide](https://developers.cloudflare.com/pages/get-started/git-integration/).

## Project workflow
See [DEVELOPMENT_RULES.md](DEVELOPMENT_RULES.md), [CHANGELOG.md](CHANGELOG.md), and [DEVELOPMENT_LOG.md](DEVELOPMENT_LOG.md). Development happens on `game-development`; do not change `main` without explicit permission.
