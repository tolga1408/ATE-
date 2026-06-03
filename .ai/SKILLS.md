# ATEŞ Project Skills

These are reusable working skills for improving ATEŞ. ChatGPT should use the relevant skill before proposing or making changes.

## Skill: Launch Hardening

Use when preparing ATEŞ for public beta or public launch.

Checklist:
- Confirm GitHub Pages URL.
- Remove dead UI controls.
- Remove production-visible TODOs.
- Add favicon.
- Add social metadata.
- Confirm high score persistence.
- Confirm share fallback.
- Confirm mobile layout.
- Update README.
- Run launch scorecard.

Output:
- Launch verdict: SHIP, BETA ONLY, or BLOCKED.
- Exact blockers.
- Smallest fix list.
- Manual tests completed or still required.

## Skill: Game Feel Polish

Use when improving moment-to-moment play.

Focus areas:
- Tap responsiveness.
- Fuse visibility.
- Critical danger warning.
- Combo feedback.
- Score popups.
- Restart speed.
- First-run clarity.
- Audio and mute if implemented.

Rules:
- Keep changes small.
- Do not change multiple mechanics at once.
- Test at least five full runs after balance changes.
- Report whether the game became easier, harder, clearer, or more exciting.

## Skill: Mobile QA

Use when changing layout, touch input, viewport, or HUD.

Viewports:
- 390 x 844 iPhone-like portrait
- 430 x 932 large phone portrait
- 360 x 800 Android-like portrait
- 768 x 1024 tablet
- 1366 x 768 desktop

Test cases:
- Start game.
- Tap all visible card types.
- Pause/resume.
- Let a card burn.
- Trigger game over.
- Restart.
- Share.
- Refresh and check high score.

Blockers:
- Cards too small.
- HUD overlaps.
- Game over hidden.
- Tap delay.
- Accidental zoom.
- Text selection.
- Unwanted scrollbars during gameplay.

## Skill: Monetization and Portal Readiness

Use when preparing ATEŞ for revenue or portal submissions.

First principle:
Do not monetize before the game is fun enough to replay.

Portal order:
1. Itch.io
2. Newgrounds
3. Reddit feedback posts
4. CrazyGames
5. Poki
6. GameDistribution

Required before portals:
- Stable mobile layout.
- No dead controls.
- No visible TODOs.
- Clean README.
- Clean game description.
- Share text.
- Favicon/social image.
- At least ten beta players.

Avoid:
- Predatory ads.
- Fake scarcity.
- Gambling mechanics.
- Crypto/NFT features.
- In-game currency before retention exists.

## Skill: Repo Safety

Use before making any repository changes.

Rules:
- Work on a branch for multi-file changes.
- Do not overwrite `index.html` unless the full file has been read or the user explicitly approves a rewrite.
- Keep generated documentation separate from gameplay code.
- Prefer one logical change per commit.
- Summarize files changed and why.
