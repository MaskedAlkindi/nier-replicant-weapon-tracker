# Grimoire of Blades — Nier Replicant Weapon Tracker

A single-file, offline weapon checklist for **NieR Replicant ver.1.22474487139...**, built for players working toward Endings C, D, and E — which require every one of the game's 33 weapons to be collected before finishing a third playthrough.

Spoiler-free: entries list only weapon names, how they're obtained, and general locations. No story events are described.

![status](https://img.shields.io/badge/spoilers-free-6b8f5a) ![type](https://img.shields.io/badge/type-single--file%20HTML-b08d3e)

## Features

- **All 33 weapons**, grouped by how you get them:
  - Story (automatic pickups)
  - Purchasable (weapon shops)
  - Found exploring (item boxes)
  - Sidequest rewards
  - 15 Nightmares / Route B arena rewards
- **Check off weapons** as you collect them, with a gold seal ring that fills in as your total climbs toward 33/33
- **Filters** for All / Missing / Owned, plus a category dropdown to narrow the list down (e.g. "just show me what I still need to buy")
- **Progress is saved automatically** in your browser via `localStorage` — close the tab, restart your browser, come back next week, your checklist is still there
- **Reset** button to wipe the checklist and start over (e.g. for a new save file)
- No build step, no dependencies to install, no server — it's one HTML file

## Getting started

1. Download `nier_replicant_weapon_grimoire.html`
2. Open it in any modern browser (double-click it, or drag it into a browser window)
3. Start checking off weapons as you find them

That's it — there's nothing to install or configure.

## Notes on data persistence

Progress is stored in your browser's `localStorage`, scoped to the file itself. Keep in mind:

- Your checklist is tied to **the browser and device** you use — it won't sync across different browsers or computers
- Clearing your browser's site data/cache for local files will also clear your checklist
- If you rename or move the file, your saved progress still applies (storage is keyed by an internal ID, not the filename)

## Weapon data

Weapon names, acquisition methods, and general locations were condensed from a public spoiler-free weapons guide and reorganized into a checklist format. All entries are written to avoid revealing story content.

## Tech

Plain HTML, CSS, and vanilla JavaScript. No frameworks, no build tools, no external JS dependencies. Fonts (Cinzel, EB Garamond) are loaded from Google Fonts.

## Contributing / customizing

Feel free to fork and adapt:
- Weapon data lives in the `WEAPONS` array near the top of the `<script>` block — each entry has `id`, `name`, `cat`, `act`, and `info` fields
- Categories and their display labels are defined in `CAT_LABELS` / `CAT_ORDER` just below the weapon list
- Colors, fonts, and layout are controlled by the CSS custom properties (`:root`) at the top of the `<style>` block

## License

No affiliation with Square Enix, Yoko Taro, or Toylogic/Square Enix's NieR Replicant. This is an unofficial fan-made companion tool. Use and adapt freely.
