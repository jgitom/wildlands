# Wildlands — Survival Strike

**Live:** https://jgitom.github.io/wildlands/

A single-file open-world survival FPS built with Three.js. No build step, no assets, no backend — just `index.html`.

## Play

Open `index.html` (or serve the folder) and click **ENTER WILDLANDS**.

| Input | Action |
| --- | --- |
| `W A S D` | Move |
| Mouse | Aim / attack |
| `Shift` | Sprint (uses stamina) |
| `Space` | Jump |
| `E` | Interact — chop, mine, forage, loot, cook, drink, harvest |
| `C` | Crafting panel |
| `F` / `B` | Eat / use bandage |
| `1` `2` `3` | Axe · Bow · Torch |
| `Esc` | Pause |

## Features

- **Procedural island world** — rolling terrain, a lake, ~1,500 instanced pines, boulders, forage bushes and ground cover.
- **Day / night cycle** — moving sun and moon, stars, fog and lighting; wolves and raiders hunt at night.
- **Three villages** — huts with lit windows, fences, campfires and lootable supply crates.
- **Survival stats** — health, food, water, stamina; food and water drain over time and damage you when empty.
- **Gathering & crafting** — wood, stone, fiber, hide; stone axe, bow, arrows, bandages, torch, leather vest.
- **Combat & hunting** — bare hands, axe melee, bow projectiles, deer, wolves, and night raiders.
- **Exploration aids** — live circular minimap with villages, game and hostiles.
- **Persistence** — best survival day is stored in `localStorage`.

## Run locally

```bash
python3 -m http.server 8089
# then open http://localhost:8089
```

Three.js is loaded from jsDelivr (`three@0.180.0`), so the page needs a network connection.

## Deploy (GitHub Pages)

1. Create a GitHub repo and push this folder to `main`.
2. Repo → **Settings → Pages → Deploy from a branch → `main` / `/ (root)`**.
3. The game is live at `https://<user>.github.io/<repo>/`.

`.nojekyll` is included so the site is served as-is.

## Layout

```
index.html                 the whole game (UI, world, gameplay)
archive/wave-shooter.html  previous wave-based build, kept for reference
```
