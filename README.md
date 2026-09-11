# Starcatcher

[![Deploy to GitHub Pages](https://github.com/embmeals/starcatcher/actions/workflows/deploy.yml/badge.svg)](https://github.com/embmeals/starcatcher/actions/workflows/deploy.yml)

Fly a little cat alien around a night sky, collect every star and dodge the spike balls.

**Play it: https://starcatcher.emills.net** (also at https://embmeals.github.io/starcatcher/)

## Controls

- **WASD** or **arrow keys** — fly
- **Space** — up, **C** — down
- **V** — recenter the camera, **R** — restart

On a touchscreen the left thumb steers and the two right-hand buttons go up and down.

## This repository

The exported web build only — no game source. Every file here is generated, so
there is nothing to edit by hand.

The source is a separate private repository, `embmeals/starlight`, built with
Godot 4.7 and Blender models generated from Python.

## How a change reaches players

Merging to `master` in the source repo is the deploy. Nothing here is updated by
hand:

1. A merge to `starlight`'s `master` runs its **Export and deploy** workflow.
2. That exports the web build with Godot and pushes it here, to `main`.
3. GitHub Pages publishes `main` to the `github.io` address.
4. That same push runs **Update the Mac**, which pulls the new build onto the
   machine serving `starcatcher.emills.net` and checks it is really serving it.

Both live sites therefore serve the same commit. The badge above is green when
the last publish succeeded.

The Mac runs the job on its own self-hosted runner, so it connects outward and
nothing is exposed to the internet. `com.local.starcatcher-sync` still pulls
hourly as a fallback, for a push that lands while the Mac is asleep.

Editing files in this repository directly will work until the next source merge
overwrites them.
