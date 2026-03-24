# Flying Bat Animation

A pure CSS pixel art bat animation — no images, no canvas, no JavaScript.

## Demo

Open `index.html` in any browser to see the bat flap its wings.

## How It Works

The entire bat is rendered using a **single 1×1px `<div>`** and CSS `box-shadow`.

| Technique | Purpose |
|---|---|
| `box-shadow` | Each shadow entry paints one pixel of the bat (blur=0 for sharp dots) |
| `transform: scale(4)` | Scales up 4× for a chunky pixel-art look |
| `@keyframes bat` | Two frames swap the full shadow map to animate wing flaps |
| `steps(1)` | Instant snap between frames — no easing, retro sprite-flip feel |
| `position: relative` + offsets | Re-centers the bat after scaling |

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
| `background` on `body` | CSS | Change page background color |
| `#222` in `box-shadow` | `@keyframes bat` | Change bat color |
| `transform: scale(4)` | `.bat` | Change bat size |
| `0.4s` in `animation` | `.bat` | Change flap speed |
