# Wildlands — Survival Strike

**Live:** https://jgitom.github.io/wildlands/

An open-world survival FPS built with Three.js. No build step, no backend, and no remote assets — the game ships as `index.html` plus a vendored Three.js build.

## Play

Serve the folder (see below) and click **ENTER WILDLANDS**. If you have a saved run, the main button becomes **CONTINUE — DAY NN**.

| Input | Action |
| --- | --- |
| `W A S D` | Move |
| Mouse | Aim / attack |
| `Shift` | Sprint (uses stamina) |
| `Space` | Jump |
| `E` | Interact — chop, mine, forage, loot, cook, drink, harvest |
| `C` | Crafting panel |
| `F` / `B` | Eat / use bandage |
| `O` | Settings |
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
- **Synthesized audio** — footsteps, chopping, mining, bow, impacts, fire, UI, plus wind, birds and wolf howls. No audio files are bundled.
- **Save / continue** — the run (position, stats, inventory, tools, day/time, harvested resources, crates, wildlife) autosaves every 12 s, on pause, and on page hide. The best day is tracked separately.
- **Settings** — mouse sensitivity, master volume, FOV, shadows, fullscreen; persisted in `localStorage`.
- **No remote dependencies** — Three.js is vendored under `vendor/`, so the game runs offline once served.

## Run locally

```bash
python3 -m http.server 8089
# then open http://localhost:8089
```

Serve the folder rather than double-clicking `index.html`: browsers block local ES-module imports over `file://`. Any static host works; there is no network dependency.

## Deploy (GitHub Pages)

1. Create a GitHub repo and push this folder to `main`.
2. Repo → **Settings → Pages → Deploy from a branch → `main` / `/ (root)`**.
3. The game is live at `https://<user>.github.io/<repo>/`.

`.nojekyll` is included so the site is served as-is.

## Layout

```
index.html                    the whole game (UI, world, gameplay, audio, save)
vendor/three.module.min.js    Three.js r180 (MIT)
vendor/three.core.min.js      Three.js core (imported by the module build)
vendor/THREE-LICENSE.txt      Three.js MIT license
archive/wave-shooter.html     previous wave-based build, kept for reference
```

## Credits & licensing

- **Three.js** © three.js authors, MIT — see `vendor/THREE-LICENSE.txt`.
- All game code, geometry, UI, and synthesized audio in this repository are original; no external art, music, or font files are included.
- To publish on itch.io, upload a zip containing `index.html` and `vendor/` with `index.html` at the root.
