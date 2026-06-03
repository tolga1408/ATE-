# ATEŞ Agent Operating Instructions

These instructions apply to the whole repository.

## Mission

ATEŞ is a mobile-first arcade card game. The goal is to turn it into a polished, shareable, monetizable web game without over-engineering the current static GitHub Pages architecture.

## Repo Rules

- Preserve GitHub Pages deployment from the repository root.
- Keep the game playable as a static site.
- Treat `index.html` as production-critical.
- Prefer small, reviewable changes over rewrites.
- Do not add a backend, login system, database, or payment flow without a written reason and rollback plan.
- Do not add ads or portal SDKs until the core game is stable and tested.
- Do not introduce a framework just for style polish.
- After changing gameplay, manually test at least five full runs.
- After changing layout, test desktop and mobile widths.
- After changing share or metadata, test the live GitHub Pages URL.

## Launch Quality Bar

A change is not launch-ready unless:

1. The game starts from the public URL.
2. OYNA starts gameplay.
3. Pause/resume works.
4. Game over appears correctly.
5. TEKRAR restarts correctly.
6. High score persists after refresh.
7. Share button works or falls back gracefully.
8. There are no dead visible controls.
9. There are no production-visible TODO labels.
10. Mobile tap behavior feels immediate.

## Product Guardrails

- Make the first 30 seconds exciting.
- Make danger obvious.
- Make score improvement feel rewarding.
- Make restart frictionless.
- Avoid menus, currencies, login, or store mechanics until there is real traffic.
