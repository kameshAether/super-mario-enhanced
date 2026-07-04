# Super Mario - Quick Start Guide

## Project Overview

This is a **browser-based HTML5 canvas platformer game** featuring procedurally generated pixel sprites, parallax scrolling, and enhanced graphics with enhanced gameplay mechanics.

**Technology:** Pure HTML5 + JavaScript (no build process required)
**File:** Single self-contained `index.html` (~34KB, 848 lines)

---

## How to Run

### Option 1: Direct Browser Open (Recommended)

Simply open `index.html` in any modern web browser:

**Methods:**
- Double-click the file
- Drag and drop into browser
- Right-click → "Open with" → Chrome/Firefox/Edge

### Option 2: Local HTTP Server (If features need it)

If you encounter CORS restrictions or want to test API features:

```bash
# Python 3
cd /root/data/projects/super-mario
python3 -m http.server 8000

# Then open: http://localhost:8000
```

**Note:** The game currently has no external dependencies, so direct browser open works fine.

---

## Controls

### Keyboard
- **Move Left:** Arrow Left or `A`
- **Move Right:** Arrow Right or `D`
- **Jump:** Space or `W`
- **Pause:** `P`

### Mobile (Touch)
- On-screen D-pad appears on screens <850px wide
- Left/Right arrows for movement
- "A" button for jump

---

## Game Features

### Visual Elements
- Procedurally generated pixel sprites (Mario, Goombas, Koopas, coins, etc.)
- 16-color retro palette
- Animated sprites (walk cycles, coin spin, flag wave)
- Parallax background with clouds and hills
- Flash overlay effects for power-ups and damage

### Audio System
- Web Audio API synthesizer (no external files)
- Sound effects: jump, coin, stomp, power-up, death, win, bump, break

### Gameplay Mechanics
- » Score, coins, lives, world tracking
- » Score popup effects
- » Dust and debris particle systems
- » Power-up mechanics (presumably from blocks)
- » Win/Game Over screens

### Enemy Types
- Goombas (2-frame animation)
- Koopas (2-frame animation)
- Basic AI movement

---

## Development History

Git commits show the project evolution:
1. **Initial commit** (`fe7896c`): Base platformer with parallax scrolling
2. **Enhancement commit** (`ccd59c7`): Added comprehensive gameplay polish
3. **Current** (`52b5583`): Merged enhanced graphics with gameplay polish

---

## Technical Notes

### Browser Compatibility
- Chrome/Edge (Chromium)
- Firefox
- Safari (iOS desktop)
- Mobile browsers (touch controls)

### Requirements
- JavaScript enabled
- Modern Web Audio API support
- Canvas 2D context
- Touch events (for mobile)

### No Dependencies
- No npm, no bundler, no frameworks
- No external images or audio files
- All assets generated procedurally in code
- Self-contained, zero network calls

---

## Troubleshooting

**Game won't load?**
- Check browser console (F12) for JS errors
- Ensure opening with modern browser (2020+)
- Try a local HTTP server if opening directly fails

**Audio not working?**
- Audio context initializes on first user interaction
- Click "START GAME" button to unlock audio
- Check system volume

**Controls not responding?**
- Wait for "START GAME" screen to appear
- Click the START button first (activates audio context)
- Verify keyboard focus is on the canvas

**Mobile controls missing?**
- Controls only appear on viewport width <850px
- Resize browser window smaller or use device emulator

---

## File Structure

```
super-mario/
├── .git/              # Version control
└── index.html         # Everything in one file!
```