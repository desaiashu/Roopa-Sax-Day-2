# Roopa + Sax Day 2

A [Songbird](https://tivra.com) project.

| | |
|---|---|
| Tempo | 120 BPM |
| Meter | 4/4 |
| Tracks | 8 |
| Clips | 15 |
| Plugins | 24 |
| Automation lanes | 0 |

## Tracks

- Roopa 04
- Backing 04
- Roopa 05
- Backing 05
- Hall
- Plate
- Delay
- Color

## Layout

- `Roopa-Sax-Day-2.bird` — arrangement & musical intent, human-readable.
- `entities/` — content keyed by stable id (clips, plugins, automation, channels). Each file stays whole until it grows large, then transparently shards into `entities/<type>/NN.json` so merges stay size-independent.
- `views/` — projections that place entities (arrangement rows, mixer bus). New views (palette, session) are added here without touching content.
- `state/` — global project state (transport, settings, sections, …).
- `samples/` & `visuals/` — media payloads, stored in R2 (see `manifest.json`).
