# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project overview

87 is a tabletop RPG set in a post-collapse dystopian future. This repo contains the game manual and an interactive browser-based adventure kit — all as self-contained HTML files with no build system, no dependencies, and no frameworks.

## Running / developing

Open any HTML file directly in a browser — no server required:

```
open index.html
open kit_aventura_01.html
open aventura_01_senal_muerta.html
```

There are no tests, no linting tools, and no build steps. Changes take effect on browser refresh.

## File structure

| File | Purpose |
|---|---|
| `index.html` | Player manual — lore, rules, character creation, dice system |
| `aventura_01_senal_muerta.html` | Adventure module 01 — story, encounters, final boss GRÚA-7 |
| `kit_aventura_01.html` | Playable interactive kit — hex map, inventory, combat system |

The three files are interlinked via sidebar and header navigation.

## Architecture — kit_aventura_01.html

The interactive kit is a single-file vanilla JS app with all logic, state, and styles inlined. Key systems:

- **Hex map** — 12×9 procedural grid with fog-of-war and position tokens
- **Game state** — managed as a single JS object, persisted to `localStorage` with auto-save on every move
- **Event system** — 9 story hexes with unique events + pool of 14 random events with item drops
- **Inventory** — 7 item types; MOTE robot has 3 module slots and can upgrade to Level 2 via Núcleo de Procesamiento
- **Combat** — two tiers: minor (Guarda Clase I with 3 player actions) and main boss (GRÚA-7 with 3 phases, player actions + enemy turn)

## Design language

All files share a consistent dark sci-fi aesthetic:

- **Fonts** — Bebas Neue (headers), VT323 (terminal/mono display), Crimson Pro (body text), Share Tech Mono (UI labels)
- **Colors** — near-black backgrounds (`#080705`/`#06080a`), rust/amber accents, cyan highlights, muted warm text
- **CSS variables** — defined in `:root` at the top of each file; always use these vars rather than raw hex values
- The manual (`index.html`) uses warm rust/amber tones; the kit (`kit_aventura_01.html`) uses cooler blue/cyan tones

## Language

All game content, UI text, and in-file comments are in Spanish.
