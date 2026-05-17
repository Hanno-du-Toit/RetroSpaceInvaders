# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project

**RetroSpaceInvaders** — single-file browser shooting game. Vanilla HTML/CSS/JS, no frameworks. Background music loaded from `music.mp3` (local file).

## Running

Open `game.html` directly in a browser. No build step, no server required.

## Architecture

Everything lives in `game.html`. The script section is organized as:

- **Constants** — speeds, cooldowns, counts
- **State** — `state` (`menu` | `playing` | `dead` | `gameover`), `score`, `lives`, `wave`, `frame`
- **Input** — `keys` map updated by `keydown`/`keyup`; read via `keyPressed(code)`
- **Background music** — `<audio id="bgm">` pointing to `music.mp3`; `ytPlay()` / `ytPause()` control playback
- **SFX** — Web Audio API synthesized sounds: `sfxShoot`, `sfxEnemyHit`, `sfxEnemyExplode`, `sfxPlayerHit`, `sfxGameOver`
- **Stars** — parallax background array, updated every frame
- **Player** — singleton object with `update()` / `draw()` / `reset()`; fires triple-shot player bullets
- **Bullet** — class used for both player and enemy projectiles; `dead` flag for removal
- **Particles** — plain array of particle objects; spawned by `spawnExplosion()`
- **Enemy** — class with three types (`grunt`, `shooter`, `tank`), each with distinct movement pattern and HP; `hit()` method handles damage and scoring
- **Wave spawning** — `buildWave(w)` generates a `spawnQueue`; `spawnWaveEnemies()` drains the queue each frame with per-enemy delays; next wave triggers automatically when `enemies` and `spawnQueue` are both empty
- **Collision** — AABB via `rectsOverlap()`; player bullets vs enemies, enemy bullets vs player, enemy contact vs player
- **HUD** — score, wave, hi-score, lives drawn directly on canvas each frame
- **Game loop** — `requestAnimationFrame` → `update()` then `draw()`; state machine drives which logic runs

## Controls

| Key | Action |
|-----|--------|
| Arrow keys / WASD | Move |
| Space / Z | Shoot |
| F | Toggle fullscreen |
