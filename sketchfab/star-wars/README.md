# Sketchfab: Star Wars originals

Downloaded from Sketchfab on 2026-10-08, kept exactly as downloaded. The GLBs are too big to push through git reliably, so they live on this repo's [`sketchfab-star-wars`](https://github.com/tilakpatell/tilakverse-assets/releases/tag/sketchfab-star-wars) release, split into 8 MB parts, with a `SHA256SUMS` file.

These are **not CC0**. Each one keeps its author's licence, and the site credits every model it uses (`src/data/modelCredits.json` in the site repo).

| file | model | author | licence | rigged | clips | triangles | size |
| --- | --- | --- | --- | --- | --- | --- | --- |
| `b1-battle-droid.glb` | [B1 Battle Droid](https://sketchfab.com/3d-models/b1-battle-droid-star-wars-f0ca5d7dd5b64869907c6e781d7c660a) | [leoxx300](https://sketchfab.com/leoxx300) | CC BY 4.0 | yes, 53 joints | none | 20k | 33 MB |
| `at-at-walker.glb` | [Imperial AT-AT Walker](https://sketchfab.com/3d-models/imperial-at-at-walker-star-wars-7eab3f41da9143d8975b9034e91f8920) | [Quiznos323](https://sketchfab.com/quiznos323) | CC BY-NC-SA 4.0 | yes, 72 joints | Walk, Walk and shoot, Trip and fall | 74k | 69 MB (4K maps) |
| `at-at-walker-1k.glb` | the same AT-AT, 1K maps | Quiznos323 | CC BY-NC-SA 4.0 | yes, 72 joints | the same | 74k | 16 MB |
| `tie-fighter.glb` | [3D T.I.E Fighter](https://sketchfab.com/3d-models/3d-tie-fighter-star-wars-model-5375de94c2484ab0b2a2bd75aa63c2b4) | [Mickael Boitte](https://sketchfab.com/boittemike1) | CC BY 4.0 | no | none | 20k | 7 MB |
| `venator-clone-wars.glb` | [The Clone Wars: Venator Prefab](https://sketchfab.com/3d-models/star-wars-the-clone-wars-venator-prefab-8a1e1760391c4ac6a50373c2bf5efa2e) | [ShineyFX](https://sketchfab.com/ShineyFX) | CC BY 4.0 | no | none | 294k | 47 MB |
| `venator.glb` | [Venator Class Star Destroyer](https://sketchfab.com/3d-models/venator-class-star-destroyer-ff65cd3c27234615a3b68088f67e99e4) | [ForkyForklift](https://sketchfab.com/ForkyForklift) | CC BY 4.0 | no | none | 402k | 74 MB |

Left out on purpose: Heataker's [Imperial-class Star Destroyer](https://sketchfab.com/3d-models/star-wars-imperial-class-star-destroyer-fa18d537db4d4020a443c1802ec0f88e). Its licence is Sketchfab Standard, which allows use in the site but not re-hosting the file itself.

## Getting one

```
gh release download sketchfab-star-wars -R tilakpatell/tilakverse-assets -p 'venator.glb.part-*' -p SHA256SUMS
cat venator.glb.part-* > venator.glb && rm venator.glb.part-*
shasum -a 256 -c SHA256SUMS --ignore-missing
```

For the site, shrink a model with `scripts/sketchfab-import.mjs` in the site repo before it goes into `public/models/`.
