<div align="center">

# 🚀 RetroSpaceInvaders

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![HTML5](https://img.shields.io/badge/HTML5-E34F26?logo=html5&logoColor=white)](https://developer.mozilla.org/en-US/docs/Web/HTML)
[![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?logo=javascript&logoColor=black)](https://developer.mozilla.org/en-US/docs/Web/JavaScript)
[![No Dependencies](https://img.shields.io/badge/dependencies-none-brightgreen)](game.html)
[![Single File](https://img.shields.io/badge/build-single%20file-blue)](game.html)

**A blazing-fast retro space shooter — open one file, start blasting.**

*Parallax stars. Synthesized SFX. Infinite waves. Pure vanilla JS.*

</div>

---

## ✨ Features

- **Zero setup** — a single `game.html` file; open it in any modern browser and play instantly
- **Three enemy types** — Grunts, Shooters, and armored Tanks, each with unique movement and attack patterns
- **Triple-shot player cannon** — spread fire that rewards aggressive play
- **Infinite wave system** — procedurally scaled waves keep difficulty climbing forever
- **Parallax star field** — multi-layer scrolling background for that classic arcade feel
- **Synthesized sound effects** — shoot, hit, explosion, and game-over cues via the Web Audio API (no audio files required for SFX)
- **Background music** — looping `music.mp3` plays automatically and is muted when the tab is hidden
- **Particle explosions** — satisfying burst effects on every kill
- **Hi-score persistence** — best score tracked per session
- **Fullscreen mode** — one keypress fills your entire screen
- **Retro CRT aesthetic** — monospace font, deep-space colour palette, pixel-perfect rendering

---

## 🎮 Controls

| Key | Action |
|-----|--------|
| `←` `→` `↑` `↓` / `W` `A` `S` `D` | Move ship |
| `Space` / `Z` | Fire |
| `F` | Toggle fullscreen |
| `Enter` | Start / restart |

---

## 🕹️ How to Play

1. **Download** — clone the repo or grab `game.html` (and `music.mp3` for background audio)
2. **Open** — double-click `game.html` or drag it into your browser — no server needed
3. **Survive** — destroy all enemies in each wave before they overrun you; you have **3 lives**
4. **Score** — Grunts are worth less, Shooters more, Tanks the most — prioritise accordingly
5. **Advance** — clear the wave to trigger the next one; enemies get faster and more numerous every round
6. **Die trying** — when all lives are gone the game is over; press Enter to go again and beat your hi-score

---

## 🛠️ Tech Stack

| Layer | Technology |
|-------|-----------|
| Rendering | HTML5 Canvas 2D API |
| Game logic | Vanilla JavaScript (ES6+) |
| Sound effects | Web Audio API (synthesized) |
| Background music | `<audio>` element + `music.mp3` |
| Styling | Inline CSS (no framework) |
| Build tool | *(none — zero-dependency single file)* |

---

## 📁 Project Structure

```
RetroSpaceInvaders/
├── game.html   ← entire game (HTML + CSS + JS)
└── music.mp3   ← background music track
```

---

## 🚀 Getting Started

```bash
git clone https://github.com/Hanno-du-Toit/RetroSpaceInvaders.git
cd RetroSpaceInvaders
# Open game.html in your browser — that's it!
```

Or just download `game.html` and `music.mp3` directly — no install, no build, no dependencies.

---

## 🤝 Contributing

Pull requests are welcome. For major changes, open an issue first to discuss what you'd like to change.

---

<div align="center">

Made with ☕ and a deep love for classic arcade games

*© 2026 Hanno du Toit*

</div>
