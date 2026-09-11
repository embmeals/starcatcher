# Starcatcher

[![Deploy to GitHub Pages](https://github.com/embmeals/starcatcher/actions/workflows/deploy.yml/badge.svg)](https://github.com/embmeals/starcatcher/actions/workflows/deploy.yml)

Fly as a little cat alien around a night sky collecting stars and dodging spiked balls.

**Play it: https://embmeals.github.io/starcatcher/**

## About this repository

This holds the exported web build only — no game source. The source lives in a
separate private repository (`starlight`), and the build here is refreshed by
re-exporting from it.

Every push to `main` redeploys the site. The badge above is green when the live
site matches `main`.

## Controls

- **WASD / arrow keys** — fly
- **Space** — up, **C** — down
- **V** — recenter, **R** — restart

On touch devices, the left thumb flies and the right buttons go up and down.

Built with Godot 4.7, models generated in Blender from Python.
