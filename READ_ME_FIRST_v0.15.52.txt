PRISMWILD v0.15.52 • STATUS DAMAGE PASS

CORE MERGE PATCH, NOT A FULL GAME BUILD.
Base: v0.15.51 Lottery Shuffle + Shop Dropdown patch.

Install:
1. Back up your current GitHub repository and save/export your important Admin content before replacing anything.
2. Extract this ZIP into the root of your working Prismwild site.
3. Replace ONLY index.html. Do not remove or replace your content/ folder, assets/ folder, or styles.css.
4. Commit/push through your normal GitHub Pages process and hard refresh.
5. Test Poison, Shock and Bleed with creatures at different levels.

IMPORTANT: If you manually modified index.html after applying v0.15.51, do not blindly overwrite those changes. Use STATUS_PASS_v0.15.51_TO_v0.15.52.diff to merge this patch into your customized file.

This patch does NOT intentionally reset localStorage, Admin content, monsters, Trial captains, Lottery pools or save data. It alters shared battle logic and Reference Guide text only.

Status tick rules:
- Poison: 10% of the affected monster's max HP at round end, minimum 1.
- Bleed: 10% of the ACTUAL damage the affected monster deals when its attack connects, rounded to nearest integer (minimum 1 for a successful hit). No damage on miss, evade or lost action. No round-end damage; original status duration still counts down at round end.
- Shock: flat 10 HP at round end. Existing speed reduction and 15% action loss remain.
- Burn: unchanged at 5% max HP at round end.
- Other status mechanics unchanged.
- All per-attack proc chances and X-turn durations remain unchanged.
- All battle modes use the same underlying status logic.

This was checked with JavaScript syntax validation and combat engine regression tests. Full browser UI acceptance testing was not available in this environment; please verify on your deployed game.
