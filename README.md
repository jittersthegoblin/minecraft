# The Linggango Field Guide

A readable, swipeable item book for Rina’s Linggango installation. Open `dist/index.html` in a browser, or serve the `dist` folder with any static web host. It needs no account, database, or Minecraft connection. The optional web fonts fall back to local fonts when offline.

## What works

- One item per book spread, with plain-language explanations and usage notes.
- Touch swipes, previous/next buttons, and keyboard arrow navigation.
- Search by item name, mod, description, or exact item ID.
- Chapter and mod filters, plus a detailed-explanations-only filter.
- Item-specific links in the URL, source notes, and pack-specific warnings.
- Responsive layouts for desktop and phones.

## Coverage — an honest first edition

The catalogue contains all **25,143 unique IDs in the existing September 2, 2026 export**, not a freshly verified live registry. The installation manifest says **Linggango V6.6.4hotfix**, Minecraft 1.20.1, Forge 47.4.20.

This edition contains **122 detailed entries**, **6,583 general item-type descriptions**, and **18,438 entries awaiting reliable behavior research**. The full catalogue is searchable, but the encyclopedia is not fully explained yet. General descriptions are explicitly marked and must not be treated as verification of a mod’s unique effects. Some detailed entries also identify specific stats or mechanics that remain unverified.

The detailed selection includes Artifacts accessories, Sophisticated Backpacks upgrades, Ars Nouveau starter devices, Enigmatic equipment, and Linggango-specific items and warnings. Explanations use local language files, bundled guidebooks, and KubeJS scripts. A recipe found inside a mod is not automatically the final recipe used by Linggango or a multiplayer server.

## Files

- `dist/index.html`, `style.css`, and `app.js`: the static book interface.
- `dist/data.js`: the full catalogue and written explanations.
- `dist/items.png`: an atlas of 10,060 available flat item pictures. These are not rendered 3D block models.
- `catalogue.json`: the same catalogue in a reusable data format.
- `.openai/hosting.json`: the private Sites deployment configuration; no credentials.

## Updating the book

Each catalogue entry includes `id`, `name`, `mod`, `category`, `status`, `summary`, `use`, `obtain`, `warning`, and `sources`. Optional fields are `icon` and `packNote`. Status is `detailed`, `general`, or `pending`. Keep uncertainty visible. Do not turn a guessed item name or a recipe ingredient into an invented gameplay effect.

After changing the catalogue, keep `catalogue.json` and the object assigned to `window.BOOK` in `dist/data.js` aligned. The atlas uses 32-pixel tiles in 128 columns; `icon` is the zero-based tile index.

## Credits

Minecraft and the respective mod names and item artwork belong to their creators. This is an unofficial personal reference guide. Explanations are paraphrased; original mod JARs, full guidebook text, world saves, logs, account information, and game configuration files are not included. Local source paths in entries are evidence references, not bundled copies of those files.
