# Flying Bat Animation

A pure CSS pixel art bat animation — no images, no canvas, no JavaScript.

## Demo

Open `index.html` in any browser. Click anywhere to toggle day/night mode.

## Features

- 6 bats flying right to left, scattered across the screen
- Night sky with CSS starfield and glowing moon
- Click to toggle day / night mode
- All pure CSS — no JavaScript except the day/night toggle

## How It Works

The entire bat is rendered using a **single 1×1px `<div>`** and CSS `box-shadow`.

| Technique | Purpose |
|---|---|
| `box-shadow` | Each shadow entry paints one pixel of the bat (blur=0 for sharp dots) |
| `transform: scale()` | Scales up for a chunky pixel-art look |
| `@keyframes bat` | Two frames swap the full shadow map to animate wing flaps |
| `steps(1)` | Instant snap between frames — no easing, retro sprite-flip feel |
| `@keyframes fly` | Moves bats from right to left across the screen |
| `nth-child(3..8)` | Each bat gets its own size, position, and timing (offset by 2 for stars/moon divs) |

### Animation Frames

- **Frame 1 (0%)** — wings spread wide
- **Frame 2 (50%)** — wings folded down
- Loops back to Frame 1 seamlessly at 0.4s per cycle

## Usage

```bash
# Clone the repo
git clone https://github.com/SUDARSHANCHAUDHARI/FlyingBatAnimation.git

# Open in browser
open index.html
```

No build steps, no dependencies — just open the file.

## Customization

| Property | Location | Effect |
|---|---|---|
| `background` on `body` | CSS | Change night sky color |
| `#222` in `box-shadow` | `@keyframes bat` | Change bat color |
| `transform: scale()` | `.bat:nth-child()` | Change individual bat size |
| `0.4s` in `animation` | `.bat` | Change flap speed |
| `12s` in `animation` | `.bat` | Change flight speed across screen |
| `top` | `.bat:nth-child()` | Change vertical position of each bat |
