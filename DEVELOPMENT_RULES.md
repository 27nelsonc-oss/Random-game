# Development Rules — Random Game

These rules follow the same careful workflow used for Ultimate Idle Clicker.

1. Read `DEVELOPMENT_RULES.md`, `CHANGELOG.md`, and `DEVELOPMENT_LOG.md` before every code change.
2. The existing game files are the source of truth. Make only requested or explicitly agreed changes; do not rewrite, redesign, reorganize, or simplify unrelated systems.
3. Never change `main` without explicit permission. Develop on `game-development` unless the user asks otherwise.
4. Keep changes small and reversible. Preserve rollback paths and inspect the resulting commit.
5. Update `CHANGELOG.md` and `DEVELOPMENT_LOG.md` for each meaningful game change.
6. Verify HTML/JS structure, controls, layout, and gameplay logic after edits. Report honestly what was and was not tested; do not claim browser testing unless performed.
7. The user does not code and expects direct repository edits. Prefer browser-friendly HTML/CSS/JavaScript unless a different technology is agreed.
8. Keep the game UI free of developer-facing code or debug comments.
9. Ask before adding external services, accounts, paid dependencies, or systems that could risk player data.
10. Prioritize stability and preserve existing features when adding new ones.
