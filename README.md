# Unicode Forge

**Turn images, videos and GIFs into Unicode character art — right in your browser.**

### 👉 [Try the app](https://ndscplnt.github.io/unicode-forge/)

> 🚧 **The source code will be publicly available soon.**
>
> This repository only holds the published build of the site (`gh-pages` branch). It is generated
> automatically on every update of the app, so it should not be edited by hand.

---

## What it does

Each cell of the grid picks the glyph that best matches its **shape, ink distribution and edge
direction**, not just its brightness like classic ASCII art. Everything runs on your device: no file is
ever uploaded to a server.

### 🖼️ Images
- Open or drag in PNG, JPEG, WebP, GIF, BMP, AVIF or SVG files, or start from one of 10 public-domain
  samples (Hokusai, Van Gogh, Vermeer, Klimt, NASA photos…).
- Tune the tone: contrast, brightness, gamma, sharpness, clarity, antialiasing, outlines, glitch,
  automatic levels and automatic adjustment.
- Choose the characters: base sets, classics (ASCII ramp, blocks, box drawing, braille), world scripts,
  ready-made combinations, or your own sets picked from the Unicode catalogue.
- Pick a matching strategy (Balanced, Tone, Shape, Edges, Texture), font, grid and colours (themes,
  colour from the image, solid, gradient or transparent background).

### ✏️ Manual editing
- Click a cell to inspect its glyph, change it, clear it or recolour it — with undo and redo.
- Saved presets, Result / Split / Original preview, zoom and pan.

### 🎞️ Video and GIF
- Open an MP4, WebM or MOV video or an animated GIF, or one of 6 public-domain samples (Muybridge's
  horses and bison, the Earth and an aurora from the International Space Station, the Sun, waves).
- Player with range selection, frame-by-frame stepping, 0.25×–2× speed and loop.
- Cell edits apply to the current frame or to the whole clip.
- Export to MP4 (H.264) or WebM (VP9/VP8) keeping the original audio, or to GIF.

### 🔤 Unicode catalogue
- Browse 94,713 characters from planes 0 and 1 in 28 groups, with search and a detail card for every
  character.

### 🧩 Your own sets
- Edit a copy of any set and save it among your own sets.
- Build your own groups of sets, personal ones included, and switch between them with one click.
- Exclude characters you never want to see, whatever set they come from.
- Don't like a glyph? Let the engine pick the next most similar one, or choose the replacement yourself: it goes
  where it still fits the image, or everywhere if you force it.
- Turn on *variety* if you like: where several glyphs fit equally well they alternate, while flat areas stay clean.

### 📤 Export
PNG · JPEG · WebP · SVG (real text) · coloured HTML · plain TXT · copy as text · MP4 · WebM · GIF.

### 🌍 And more
- Interface in Italian and English.
- Phone-friendly layout with a tabbed panel.
- Full configuration (settings, sets and presets) can be downloaded and re-loaded as JSON.

## Requirements

A recent browser (up-to-date Chrome, Edge or Safari). Rendering runs in a Web Worker with
OffscreenCanvas, video export uses WebCodecs and animated GIFs are decoded with ImageDecoder.

## How it is built

The app is a Vite + React + TypeScript single-page app, powered by the **Unicode Forge engine**: a pure
TypeScript glyph-matching engine that runs unchanged in Node and in the browser.
