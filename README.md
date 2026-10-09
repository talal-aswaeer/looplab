# Looplab v0.2

**[Open Looplab](https://talal-aswaeer.github.io/looplab/)** — use the tool directly in your browser.

Run `node server.js` and open http://127.0.0.1:4173. Run `node tests.mjs` for seed, scaling math, and ZIP checks. No runtime dependencies or build step.

## Animation

- Dots stay fixed and scale up/down. Random timing gives each dot a seeded phase; Linear sends a scaling wave horizontally, vertically, or diagonally; Together synchronizes the grid. Adjust minimum/maximum scale, wave bands, and speed.
- Lines and hash keep their Flow/Pulse motion.
- Wavy lines ripple along their length, with forward/reverse direction, wave amplitude, frequency, and speed.
- Flakes stay fixed and twinkle through grayscale intensity. Adjust speed and twinkle sharpness. Pure black-and-white output turns twinkles into binary visibility.

Speed uses whole cycles per loop; actual cycles per second is displayed. Integer cycles and spatial wave bands preserve looping and tiling. Changing loop duration changes speed.

## Workflow

Single-tile or repeated preview, play/pause, scrubbing, grid spacing, orientation, seeds, grayscale adjustments, two-pattern layering, JSON presets, and settings links. Each layer uses its pattern's motion. Still stops both layers.

PNG sequence exports support 512-4096 pixels, opaque grayscale or transparent masks. Transparent masks store intensity in alpha with black RGB. ZIP files contain frames starting at 0001, settings.json, and instructions. Frames sample phase i / frameCount; the duplicate endpoint is omitted.

Export retains encoded frames until ZIP download. The encoded sequence limit is 512 MB. Cancel stops after the current frame.

Validation: 45 rendering checks for fixed geometry, timing modes, speed, deterministic seeds, loop endpoints, orientation, layering, and binary values. A real browser export of 24 twinkle frames was verified for dimensions, numbering, ZIP CRCs, and settings.

Hash grid also offers Cross intersections: faint connectors with darker plus markers. Line and cross thickness, darkness, and cross size are independent controls.
