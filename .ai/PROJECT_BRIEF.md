# ATEŞ Project Brief

## Goal

Turn ATEŞ into a polished, mobile-first browser game with strong replay value and a realistic path to public distribution.

## Live URL

https://tolga1408.github.io/ATE-/

## Current Repo Shape

- Main game file: `index.html`
- Static hosting: GitHub Pages from `main` root
- No framework
- No backend
- No build step

## Product Positioning

ATEŞ is a fast arcade card game where every card in your hand is burning. The player taps cards before their fuses run out, chains combos, and survives as long as possible.

## Near-Term Priorities

1. Launch hardening
2. Mobile polish
3. Sound and mute implementation
4. Shareability
5. Game-feel improvement
6. Public beta feedback
7. Portal submission preparation
8. Revenue experiments only after retention evidence

## Do Not Do Yet

- Do not add backend accounts.
- Do not add a payment flow.
- Do not add ads before the game is polished.
- Do not add portal SDKs until the base web version is stable.
- Do not add gambling-like or speculative mechanics.

## Working Method

Use the repo-level subagents and skills in `.ai/` before making project changes.

For every change:

1. Identify the relevant skill.
2. Identify the relevant subagent role.
3. Make the smallest useful patch.
4. Explain what changed.
5. Give the exact next test.
