# tilakverse-assets

Source asset packs for [tilakpatell.com](https://tilakpatell.com)'s 3D worlds, kept apart from the site's repo so its clones and deploys stay small. Each pack is exactly as it was downloaded: Blender sources, FBX, OBJ, glTF/GLB, textures, and engine exports.

Every pack under `quaternius/` is **CC0 1.0** (public domain), by [Quaternius](https://quaternius.com). Credit isn't needed, though the site names Quaternius in its credits when a pack's models go into a world. Support him on [Patreon](https://www.patreon.com/quaternius).

## Getting them

The whole repo (about 2.2 GB):

```
git clone https://github.com/tilakpatell/tilakverse-assets.git
```

Or one pack, without the rest:

```
git clone --filter=blob:none --sparse https://github.com/tilakpatell/tilakverse-assets.git
cd tilakverse-assets
git sparse-checkout set quaternius/universal-animation-library-2
```

From the site's repo, `node scripts/assets-fetch.mjs <pack>` fetches a pack's zip from the site repo's `assets-quaternius` release into its git-ignored `lab/assets/`.

## The packs

| folder | what | for |
| --- | --- | --- |
| `quaternius/universal-animation-library` | Universal Animation Library (source): 120+ humanoid clips. `Unreal-Godot/UAL1.glb` has them all (and `UAL1_RM.glb` with root motion), plus FBX for Unity and the `.blend`. Covers walking and jogging in 8 directions, crouching, crawling, climbing, sitting, hits, deaths, a pistol, punches, spells, swimming, driving, a shop counter | every rigged figure: `scripts/ual-bake.mjs` in the site repo bakes clips onto the Meshy skeleton |
| `quaternius/universal-animation-library-2` | Universal Animation Library 2 (source): 130+ more clips in `Unreal-Godot/UAL2.glb`, plus the female mannequin. Covers melee and sword combos, strafes, parkour, deaths, talking, carrying, lying down, being lifted, farming, fishing, zombies | the same |
| `quaternius/downtown-city-megakit` | Downtown City MegaKit (standard): modular brick and metal facades, windows, doors, cornices, roofs, three whole buildings, streets, sidewalks, road decals, props | Albuquerque, Invincible's city, Scranton |
| `quaternius/street-pack` | road tiles, bridges, ramps, traffic lights, street lights, signs | Albuquerque, Invincible |
| `quaternius/furniture-pack` | beds, sofas, chairs, tables, bookcases, closets, lamps, vases | interiors in every world |
| `quaternius/ultimate-space-kit` | astronauts and mechs (rigged), enemies, rovers, spaceships, domes and base parts, alien trees, rocks, planets, pickups | the Rick and Morty dimensions, toy space props |
| `quaternius/farm-animals` | horse, cow, sheep, pig, llama, zebra, pug, rigged and animated | Middle-earth (ponies, the Shire's sheep, Rohan's horses) |
| `quaternius/stylized-nature-pack` | birch, maple, pine, palm and dead trees, bushes, flowers, grass, rocks | the Shire, Lothlórien, Naboo, Yavin 4 |
| `quaternius/stylized-nature-megakit` | Stylized Nature MegaKit (source): five of each tree, bushes, ferns, flowers, grasses, mushrooms, rocks, rock paths, pebbles, and the Godot project | the same worlds' ground cover and paths |

The Nature MegaKit's Unreal, Unity and Godot projects (204, 207 and 89 MB zips) are attached to this repo's [`engine-projects`](https://github.com/tilakpatell/tilakverse-assets/releases/tag/engine-projects) release instead, split into parts: `cat Stylized_Nature_MegaKitGodot.zip.part-* > Stylized_Nature_MegaKitGodot.zip` (sha256 `27fe9a17d0aec1e4f2036a7edd89b28a351f763c5c8f513055f6418495223e16`).

## Sketchfab

`sketchfab/star-wars/` lists Star Wars models from Sketchfab: a rigged B1 battle droid, a rigged and animated AT-AT, a TIE fighter and two Venators. They are CC BY or CC BY-NC-SA, not CC0, and the GLBs themselves are on the [`sketchfab-star-wars`](https://github.com/tilakpatell/tilakverse-assets/releases/tag/sketchfab-star-wars) release.
