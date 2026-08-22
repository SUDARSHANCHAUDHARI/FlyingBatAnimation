# Flying Bat Animation

A pure CSS pixel art bat animation — no images, no canvas, no JavaScript frameworks.

## Table of Contents

- [Demo](#demo)
- [Features](#features)
- [How It Works](#how-it-works)
- [Usage](#usage)
- [Customization](#customization)
- [License](#license)
- [About](#about)

## Demo

Open `index.html` in any browser.

## Features

- 6 bats flying right to left, scattered across the screen
- Wavy sine-wave flight paths for natural movement
- Night sky with full-screen CSS starfield and glowing moon
- Day / night toggle button (top-right corner)
- Smooth day sky gradient in day mode
- All pure CSS — no JavaScript except the day/night toggle button

## How It Works

The entire bat is rendered using a **single 1×1px `<div>`** and CSS `box-shadow`.

| Technique | Purpose |
|---|---|
| `box-shadow` | Each shadow entry paints one pixel of the bat (blur=0 for sharp dots) |
| `transform: scale()` | Scales up for a chunky pixel-art look |
| `@keyframes bat` | Two frames swap the full shadow map to animate wing flaps |
| `steps(1)` | Instant snap between frames — no easing, retro sprite-flip feel |
| `@keyframes fly` | Moves bats from right to left across the screen |
| `@keyframes sineWave` | Oscillates `margin-top` for wavy flight path |
| `nth-child(4..9)` | Each bat gets its own size, position, and timing (offset by 3 for stars/stars2/moon divs) |

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
| `background` on `body.day` | CSS | Change day sky gradient |
| `#222` in `box-shadow` | `@keyframes bat` | Change bat color |
| `transform: scale()` | `.bat:nth-child()` | Change individual bat size |
| `0.4s` in `animation` | `.bat` | Change flap speed |
| `12s` in `animation` | `.bat` | Change flight speed across screen |
| `top` | `.bat:nth-child()` | Change vertical position of each bat |


## License

MIT — see [LICENSE](LICENSE).

---

## About

I'm Sudarshan Chaudhari, a Senior Quality Engineer, Test Automation specialist, and AI systems builder based in Bangkok, Thailand.

I have 13+ years of experience in software quality engineering, working across SaaS, fintech, gaming, web, mobile, cloud, and digital signage platforms. My background combines hands-on test automation with QA leadership, test strategy, CI/CD, release quality, production investigation, and cross-platform validation.

Alongside my professional QA career, I run [SudarshanTechLabs](https://sudarshantechlabs.com/), my independent engineering and product lab where I design, build, test, and ship software across Android, web, AI, cybersecurity, developer tooling, and cross-platform applications.

### What I work on

- ⚙️ **Quality Engineering & Test Automation** — Playwright, Selenium, Cypress, Appium, API testing, automation frameworks, end-to-end testing, CI/CD, release gates, GitHub Actions, risk-based testing, and production validation
- 🤖 **AI Systems & Automation** — AI agents, multi-agent orchestration, MCP servers, AI-assisted QA, prompt tooling, developer workflows, automation systems, and Claude Code plugins
- 📱 **Mobile & Cross-Platform Applications** — Android applications built with Kotlin and Jetpack Compose, Google Play releases, automated build and publishing pipelines, and cross-platform development spanning iOS, web, Windows, and macOS
- 🌐 **Web Applications & Platforms** — Full-stack applications using Next.js, TypeScript, Firebase, Cloudflare, REST APIs, and modern web infrastructure
- 🛠️ **Developer Tooling & CLI Engineering** — Rust, Python, TypeScript, CLI utilities, multi-repository tooling, build automation, release tooling, and engineering productivity systems
- 🛡️ **Cybersecurity & Observability** — Threat detection, log analysis, security auditing, vulnerability assessment, monitoring, and security-focused developer tools
- 📺 **Digital Signage & Device Platforms** — Content validation, playback testing, device compatibility, production investigation, monitoring, and QA across diverse hardware and operating-system environments

My work sits at the intersection of quality engineering, automation, AI, and software development. I approach products with a QA mindset from the beginning: understanding failure modes, designing for testability, automating repetitive work, and building release confidence into the engineering process.

Through SudarshanTechLabs, I also build products and tools from idea to production, covering architecture, development, testing, CI/CD, release automation, monitoring, and ongoing maintenance.

🌐 [sudarshantechlabs.com](https://sudarshantechlabs.com/) · 💼 [LinkedIn](https://linkedin.com/in/sudarshan-chaudhari) · 🐙 [GitHub](https://github.com/SUDARSHANCHAUDHARI) · ✉️ [sunny.sudarshan@gmail.com](mailto:sunny.sudarshan@gmail.com)
