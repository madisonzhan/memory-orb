# Memory Orb

A 3D constellation of memories. A calm, ambient second brain shaped like a glass sphere.

Leave a thought, photo, place, or song. Each memory becomes a star inside the orb. Real constellation patterns (Big Dipper, Orion, Cassiopeia, and a dozen others) float across three depths. As you save more, the orb finds threads of similarity and draws them as gossamer lines between stars. Ask it to find patterns and it surfaces the recurring themes as glowing constellations on the sky.

## Live demo

**[madisonzhan.github.io/memory-orb](https://madisonzhan.github.io/memory-orb/)**

Open it in any modern browser. No sign-in, no server, no tracking. Your memories live in your own browser's localStorage.

## What it does

- **3D constellation orb** rendered on canvas — drag or scroll to rotate, pinch to zoom, click any star to spin it to the front
- **Real constellation patterns** at three depths: 14 canonical figures (Big Dipper, Orion, Cassiopeia, Cygnus, Lyra, Crux, Pegasus, Scorpius, Leo, Aquila, Ursa Minor, Sagittarius, Bootes, Gemini), each placed at a random orientation across outer, mid, and inner shells, plus 120+ field stars
- **Memories with depth** — each holds text, an optional photo, a place, and a song link
- **Automatic context web** computed from semantic similarity between memory texts; related memories are linked with soft hue-blended lines
- **Pattern analysis** powered by Claude — surfaces 3-5 recurring themes across your memories and draws them as glowing constellations on the sky, with names and observations
- **Constellation tour** — click "constellations" to cycle through every named figure with smooth camera spins
- **Custom palettes** — 7 built-in themes (Maddy, Ember, Ocean, Forest, Twilight, Sunset, Frost) plus a Custom mode with 7 hue sliders
- **Ambient mode** — hides all UI for a screensaver-style breathing orb
- **Intro animation** — every load opens with a slow zoom-in spin
- **Live aura** — a swirling iridescent background that follows your camera motion
- **Soft sliders** for halo radius and aura size
- **Local-first** — everything stored in your browser; export/import as JSON

## Controls

| Action | Result |
| --- | --- |
| Drag or scroll | Rotate the sky |
| Pinch (trackpad) | Zoom in or out |
| Click a star | Spin it to the front, show its memory |
| Click empty space | Dismiss the floating memory |
| `Esc` | Close any open panel |
| `←` `→` (in constellation mode) | Cycle through constellations |
| `/` | Open the browse panel |

## Stack

A single self-contained HTML file. No build step, no dependencies, no framework, no server.

- Vanilla JavaScript
- Custom 3D engine on Canvas 2D (hand-rolled perspective projection — no Three.js)
- localStorage for persistence
- Optional: Cowork's `askClaude` for pattern analysis when running inside [Cowork](https://anthropic.com)

## Run locally

Just open `index.html` (or `memory-orb.html`) in any modern browser. There's nothing to install.

```bash
git clone https://github.com/madisonzhan/memory-orb.git
cd memory-orb
open index.html       # macOS
xdg-open index.html   # linux
start index.html      # windows
```

## Privacy

Everything is local. Your memories live in your browser's localStorage and never leave your device. There's no analytics, no telemetry, no server. The "find patterns" feature only works when running inside Cowork (which runs Claude inference locally on your behalf); on the public site, it falls back to a lightweight word-frequency analysis.

## Built with

[Cowork](https://anthropic.com) — Anthropic's desktop tool for non-developers to automate file and task management.

## License

MIT — see [LICENSE](LICENSE).
