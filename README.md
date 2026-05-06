# Memory Orb

A 3D constellation of memories. A calm, ambient second brain shaped like a glass sphere.

Leave a thought, photo, place, or song. Each memory becomes a star inside the orb. The orb finds connections between your memories automatically and links the related ones with gossamer lines. When you ask it to find patterns, it surfaces the recurring threads as glowing constellations on the sky.

## Live demo

Visit [https://madisonzhan.github.io/memory-orb/](https://madisonzhan.github.io/memory-orb/) (after enabling GitHub Pages in repo settings → Pages → deploy from main branch).

Or open `index.html` directly in any modern browser.

## Features

- **3D constellation orb** rendered on canvas, drag/scroll to rotate, pinch to zoom
- **Rich memories** — text, photo, place, song link
- **Automatic context web** built from semantic similarity between memory texts
- **Pattern analysis** powered by Claude — surfaces recurring threads and draws them as constellations
- **Dreamy heaven landscape** with iridescent color regions inside the orb
- **Light + dark mode** — pastel sky or starry void
- **Local-first** — all memories stored in your browser via localStorage; export/import as JSON

## Stack

Single self-contained HTML file. No build step, no dependencies, no server. Just open and use.

- Vanilla JavaScript
- Canvas 2D for the 3D rendering (custom hand-rolled projection — no Three.js)
- localStorage for persistence
- (Optional) Cowork's `askClaude` for pattern analysis when running inside Cowork

## Controls

- **Drag** or **scroll** — rotate the orb
- **Pinch** (trackpad) — zoom in and out
- **Click a star** — orb spins to bring it to the front, opens its detail
- **Find patterns** — Claude reads across your memories and draws constellations

## Built with

[Cowork](https://anthropic.com), Anthropic's desktop tool for non-developers to automate file and task management.
