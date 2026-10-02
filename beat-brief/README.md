# Beat Brief — Production Prompt Generator

A single-file, dependency-free web app for generating music-production prompts for
**hip hop / rap** and **drum & bass**. Pick a genre, tempo, and key, then multi-select
ingredients across nine color-coded categories to assemble a copy-ready prompt — for
AI music tools (Suno/Udio) or as a brief for a producer.

## Features

- **Two genres** — Hip Hop / Rap and Drum & Bass, each with its own subgenres,
  tempo range, and ingredient palette.
- **Nine color-coded categories** — DAW, Drums, Bass, Melody, Vocals, Effects,
  Lyrics, Arrangement, and Mix & Master.
- **Multi-select throughout** — subgenres, mood / energy / era vibe groups, and every
  ingredient category.
- **Two output formats** — compact **Tags** (comma-separated) and prose **Brief**.
- **Negative prompt** — multi-select "avoid" chips plus a free-text field; kept as a
  separate block in the output.
- **Copy buttons everywhere** — per chip, per group, and for the whole prompt.
- **Save / share presets** — save named setups to the browser (`localStorage`), and
  share via an encoded link or code that others can import.
- **Theme-aware** (light/dark) and mobile-friendly.

## Usage

Open `index.html` in any modern browser — no build step, no dependencies, works
offline. It can also be served as a static page (e.g. GitHub Pages).

## Implementation notes

- Everything is inline in `index.html`: no external scripts, styles, or fonts.
- Presets are stored under the `localStorage` key `beatbrief.presets.v1`, with an
  in-memory fallback if storage is unavailable.
- Share codes are UTF-8-safe base64 of the app state, carried in the URL hash
  (`#p=…`) or as a standalone code.

The ingredient lists are representative, not exhaustive — production styles vary by
artist and era.
