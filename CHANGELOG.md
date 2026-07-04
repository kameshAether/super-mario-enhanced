# CHANGELOG

All notable changes to `index.html` are documented here.
The format is based on [Keep a Changelog](https://keepachangelog.com/).

---

## [0.3.0] — 2025-07-04 — Polish Release

### Added
- **Orbitron font** — Google Fonts CDN link for the futuristic arcade lettering throughout the UI.
- **Sound-toggle button** — 🔊/🔇 circular button (top-right of the game container) to mute/unmute SFX.
- **Keyboard sound toggle** — press `M` while playing to toggle sound on/off.
- **Keyboard restart from Game Over** — press `Space` or `Enter` on the Game Over screen to restart immediately without clicking.

### Changed
- **UI font-family** updated from `Arial, sans-serif` → `'Orbitron', Arial, sans-serif` for a sci-fi arcade aesthetic.
- **Pause screen** replaced the old inline-style overlay with a proper `.screen` class-based overlay (matches title/win/game-over styling and includes a RESUME button).
- **Flash rendering** simplified — removes the separate `flashOverlay` canvas and `flashCtx` context. Flash effects now render directly on the main `canvas` via `ctx.setTransform()` / `ctx.fillRect()`, removing an entire off-screen canvas from the render path.
- **Canvas resize handling** — new `fitCanvas()` function constrains the game canvas to `min(window.innerWidth - 40, 800)` px; called on window resize and each `startGame()`.
- **Input routing** — Space/Enter gameover restart handler placed *before* the jump logic in `keydown`, so gameover always takes priority.

### Removed
- Deleted the orphan `<canvas id="flashOverlay">` HTML element and its `#flashOverlay` CSS block (flash is now drawn on the main canvas).

---

## [0.2.0] — prior — Enhanced Graphics & UI Polish

From commit `ccd59c7` — *Add comprehensive gameplay and UI polish* and `52b5583` — *Merge enhanced graphics with base gameplay*.

- Merged enhanced pixel-art graphics with core gameplay loop.
- Added parallax scrolling (clouds + hills).
- Particle system (sparkles, dust, debris, floating score pop-ups).
- Screen-shake & hit-stop on stomp/block-hit.
- Expanded HUD (score, coins, world, lives) with retro styling.
- Question blocks, brick blocks, coin blocks, and mushroom power-ups.
- Multiple enemy types + behavior (Goomba/Koopa patrol + turn-around).
- Coyote time and jump-buffer for responsive platformer feel.
- Mobile touch controls (d-pad + jump button).

---

## [0.1.0] — prior — Initial Commit

From commit `fe7896c` — *Initial commit: Super Mario Platformer with parallax scrolling, enemies, and classic gameplay*.

- First playable version: canvas setup, sprite generation, level layout, physics, collision, enemies, coins, flagpole win condition, Web Audio SFX, and start/game-over/win/pause screens.
