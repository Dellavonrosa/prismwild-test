PRISMWILD v0.15.53 — SPRITE EDITOR ITEM COVERAGE

INSTALL:
1. Start with your working v0.15.52 Prismwild repository.
2. Back up index.html and your browser Admin data export.
3. Extract this ZIP into the repository root, overwriting ONLY index.html.
4. Retain your existing styles.css, content/prismwild-content.js, and asset folders.
5. If you have modified index.html since v0.15.52, merge the included diff instead of overwriting.
6. In Admin -> Sprite Workshop, search for a previously missing item (e.g. DNA Splicer, Lottery Coin, Potential Injector P8).
7. Upload a PNG, save it, verify it appears in Shop/Inventory, then Export Live Package to include it in your published assets.

FIXED:
- Sprite Workshop now auto-enumerates all ITEM_SHOP items as individual replaceable art slots.
- All Expedition Treasure items and both Lottery items gain slots; Winter Mystery Egg too.
- Each item uses its old icon or existing shared uploaded sprite as the fallback until its own art is uploaded.
- Dedicated slots show up in Inventory, Shop, event calendars and event reward displays.
- Lottery Egg icon also applies to incubating Lottery Egg rewards.
- Preserves all previously uploaded sprite overrides, status-pass code, Lottery, existing content, and every shop reward.

NOTES:
- Sprite Workshop remains for NON-monster artwork. Per-monster base/prismatic/egg assets belong in Monster Editor.
- A shared icon (e.g. the old Greater Injector art) still appears until a dedicated item image is supplied.
- Generic Attack Scroll remains a shared sprite across all named Scroll items.
