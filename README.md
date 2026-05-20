# Mordashka

Все что связано с маской.

Remote face assets for Severin on the XiaoZhi ESP32 cube.

This repository is intentionally separate from `indila334-lab/xiaozhi-esp32` so the firmware repository does not become storage for heavy visual assets.

## Structure

```text
masters/neutral_source.gif   # original/source asset, can be heavy
cube/neutral.png             # first PNG test asset for the cube
cube/neutral.gif             # optimized GIF test asset for the cube
cube/manifest.json           # stable metadata and raw URLs
```

## Cube Asset Rules

- Canvas: 240x240.
- Portrait should visually occupy about 200x200.
- Each cube asset must stay under 250 KB.
- Target size: 100-150 KB where possible.
- GIF target: 6-8 FPS, short loop, 32/64 colors, remove near-duplicate frames.
- Masters may be larger; cube assets must be optimized.

## Firmware Rule

The firmware repo stores only metadata URLs and fallback local emoji files. Heavy faces live here.
