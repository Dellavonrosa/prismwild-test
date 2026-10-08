PRISMWILD v0.15.55 • MYTHIC TEMPLE UPDATE
=======================================

INSTALL
- Merge this ZIP into your EXISTING v0.15.54 Prismwild repository root.
- Replace index.html only. Keep your content/ folder, assets/, styles.css, and other files intact.
- If you have edited index.html since v0.15.54, use the included unified diff to merge instead of overwriting those changes.
- Commit and Push the code change normally.

MYTHIC TEMPLE RULES
- Regular Explore maze only (NOT the Halloween or other event mazes).
- On each new maze generation: 1% chance on the first maze of a run.
- Every maze fully revealed and completed increases the chance by 3 percentage points, capped at 100%.
- At most ONE temple cell in any single maze, reachable via the generated maze paths.
- Reveals with normal fog; the player must step on the 🏛 square to trigger one Mythic battle.
- A revealed but unvisited temple delays regeneration even when all maze tiles are revealed.
- The temple triggers at most once per maze, including after a win, loss, or flee.
- The next maze's temple chance resets to 1% after triggering a temple.
- Ending Explore, leaving its page, fainting, or reloading resets the streak.
- A Mythic encounter uses the existing battle, capture, and reward rules.

ADMIN • MONSTER EDITOR
- Set the monster's Rarity to Mythic.
- Keep Crossbreed unchecked.
- Enable the new 'Mythic Temple Only' checkbox under Obtaining & Breeding.
- Save the monster. If custom, also enable 'Include in Live Content export'.
- Export Live Content and merge/push that package for hosted players to see updated monsters.
- The temple pool selects ONLY published, non-Crossbreed Mythics explicitly marked Temple Only.
- Mythic Temple Only species do not appear in the ordinary wild Explore or wild-egg pool.
- If no published Temple-only Mythics exist, no temples generate (no dead-end tiles).

TESTING
- Pick a published Mythic (not a Crossbreed) and mark it Mythic Temple Only.
- Begin normal Explore. The current/next maze chance appears under the maze controls.
- Temple tiles appear as 🏛 after their location becomes revealed.
- At 1% base chance the temple can take many mazes to appear naturally.
- Tests passed: syntax, pool selection, chance progression/cap, one tile max, encounter startup, one-shot temple, admin toggling, and next-maze reset.
- Full-browser acceptance was blocked by this environment; please verify the live UI after installing.

No player save reset required. No assets or sprites modified.
