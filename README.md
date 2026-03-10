# History-cold-war-graph
# Cold War Tensions (1947–1991)

An interactive, single-file historical visualization that maps key Cold War events and a custom tension index from **1947 to 1991**.

## Overview

This project is a standalone HTML app (no build tools required) that combines:

- A cinematic, declassified-style UI
- A zoomable/pannable canvas timeline
- Event filtering by side, severity, era, and chapter
- A navigator mini-chart for fast range selection
- A detailed event card grid linked to timeline focus

## Features

- **Interactive main chart**
- Tension index line with glow + area fill
- Event nodes sized/styled by severity
- Dynamic labels at tighter zoom levels
- Background era bands and chapter highlights

- **Navigation and zoom**
- Mouse wheel zoom
- Drag to pan
- Touch pinch + drag support
- Navigator window drag/jump controls

- **Filtering**
- Side filters: `All`, `US`, `USSR`, `Critical`
- Era filters (e.g., Early Cold War, Détente, Endgame)
- Chapter filters (`Ch.1`, `Ch.2`, `Ch.3` + subchapters)
- Manual year range input

- **Event details**
- Tooltip on hover with date, description, score, and side
- Event cards with tension classification
- Click a card to auto-focus timeline around that event

## Tech Stack

- **HTML5**
- **CSS3** (custom variables, layered effects, responsive layout)
- **Vanilla JavaScript**
- **Canvas API** for charts
- **ResizeObserver** for responsive redraws
- Google Fonts: `Anton`, `DM Serif Display`, `DM Mono`

## Data Model

Events are defined in a single `EVENTS` array:

- `y`, `m`, `d`: date fields
- `t`: tension score (`0.0` to `10.0`)
- `label`: event name
- `desc`: event description
- `lv`: event level/severity (`1` to `6`)
- `side`: `US`, `USSR`, or `Both`

Derived fields are added at runtime (`dv`, `dateStr`, `dateShort`) for plotting and UI display.

## Run Locally

1. Save the file as `index.html`.
2. Open it in any modern browser (Chrome, Edge, Firefox, Safari).
3. No dependencies or server setup required.

## Controls Quick Reference

- **Zoom:** mouse wheel / toolbar (`+ In`, `− Out`)
- **Pan:** drag on main chart
- **Jump range:** use navigator bar or `Range` inputs
- **Inspect event:** hover a node
- **Focus event:** click an event card

## Customization

- Edit color theme in `:root` CSS variables.
- Add/remove historical events in the `EVENTS` array.
- Adjust chapter boundaries in `CHAPTERS`.
- Tune tension color bands in `tCol()`, `tLabel()`, and chart band config.

## Notes

- This is a handcrafted educational visualization, not an academic dataset pipeline.
- Tension scores are interpretive and intended for visual comparison, not strict quantitative analysis.
https://galen-pereira.github.io/History-cold-war-graph/
