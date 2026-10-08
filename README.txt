PRISMWILD PROTOTYPE v0.15.49

See READ_ME_FIRST_v0.15.49.txt and PATCH_NOTES_v0.15.49.txt for the current checkpoint.

HISTORIC NOTES FOLLOW
---------------------
PRISMWILD PROTOTYPE v0.15.44



V0.15.44 — DAILY ZONE WALLPAPERS
- Fixed daily region artwork behind the scrolling UI.
- Zone-specific ambient VFX and local-midnight crossfade.
- Seven backgrounds cover Monday through Sunday, including Chaos Wastes.

V0.15.43 — INVENTORY SELLING + RECOVERY ITEMS
- Added Medium Healing Gel (650 currency): restores 50% maximum Vitality in battle.
- Added Life Crystal (2500 currency): fully restores Vitality in battle.
- Inventory now uses click-to-inspect item details with consumable status and quantity-based selling.
- Shop merchandise and Attack Scrolls resell for 5% of shop value, rounded down; Field Finds keep their native trade values.
- Existing saves remain compatible and Live Content packaging is unchanged.

V0.15.42 — SILVERWIND REFERENCE DESK
- Added Silverwind's searchable Reference Guide covering core mechanics, monsters, battle, fieldwork, progression, events, Trials, items, and economy.
- Expanded authored Silverwind dialogue from 16 to 44 lines, including newer monsters and seasonal chatter.
- Keeper's Desk can now react to ready Expeditions, owned Prismatics, owned Crossbreeds, and cleared Trials.
- Live Content schema remains v9; published art remains external under assets/live/.

V0.15.41 — GITHUB-SAFE LIVE ASSET PACKAGING
- Live Content images are stored as normal files under assets/live instead of giant Base64 strings inside prismwild-content.js.
- Export Live Content is now Export Live Package and downloads prismwild-live-content.zip.
- Extract that ZIP into the GitHub repository root before Commit + Push.
- This prevents content/prismwild-content.js from crossing GitHub's 100 MB single-file limit as the custom roster grows.
- Existing Admin Data backups still embed art for portable local backup/import.

V0.15.40 — FIRE TRIAL + WORKSHOP CONTENT PACK
- Added Dell's latest authored Live Content export.
- Added Flamecoil as the finalized Kilnslug x Aeralith Fire/Air Crossbreed, including Base + Prismatic art.
- Updated Thermal Spiral to use Flamecoil's final name.
- Updated the Magma Trial lineup to use Flamecoil as Razzik's ace.
- Completed Razzik's Hard intro and Captain lore fields; corrected the Flame Jewel Badge label.
- Latest content now includes 22 custom species, 22 custom attacks, 2 Trials, and both Captain asset sets.
- Added the v0.15.40 News post summarizing Monster Census improvements, Battle FX, Trial Captains, new Air monsters, Flamecoil, and the dynamic Haunted Maze fix.
- v0.15.39's dynamic Halloween Maze encounter logic remains intact.


V0.15.39 — DYNAMIC HALLOWEEN MAZE ENCOUNTERS
- Haunted Maze encounters now build their monster pool automatically from the species registry.
- Any published, non-Crossbreed species with Obtain Method set to "Halloween Maze Encounter" is eligible without a code change.
- Grievwing now joins the Haunted Maze encounter pool automatically from its authored species data.
- Existing per-species maze weights remain supported; unlisted tagged species use the standard default weight of 40.
- The Maze screen's registered-monster count now reflects the live dynamic pool instead of the old hard-coded list.
- The previous hard-coded eventSpecies list remains only as a backwards-compatible fallback if no tagged species are available.

V0.15.38 — ROSWYN + TRIAL CAPTAIN PERSONALITY UPDATE
- Roswyn Cloverhoof is now the Nature Trial Captain, with her new full-body pixel-art Captain asset.
- Nature Trial lineup preserved from Dell's current authored content: Thornjack, Bloomreign, then Wraithwood.
- Trial Captains now support separate talk, Normal intro, Hard intro, victory, defeat, lore, and Trial philosophy text.
- Trial pages display Captain philosophy and lore while keeping the click-to-talk interaction.
- The first Trial battle now opens with the Captain's Normal or Hard challenge line in the battle log.
- Trial victory and defeat result screens can show Captain-specific dialogue.
- Trial Workshop now exposes all new Captain dialogue/lore fields for future Trial Captains.
- Updated to Dell's current Live Content pack with 21 custom species and 20 custom attacks.
- Roswyn's authored Live Content data and Captain art are included in content/prismwild-content.js.

V0.15.37 — BATTLE ATTACK VISUAL FX
- Added reusable combat FX families: Bite, Slash, Slam, Projectile, Burst, Beam, and Wave.
- Attack Workshop now includes a Visual FX selector with Auto inference or explicit family overrides.
- All existing built-in attacks and the current published custom attacks have hand-tuned automatic FX family mappings.
- Light / Standard / Heavy attack styles now affect visual scale and impact weight.
- Elements use distinct effect palettes and particle shapes rather than simple one-color recolors.
- Heavy successful attacks add a small battlefield kick; misses visibly whiff or veer away.
- Attack Registry and live preview display the resolved FX family.
- Custom Visual FX selections are preserved through normal Live Content export/import.
- v0.15.37 originally preserved the authored prismwild-content.js from that build's supplied content file.


V0.15.36 — MONSTER CENSUS + ADMIN ROSTER FILTERS
- Monster Workshop now includes a live Monster Census for the entire registered roster.
- Census shows Total, Custom, Crossbreed, and Mythic counts.
- Element counts can switch between Primary only and Contains element, so Crossbreed secondary Elements can be included in roster planning.
- Clicking an Element count filters the registry to that Element; click it again to clear it.
- Added Battle Type filters for Speed, Brute, and Defender.
- Added roster filters for Base Monsters, Crossbreeds, Built-in, Custom, Published Custom, Draft Custom, and Mythic.
- Added sorting by Name, Element, Battle Type, and P1 BST ascending/descending.
- Registry search now also matches Element, secondary Element, Battle Type, and role/description.
- Clear button resets registry filters/search while leaving the chosen census counting mode available for planning.
- Current authored prismwild-content.js was preserved exactly from Dell's supplied current content file.


V0.15.18 — LEGACY ADMIN SAVE + INLINE EXPLORE FINDS
- Fixed an upgrade-compatibility bug that could silently block Save Monster for existing non-Crossbreed custom species.
- Crossbreed-only form controls are now disabled while hidden, so legacy chance=0 values cannot fail browser validation behind the scenes.
- Older custom obtain-method labels and missing shop-price values are normalized safely when saves load.
- Existing custom Halloween Shop Egg species can now be edited normally, including changing their Fang price.
- Normal Explore Field Finds, regular items, currency, and wild eggs now announce directly beneath the maze movement controls instead of opening the large reward panel.
- Lightweight Explore rewards still update inventory/currency/eggs immediately and preserve the current maze.
- Wild battles remain interrupting encounters and continue to use the larger battle/event flow.
- Halloween Event Shop Egg species remain registry-driven from v0.15.17 and continue to use Admin-set Fang prices and custom egg art.

V0.15.17 — SHOP EGG ADMIN + HALLOWEEN SHOP FIX
- Halloween Event Shop Egg species are populated dynamically from the species registry.
- Admin exposes the price field for both normal Shop Egg and Halloween Event Shop Egg species.
- Halloween Event Shop Egg prices are paid in Fangs; normal Shop Egg prices use normal currency.
- Custom egg art controls enable for both shop egg types and disable for non-shop obtain methods.
- Halloween Event Shop monster eggs use custom egg art when supplied.
- Legacy Mournwick event-shop pricing migrates from the old hidden 1000 default to its intended 75 Fangs.

V0.15.16 — ENDLESS EXPLORE MAZE
- Normal Explore now uses an unlimited navigable 7x7 maze-style map.
- Every successful move performs one normal Explore roll using the existing reward/encounter rates.
- Revealed tiles stay visible for the current expedition; revealing the full map immediately generates a fresh random layout.
- There is no normal Explore step limit and no map-clear reward.
- Leaving Explore ends the expedition; the next visit starts a fresh layout.
- If the Active Monster faints in a wild battle, the expedition ends and returns to the Battle menu.
- Halloween Haunted Maze remains separate and keeps its Step bank, exit, event finds, and seasonal rewards.


V0.15.15 — ADMIN CONFIRMATION SAFETY PASS
- Monster Workshop now confirms Save Monster, Grant Test Copy, Grant Prismatic Test Copy, and Delete Custom Species.
- Attack Editor now confirms Save Attack and Delete Custom Attack.
- Sprite Workshop now confirms Save Sprite and restoring the built-in example.
- Silvy Dialogue now confirms Add/Update Dialogue and Delete.
- Trial Workshop now confirms Save Trial and Delete Custom Trial.
- Confirmation prompts occur after validation but before state or asset mutation, so Cancel leaves data unchanged.
- Legacy custom-monster repair: Save Monster now treats the visible Signature Attack selector as authoritative, allowing old custom species with stale signature data to be repaired in place without deletion/recreation.


V0.15.14 — COLLECTION DETAIL PORTRAIT POLISH
---------------------------------------------
Built on v0.15.13. Existing monsterGame_v06 saves remain compatible.

- Collection monster portraits now anchor near the top of the detail modal.
- Portrait size limits, pixel rendering, and Prismatic shine behavior are preserved.
- Mobile uses tighter portrait spacing for a cleaner vertical layout.

V0.15.13 — MONSTER WORKSHOP SIGNATURE ATTACK HOTFIX
--------------------------------
Built on v0.15.12. Existing monsterGame_v06 saves remain compatible.

- Hit sound effects are now selected by the attacking monster's Battle Type.
- Brute uses the existing Punch impact sound from v0.15.11.
- Defender uses Defender.wav, trimmed to 1.30s with a short fade to keep the heavier tail without overlapping later turns.
- Speed uses speed attack.wav, trimmed to 0.90s with a short fade.
- All three trigger at the same ~120 ms visual impact point established in v0.15.11.
- The mapping is data-driven from species.battleType, so built-in species, custom species, wild enemies, Trial opponents, and future monsters automatically use the correct sound.
- Misses, evades, and status-only damage do not play Battle Type hit audio.
- Audio playback remains fail-safe: browser playback errors never interrupt combat.

V0.15.4 — SILVERWIND PORTRAIT SIZE PATCH
--------------------------------------------------
Built on v0.15.2. Existing monsterGame_v06 saves remain compatible.

See the v0.15.14 Candidate Notes at the end of this file for the latest Collection detail layout polish.

PRISMWILD PROTOTYPE v0.15.1
============================

V0.15.1 — SPRITE WORKSHOP
--------------------------
Built on v0.15.0. Existing monsterGame_v06 saves remain compatible.

- Added a fourth Admin subtab: Sprite Workshop.
- Sprite Workshop centralizes the current non-monster visual slots so a sprite can be replaced once and reused everywhere that slot appears.
- Current editable slots include normal currency, item/scroll/injector icons, generic/shop/wild/prismatic eggs, field finds, Halloween event visuals and Fangs, Haunted Event Egg, seasonal placeholder visuals, and incubator/facility icons.
- Existing packaged icons remain the built-in fallback examples, so missing custom art never becomes a broken image.
- Added simple built-in placeholder sprites for event/facility slots that previously depended mostly on emoji/glyphs.
- Uploaded sprite overrides are stored in the existing IndexedDB asset database alongside custom monster art.
- Admin Export/Import is now version 3 and includes custom sprite overrides as well as custom species/attacks/art.
- Resetting game save data leaves uploaded monster art and sprite overrides in browser asset storage, matching previous custom-art behavior.
- Sprite replacements are hydrated across Shop, Inventory, Explore rewards, Eggs, Incubators, Event UI, event rewards/currency, and related detail panels.
- Monster Base/Prismatic/Special Egg art remains in Monster Workshop rather than being duplicated into Sprite Workshop.

NOTE
----
This is a candidate build and should get the usual browser smoke test before becoming the stable baseline.

PRISMWILD PROTOTYPE v0.14.0
============================

V0.14.0 — HARROWJACK + MARROWSTRIDE + BATTLE FACING
-----------------------------------------------------
Built on v0.13.0. Existing monsterGame_v06 saves remain compatible.

- Official built-in roster expanded from 29 to 31 species.
- Added Harrowjack — Nature / Defender / P1 BST 310 / rare Spooky Halloween Maze encounter.
- Harrowjack P1 stats: Vitality 86 / Attack 68 / Armor 110 / Speed 46.
- Signature: Reaping Shackle — Nature / Heavy / Power 64 / Accuracy 94% / Slow 25% for 3 turns.
- Haunted Maze Event monster encounters now weight Dirgewake 40 / Vesperfang 40 / Harrowjack 20.
- Added Marrowstride — Shadow / Spirit / Speed / P1 BST 346.
- Marrowstride is a seasonal Halloween Crossbreed: Velvetrend + Veilwyrm, 15% while a Spooky Halloween event is active.
- Marrowstride P1 stats: Vitality 78 / Attack 96 / Armor 66 / Speed 106.
- Signature: Phantom Stride — Shadow / Standard / Power 58 / Accuracy 98%.
- Phantom Stride introduces Stride Veil: a flat 10% chance to evade the next incoming attack. It does not stack and is consumed by the next attack attempt whether the dodge succeeds or fails.
- Added Next-attack Dodge % to the Admin Attack Editor for reusable future attacks.
- Crossbreed eggs now guarantee the Crossbreed species Signature Attack in Slot 1, with the father's Slot 1 move inherited into Slot 2 when available.
- Existing owned Crossbreeds missing their species Signature Attack receive a one-time Slot 1 repair; future intentional Attack Scroll overwrites are left alone.
- Existing pre-v0.14 Crossbreed eggs also enforce the species Signature Attack when hatched.
- Battle sprites now face one another automatically in Wild, Event, and Gauntlet battles using per-species Native Facing metadata.
- Frostmaw, Gravemire, Guttergore, and Mournwick are registered with the opposite native facing from the normal roster.
- Monster Workshop now includes Native Battle Facing: Left / Right for future species and custom art.
- Added packaged Base + Prismatic art for Harrowjack and Marrowstride.
- Added the new pumpkin Haunted Event Egg icon to rare maze eggs, incubators, and egg inventory displays.

PRISMWILD PROTOTYPE v0.13.0
============================

V0.13.0 — VEILWYRM + COLLECTION / ECONOMY TUNING
--------------------------------------------------
Built on v0.12.1. Existing monsterGame_v06 saves remain compatible.

- Official built-in roster expanded from 28 to 29 species.
- Added Veilwyrm — Spirit / Speed / P1 BST 312 / Haunted Event Egg.
- Veilwyrm P1 stats: Vitality 74 / Attack 86 / Armor 62 / Speed 90.
- Signature: Veil of Bones — Spirit / Standard / Power 61 / Accuracy 97% / Sleep 18% for 2 turns.
- Added packaged Base + Prismatic art for Veilwyrm.
- Haunted Event Egg pool now contains Dreadrein + Veilwyrm.
- Haunted Maze clears retain 10 Fangs + 25 Account XP and now have a 10% chance to also award a Haunted Event Egg.
- Existing 0.5% rare Haunted Event Egg chance per successful non-exit maze step remains active.
- Normal Explore direct-currency finds reduced to 1–50 currency.
- Normal wild-battle currency reward is now exactly 1 × defeated monster level.
- Global defeated-wild Collection reward chance increased from 5% to 15%, including Event wild encounters.
- Added Release Monster to Collection detail. Release is permanent, gives no reward, and cannot be used on the Active Monster, the final owned monster, a monster in an active breeding job, or a monster currently battling.
- Archive discovery now persists after releasing the last owned individual of a species.
- v0.12.1 resolved-battle cleanup hotfix remains included.

V0.12.1 — RESOLVED BATTLE CLEANUP HOTFIX
-----------------------------------------
Built on v0.12.0. Existing monsterGame_v06 saves remain compatible.

- Fixed a post-defeat lockout discovered in the Haunted Maze.
- If a finished battle is left through Shop, Collection, Event, or another top-level tab instead of the battle result's Back button, the resolved battle session is now cleaned up automatically.
- Using a Revive Gem also clears any stale finished battle session tied to that monster as a safety fallback.
- This prevents a monster that has already been revived from remaining blocked by the old battle's cached 0 Vitality state.
- In-progress battles are NOT cleared by tab navigation; only battles that already have a result are cleaned up.


V0.12.0 — VESPERFANG + LIFE STEAL TEST
-----------------------------------------
Built on v0.11.0. Existing monsterGame_v06 saves remain compatible.

- Official built-in roster expanded from 27 to 28 species.
- Added Vesperfang — Shadow / Speed / P1 BST 306. Haunted Maze encounter with the standard 5% post-victory Collection chance.
- Vesperfang P1 stats: Vitality 70 / Attack 93 / Armor 55 / Speed 88.
- Signature attack: Crimson Siphon — Shadow / Standard / Power 60 / Accuracy 96%.
- Added reusable Life Steal attack property. Life Steal restores the attacker by X% of the actual Vitality damage removed from the target, rounded down, and cannot exceed maximum Vitality.
- Crimson Siphon uses Life Steal 50%. Combat displays a separate DRAIN +X feedback popup and battle-log entry when Vitality is actually recovered.
- Added Life Steal % to the Admin Attack Editor so future custom attacks can use the same effect.
- Added Crimson Siphon Scroll to the Spooky Halloween Event Shop for 150 Fangs. It can be taught to any monster through the existing Attack Scroll system.
- Added packaged Base + Prismatic art for Vesperfang.
- Haunted Maze event encounter pool now includes Dirgewake and Vesperfang.


TYPE MATCHUPS + DAMAGE FORMULA UPDATE
-------------------------------------
Built on v0.8.0. Existing monsterGame_v06 saves remain compatible.

ELEMENT EFFECTIVENESS
---------------------
All 14 Elements now have exactly two offensive strengths and two resistances.
- Strong matchup: 1.5x damage
- Neutral matchup: 1.0x damage
- Resisted matchup: 2/3x damage (shown as about 0.67x)

Dual-Element defenders evaluate both Elements. Matchup multipliers combine, then clamp between 0.5x and 2.0x. A weakness and resistance cancel to neutral, double weaknesses cap at 2.0x, and double resistances floor at 0.5x.

Current chart:
- Fire: strong vs Nature / Ice; resisted by Water / Void
- Water: strong vs Fire / Metal; resisted by Nature / Lightning
- Nature: strong vs Water / Earth; resisted by Fire / Ice
- Earth: strong vs Lightning / Toxic; resisted by Nature / Air
- Air: strong vs Earth / Toxic; resisted by Ice / Lightning
- Ice: strong vs Nature / Air; resisted by Fire / Metal
- Lightning: strong vs Water / Air; resisted by Earth / Aether
- Metal: strong vs Ice / Light; resisted by Water / Aether
- Toxic: strong vs Spirit / Shadow; resisted by Earth / Air
- Spirit: strong vs Shadow / Void; resisted by Toxic / Light
- Shadow: strong vs Light / Aether; resisted by Toxic / Spirit
- Light: strong vs Spirit / Void; resisted by Metal / Shadow
- Void: strong vs Fire / Aether; resisted by Spirit / Light
- Aether: strong vs Lightning / Metal; resisted by Shadow / Void

NEW DAMAGE FORMULA
------------------
Combat now uses a Gen-5-inspired Prismwild formula:
Base Damage = ((((2 x Level / 5) + 22) x Power x Attack / Armor) / 50) + 2
Final Damage = Base Damage x STAB x Type Effectiveness x Random

- STAB remains 1.10x when the move matches either of the attacker's Elements.
- Random damage variance is now 90-100% instead of 90-110%.
- Type effectiveness applies after the base damage calculation.
- No critical-hit system has been added yet.

BATTLE UI
---------
- Combatant metadata now displays each monster's Element(s).
- Attack choices preview SUPER EFFECTIVE or RESISTED matchups.
- Damage feedback and the battle log call out matchup effectiveness.
- A Type Chart dialog is available from both the Battle hub and active combat.

SAVE COMPATIBILITY
------------------
The localStorage key remains monsterGame_v06. This update changes combat rules only and does not require a save migration.


PRISMWILD PROTOTYPE v0.8.0
============================

ACCOUNT PROGRESSION + REQUEST BOARD + WILD GAUNTLET
----------------------------------------------------
Built on the successful v0.7.0 Trail Signs / Field Finds build. Existing monsterGame_v06 saves remain compatible.

ACCOUNT LEVEL + XP
------------------
- Account Level is separate from monster levels and never changes monster stats.
- Account XP starts with 100 XP needed for Level 2, then each next level requires 50 more XP than the previous level.
- A persistent Account Level / XP bar appears in the top header and on the Requests page.
- Level-ups give modest automatic rewards: currency, Recovery Gels, Incubation Catalysts, and occasional Revive Gems at milestones.

DAILY REQUEST BOARD
-------------------
- Three requests are generated per local calendar day: one Easy, one Medium, and one Hard.
- The daily board is saved, so refreshing cannot reroll the requests.
- Requests can track Explore routes, wild battle wins, Field Finds gathered, Field Find sale value, breeding, hatching, and Wild Gauntlet progress.
- Each completed request can be claimed for normal currency + Account XP.
- Claiming all three unlocks a Daily Completion Bonus: 50 Account XP + one useful item.

WILD GAUNTLET
-------------
- New five-stage battle activity available from the Battle hub.
- Enemy levels rise as the run goes deeper.
- The player's current Vitality carries between stages; battle statuses clear between stages.
- Recovery Gels can still be used during combat.
- Fleeing is disabled inside Gauntlet battles.
- Each win adds unclaimed currency and loot to the run's haul.
- After every cleared stage, return to camp and choose to Continue or Claim Rewards & Leave.
- Losing a battle forfeits the unclaimed haul and grants only a small consolation currency reward.
- Deep stages can add useful items, Attack Scrolls, and rarely a Wild Egg to the banked haul.
- Account progress tracks best Gauntlet stage cleared and total cash-outs.

SAVE COMPATIBILITY
------------------
The localStorage key remains monsterGame_v06 intentionally. v0.7.0 and older v0.6.x saves gain the new Account / Request fields during normalization.


PRISMWILD PROTOTYPE v0.7.0
============================

TRAIL SIGNS + FIELD FINDS UPDATE
--------------------------------
Official built-in roster expanded to 24 species. Existing monsterGame_v06 saves remain compatible.

New official species:
- Shardback — Ice / Defender / P1 BST 300 / Glacier Break
  Breed 35 min / Hatch 50 min / Random Battle Reward
- Hexolith — Earth / Defender / P1 BST 309 / Ruin Hammer
  Breed 40 min / Hatch 55 min / Random Battle Reward

Both species include packaged Base + Prismatic art.

TRAIL SIGNS
-----------
Explore now adds one small decision before the event roll. Press Scout the Trail to reveal three route clues, then choose one. A Trail Sign changes the event weights slightly but never guarantees an outcome.

Current route clues can lean toward:
- wild monster encounters
- Field Finds
- useful items
- wild eggs
- or an unmarked / neutral path

The core event table is now:
- Wild Battle: 60%
- Field Find: 19%
- Currency: 8%
- Useful Item: 8%
- Wild Egg: 5%

FIELD FINDS + SELLING
---------------------
Field Finds are simple sell-only exploration loot in this first implementation.
- Loose Shiny Rocks — sells for 2 currency each
- Monster Scale — sells for 3 currency each
- Herbs — sells for 2 currency each

Field Finds stack in Inventory. Their cards include Sell 1 and Sell All actions. Sell All asks for confirmation. Shop consumables, Attack Scrolls, eggs, and other existing items are not sellable in this version.

No crafting system has been added. Field Finds are intentionally lightweight so the exploration loop gains flavor without becoming a separate resource-management game.

PRISMWILD PROTOTYPE v0.6.9
============================

CROSSBREEDS, WATER + INCUBATOR UPDATE
--------------------------------------
Official built-in roster expanded to 22 species.

New authored crossbreeds:
- Wraithwood — Nature / Spirit / Speed / P1 BST 334 / Bloomreign + Morrowisp / 16%
- Railclast — Metal / Lightning / Defender / P1 BST 336 / Clatterjaw + Voltalon / 15%

New base species:
- Tideveil — Water / Speed / P1 BST 294 / Undertow Aria

WATER ZONE UPDATE
-----------------
Thursday / The Bright Temple now supports Light / Spirit / Water.
Tideveil is therefore eligible for The Bright Temple and Sunday Chaos Wastes when Water rolls.

INCUBATION CATALYST
-------------------
Incubation Catalyst is now functional.
- One catalyst maximum per egg.
- Reduces remaining hatch time by 30 minutes.
- If less than 30 minutes remain, the egg becomes ready immediately.
- Catalyst use persists in the save.

INCUBATOR UI REWORK
-------------------
Incubators are now compact icon-first tiles, matching the Shop direction.
Selecting an occupied incubator opens a detail popup showing:
- egg art / icon
- egg name and ID
- live time remaining
- Hatch button
- Incubation Catalyst ownership and use button
- whether a catalyst has already been used on that egg

Archive discovery silhouettes and all v0.6.8 systems remain intact.
Existing monsterGame_v06 saves remain compatible.

PRISMWILD PROTOTYPE v0.6.8
============================

ROSTER COMPLETION UPDATE
------------------------
Official built-in roster expanded from 15 to 18 species.

Added official built-ins:
- Clatterjaw — Metal / Brute / P1 BST 301 / Shear Maw
- Guttergore — Toxic / Brute / P1 BST 303 / Gutter Clamp
- Halowing — Air / Speed / P1 BST 296 / Gale Shear

All three include packaged base and Prismatic art.
Wide generated Guttergore and Prismatic Halowing assets were padded to transparent square canvases without cropping or rescaling the creature art.

Older v0.6 saves remain compatible. Built-in species and attacks merge into existing saves during normalization.
The localStorage key remains monsterGame_v06 intentionally.

PRISMWILD PROTOTYPE v0.6.6
================================

A Fantastical Grim Monster Breeding Game

SHOP UI CLEANUP
---------------
The Shop is now icon-first instead of using large information cards.

Each shop section displays compact tiles containing:
- the item / egg / scroll / upgrade icon
- the item name
- a small category label

Clicking a tile opens a Collection-style detail popup.

The popup shows:
- large artwork / icon
- name and category
- full description
- useful metadata
- current owned quantity when relevant
- price with the Prismwild currency icon
- Purchase button

PURCHASE CONFIRMATION
---------------------
Pressing Purchase does NOT immediately spend currency.

The detail popup changes into a confirmation step showing:
- the exact item being purchased
- exact price
- current currency balance
- Cancel
- Confirm Purchase

Only Confirm Purchase completes the transaction.

This confirmation flow applies to:
- Monster Eggs
- Attack Scrolls
- normal Items
- Revive Gems
- Potential Injectors
- Incubator upgrades

All v0.6.5 gameplay systems remain intact, including:
- 15 official monsters
- element-driven Explore zones
- weekly Chaos Wastes elements
- rare Explore item drops
- 5% defeated-monster Collection reward
- 3-minute faint timer
- Revive Gem
- breeding / eggs / incubators
- Attack Scrolls
- Traits / Potential
- sequential combat
- Admin Monster Workshop and Attack Editor

SAVE COMPATIBILITY
------------------
Still uses monsterGame_v06. Existing v0.6.x saves remain compatible.

PRISMWILD PROTOTYPE v0.6.5
============================

A Fantastical Grim Monster Breeding Game

THIS BUILD
----------
v0.6.5 is a gameplay-polish and official-roster update built on v0.6.4.

OFFICIAL ROSTER ADDITIONS
-------------------------
The following three monsters are now baked directly into the prototype,
including base and Prismatic artwork plus their signature attacks:

AUREVANE
- Light
- Speed
- P1 BST 292
- Signature: Crescent Flash
- Thursday / The Bright Temple

CINDERVANE
- Metal
- Brute
- P1 BST 308
- Signature: Crucible Horn
- Monday / Blaze Lands
- Also eligible for Saturday / The Wastelands because Metal is present there

MORROWISP
- Spirit
- Defender
- P1 BST 287
- Signature: Soul Lantern
- Thursday / The Bright Temple

Older v0.6 saves automatically receive these official species and attacks.
If Dell already created matching custom versions through Admin, those records
are preserved while the packaged art becomes available as a fallback.

EXPLORE RARITY REBALANCE
------------------------
Previous Explore event rates:
- Wild battle 55%
- Item 20%
- Currency 20%
- Egg 5%

New rates:
- Wild battle 60%
- Item 8%
- Currency 27%
- Egg 5%

Items should now feel meaningfully less common.

Within the 8% item event:
- Recovery Gel: 60% of item finds
- Incubation Catalyst: 30% of item finds
- Revive Gem: 10% of item finds

That makes a Revive Gem approximately a 0.8% result on any individual Explore
action.

REVIVE GEM
----------
New item:
Revive Gem

Shop price:
500 currency

Icon:
Uses the Prismatic Shard icon from Item Sheet 01.

Function:
Immediately clears a monster's faint recovery timer.

FAINT SYSTEM
------------
If the player's monster reaches 0 Vitality in a wild battle:
- it becomes FAINTED
- it cannot battle for 3 minutes
- the timer persists through refreshes / closing the page
- it may still be viewed, bred, renamed, etc.
- a different healthy monster can be made Active
- a fainted monster cannot be newly selected as Active
- if the currently Active monster faints, Explore is disabled until the player:
  1. waits for recovery,
  2. uses a Revive Gem from that monster's Collection detail, or
  3. switches to another healthy monster

Collection cards, monster detail, Battle Hub, and Explore show the recovery
countdown.

WILD MONSTER BATTLE REWARD
---------------------------
Every defeated wild monster now has a flat 5% chance to join the player's
Collection after victory.

On success:
- the encountered species is kept
- its encountered level is kept
- its generated gender is kept
- its generated Trait is kept
- its P1 Potential is kept
- its current attack set is kept
- it receives a new permanent Collection ID
- the victory panel announces NEW MONSTER

This is intentionally uncommon and is separate from the normal XP / currency
reward.

SAVE COMPATIBILITY
------------------
Still uses:
monsterGame_v06

Existing v0.6.x progress remains compatible.

CURRENT WEEKDAY ZONES
---------------------
Monday: Blaze Lands
Fire / Earth / Metal

Tuesday: Flat Lands
Nature / Air / Lightning

Wednesday: The Shadow Plains
Shadow / Void / Aether

Thursday: The Bright Temple
Light / Spirit / Water

Friday: Permafrost Peaks
Earth / Ice / Air

Saturday: The Wastelands
Toxic / Metal

Sunday: Chaos Wastes
Three Elements rolled once per calendar week.

All v0.6.4 systems remain intact, including:
- automatic Element-based zone assignment
- Item Sheet 01 atlas
- Explore Travel Supplies
- Admin Monster Workshop
- Admin Attack Editor
- custom art via IndexedDB
- Admin export/import
- breeding / eggs / incubators
- Traits
- Potential
- Attack inheritance
- Attack Scrolls
- sequential Speed-based combat
- status effects
- XP / levels
- Active Monster system
- daily Explore zones



v0.6.8 CROSSBREED + ARCHIVE UPDATE
- Added Rimeforge as the first official authored crossbreed (Moltcrag + Frostmaw).
- Crossbreeds support a second Element and are forced to Breeding Only.
- Crossbreed chance editor is constrained to 10-20%.
- Dual-Element monsters receive same-element attack bonus from either Element.
- Rimeforge uses Fire / Ice, Brute, P1 BST 345, 12% crossbreed chance.
- Archive now hides unowned species as black silhouettes with ???? data until obtained.
- Existing monsterGame_v06 saves remain compatible.


v0.10.0 — EVENT FRAMEWORK / SPOOKY HALLOWEEN TEST
- Adds reusable Event tab, calendar, event currency wallets, event shops, date windows, and Admin event overrides.
- Spooky Halloween uses Fangs and the Haunted Maze activity.
- Haunted Maze: random persistent 7x7 perfect maze, fog of war, 10 starting Steps, +5 Steps/hour, 20-Step cap.
- Maze movement can find Fangs, exchangeable event finds, rare useful items, and future Event monster encounters.
- Escaping grants 10 Fangs + 25 Account XP and allows generating a new random maze.
- Event monster pool is intentionally empty in this framework-test build. Once event species are added to EVENT_DEFS.spooky_halloween_2026.activity.eventSpecies, maze encounters use normal battles and the standard 5% post-victory Collection chance.
- Test Event Shop verifies Fang spending, purchase limits, item delivery, and egg delivery.
- Event Admin Tester can force Halloween active/inactive, grant Fangs/Steps, and reset the maze.


v0.11.0 — SPOOKY HALLOWEEN MONSTER TRIO

- Official built-in roster expanded from 24 to 27 species.
- Added Dirgewake — Shadow / Brute / P1 BST 305. Haunted Maze encounter; standard 5% post-victory Collection reward chance. Signature: Funeral Rush.
- Added Mournwick — Spirit / Defender / P1 BST 309. Available from the Spooky Halloween Event Shop as a 75-Fang egg. Signature: Lantern Dirge.
- Added Dreadrein — Aether / Speed / P1 BST 308. Rare Haunted Event Egg species found in the maze. Signature: Pale Gallop.
- Added packaged Base + Prismatic art for all three Halloween monsters.
- Haunted Maze now supports data-driven event encounter, Fang, trade-find, rare-item, and rare-event-egg rates.
- Haunted Event Eggs are currently a 0.5% find per non-exit successful maze step and use a reusable rareEggPool for future Halloween species.
- Haunted Event Eggs hide their species name in the egg/incubator UI until hatching.
- Existing monsterGame_v06 saves remain compatible; new built-ins merge into older saves automatically.


v0.15.0 timing note
- Authored Crossbreed pairings use the target recipe's breed timer even when the rarity roll fails; hatch time follows the resulting egg species.


=== v0.15.2 Candidate Notes ===
- Added Silverwind's Desk as an in-world resident researcher/check-in page. Silverwind has a Sprite Workshop slot for replacement art.
- Added Breeding Pens: 1 unlocked by default, up to 5 total. Extra pens cost 10,000 / 25,000 / 50,000 / 100,000 currency.
- Breeding parents are now locked to their exact active pen and persist through refreshes until the egg is collected.
- Legacy v0.15.1 single breeding jobs migrate automatically into Breeding Pen 1.
- Added Hormone Catalyst (750 currency), usable once per active pairing to cut 30 minutes from remaining breed time.
- Added Sprite Workshop slots for Breeding Pen, Hormone Catalyst, and Silverwind.

=== v0.15.3 Candidate Notes ===
- Added final Silverwind NPC art with two independent Sprite Workshop slots: Normal Pose and Check-In Pose.
- Silverwind swaps to the Check-In pose for several seconds whenever the player presses Check In.
- Added a permanent fourth daily request, Keeper Check-In. It does not rotate with the Easy/Medium/Hard requests and resets once per local day.
- The first Silverwind check-in each day automatically completes/claims that request, grants 25 Account XP, and grants one weighted random useful item.
- Daily random check-in item pool: Recovery Gel, Incubation Catalyst, Hormone Catalyst, Revive Gem, or P2 Potential Injector.
- The Daily Board completion bonus now requires the three rotating requests plus the daily Silverwind check-in.
- During an active event, Silverwind can occasionally select event-specific dialogue. Special first-check-in event gift lines grant 5 units of that event's currency when selected.
- Seeded Spooky Halloween dialogue includes Haunted Maze chatter and Fang gift lines. Future Winter/Spring examples are included as editable planning content.
- Added Admin > Silvy Dialogue. Dialogue can be created, edited, and deleted for General chatter, any registered Monster, or any Event.
- Monster targets are populated directly from the species registry, so newly imported/created monsters automatically appear in the dialogue editor.
- Event dialogue has an optional First Daily Check-In Gift flag; those lines automatically award 5 of the selected event's currency when rolled on the first check-in of the day.
- Silvy dialogue is stored in the save and included in Admin Export/Import (export schema v4).


=== v0.15.5 Candidate Notes ===
- Increased Silverwind's Desk portrait display from 220px to 384px on desktop so the full-body NPC art is clearly readable.
- Medium layouts use a 320px portrait; narrow/mobile layouts scale up to 340px while respecting the viewport.
- Added crisp pixel-image rendering to preserve the sprite-art look when enlarged.
- No check-in, dialogue, reward, breeding, save, or sprite-registry logic changed in this patch.


v0.15.5 hotfix: Breeding pen countdowns now update in place instead of rebuilding the entire pen UI every 500ms. This prevents Collect Egg and Hormone Catalyst clicks from being swallowed by timer refreshes.


=== v0.15.6 Candidate Notes ===

Breeding system second pass / reliability rebuild.

- Restored the missing pairKey() helper used by Crossbreed recipe lookup. Its absence was the root cause of both Start Breeding failing and ready eggs disappearing during collection.
- Breeding outcomes are now rolled and stored as a pendingEgg inside the pen when breeding STARTS, instead of being generated only when Collect Egg is clicked.
- Collection is now two-phase and recovery-safe: the egg is persisted before the pen is freed. On reload, a stale pen whose pending egg is already in Egg Inventory is automatically cleared without duplicating or deleting the egg.
- Existing v0.15.2-v0.15.5 pens without pendingEgg data are repaired automatically on load.
- Breeding Pen buttons now use delegated click handling so UI card refreshes cannot detach Collect Egg or Hormone Catalyst handlers.
- Start Breeding is now an explicit type=button control with clearer availability checks and warnings.
- Parent selectors refresh after pen state changes and continue excluding monsters locked in active pens.
- Timer transitions only rebuild the pen when it becomes READY.
- Tested: start breeding, simulated refresh, ready/collect, post-collection refresh, immediate re-breed, two simultaneous pens, Hormone Catalyst, old-pen repair, and interrupted-collection recovery.


=== v0.15.7 Candidate Notes ===

Silverwind Reference Desk / navigation cleanup.

- Removed the standalone Archive and Attack Index buttons from the main navigation.
- Silverwind's Desk now acts as the Prismwild reference hub with three internal sections: Keeper's Desk, Monster Archive, and Attack Index.
- Keeper's Desk preserves daily check-in rewards, dynamic dialogue, event chatter, and Desk Notes.
- Monster Archive reuses the existing discovery/silhouette system and automatically reflects registered species.
- Attack Index reuses the existing search, Element filter, and Admin-added attack registry.
- Entering Silverwind from the main navigation or Request Board opens Keeper's Desk by default.
- No save schema, breeding, monster, attack, reward, event, or Admin data logic changed in this cleanup.


=== v0.15.8 Candidate Notes ===
- New top-level My Hideout tab. Collection, Incubators, Breeding Pens, and Inventory now live as internal Hideout sections.
- Existing switchTab destinations for collection / eggs / breed / inventory route into My Hideout, preserving older internal buttons and flows.
- Collection is now organized into Collection Pens. Each Pen has a 50-monster capacity.
- Start with 1 Collection Pen. Up to 10 total can be unlocked from Shop > Facility Upgrades.
- Collection Pen upgrade costs: Pen 2 5,000; Pen 3 10,000; Pen 4 20,000; Pen 5 35,000; Pen 6 55,000; Pen 7 80,000; Pen 8 110,000; Pen 9 150,000; Pen 10 200,000.
- Existing saves migrate monster IDs into Pens without deleting or hiding them. If a legacy save already exceeds 50 monsters, enough Pens are automatically unlocked to fit the existing roster.
- Monster detail now has a Collection Pen control for moving an individual monster between unlocked Pens. Full Pens cannot be selected as a destination.
- Press and hold a monster card for 450 ms, then drag over another monster in the same Pen and release to rearrange that Pen. Order is saved.
- Hatching, wild/event monster rewards, and Admin test copies now respect unlocked Collection Pen capacity. A ready egg remains intact if all unlocked Collection Pens are full.
- Collection Pen has its own Sprite Workshop key and currently uses the Breeding Pen sprite as a basic fallback placeholder.
- v0.15.8 is a candidate build until Dell completes hands-on testing.


=== v0.15.9 Candidate Notes ===
- New top-level Explore tab. Battle, Shop, and Trials now live as internal Explore sections. Existing legacy routes to Battle/Shop are redirected into the correct Explore section.
- Added permanent Trial challenges using the existing single Active Monster battle system. Each Trial has a Captain NPC, Element, three-monster lineup, Normal/Hard requirements, badge reward, and Hard-mode exclusive Attack reward.
- Trial fights are three consecutive battles. Vitality carries between opponents, battle statuses clear between opponents, Recovery Gels remain usable, and fleeing is disabled.
- Added the first built-in Nature Trial: Thornjack Lv.20 / Thornjack Lv.22 / Bloomreign Lv.25 on Normal, and Lv.70 / Lv.72 / Lv.75 on Hard.
- Nature Trial Normal clear awards the Nature Badge. Hard clear awards one Nature Beam Attack Scroll. Rewards are one-time; cleared modes can still be replayed.
- Added Nature Beam: Nature / Heavy / Power 90 / Accuracy 95% / 15% Stun. Nature Beam is Trial-exclusive and is not sold through the normal Attack Scroll shop.
- Added Stun as a reusable Attack Editor status. Stun skips exactly one action, including when applied by a slower attacker late in the round.
- Added Profile page showing Account Level + XP, total monsters, Normal Trial badges, Hard clears, the player's three highest-level monsters, and a Trial badge display.
- Added Admin > Trial Workshop. Trials can be created/edited with Element, Captain name/dialogue, Normal/Hard requirements, three registered species, per-mode enemy levels, badge name, Hard reward Attack, Captain sprite, and badge sprite.
- Built-in Trials can be edited but cannot be deleted. Custom Trials can be deleted. Trial lineups automatically use the current species registry and reward dropdown uses the current Attack registry.
- Trial Captain and badge art are stored in the existing IndexedDB asset system. Generic Captain/badge placeholders are packaged for new Trials.
- Admin Export/Import schema is now v5 and includes Trial definitions plus custom Trial Captain/badge art.
- Monster deletion is blocked while that species is assigned to a Trial lineup. Attack deletion is blocked while that Attack is assigned as a Trial reward.
- Leaving a Trial screen during an active run now presents a clear Resume Trial action. Battle/Gauntlet entry is disabled while a Trial run is active.
- Existing monsterGame_v06 saves remain compatible. Older saves receive built-in Trial definitions and empty Trial progress during normalization.
- First-pass balance choices: Nature Beam Stun chance is 15%; Trial Vitality carries between opponents; Normal clear is not currently required to enter Hard if the active monster meets the Hard level requirement. These can be tuned after hands-on play.
- v0.15.9 remains a candidate until Dell completes hands-on testing.


=== v0.15.10 Candidate Notes ===
- Added the provided 48 kHz stereo WAV as the default battle hit sound at assets/audio/attack_hit.wav.
- The hit sound plays only when a damaging attack connects, including normal, super-effective, and resisted hits. Misses, evades, status ticks, and non-hit feedback do not trigger it.
- Added Sell Egg to every loose/unincubated egg card. Selling grants a flat 10 currency.
- Selling is limited to waiting eggs; incubating eggs are unaffected.
- A confirmation prompt protects rare eggs from accidental one-click sales.
- v0.15.10 remains a candidate until Dell completes hands-on testing.


=== v0.15.11 Candidate Notes ===
- Attack-hit audio now fires at the visual impact point of the lunge animation (~120 ms after animation start) instead of after the full lunge completes.
- Default hit WAV trimmed from 2.0 s to 0.9 s with a short fade-out to prevent the tail from overlapping the following attack.
- Damage/status resolution is synchronized to the impact callback while preserving existing combat flow and miss behavior.
- Egg selling and all v0.15.10 systems are otherwise unchanged.


=== v0.15.12 Candidate Notes ===
- Battle hit audio is now selected from the attacking monster's Battle Type.
- Brute uses brute_hit.wav (the v0.15.11 punch impact).
- Defender uses defender_hit.wav, trimmed to 1.30 s with a short fade.
- Speed uses speed_hit.wav, trimmed to 0.90 s with a short fade.
- All three sounds trigger at the same ~120 ms visual impact point.
- The mapping reads species.battleType, so it applies automatically to player monsters, wild/event enemies, Trial opponents, and custom species.
- Misses, evades, and status-only damage remain silent.
- Existing v0.15.11 gameplay and save data are otherwise unchanged.
- v0.15.12 remains a candidate until Dell completes hands-on audio testing.


=== v0.15.13 Candidate Notes ===

MONSTER WORKSHOP SIGNATURE ATTACK HOTFIX
- Added a dedicated draft value for the Signature Attack selector.
- The selected Signature Attack now survives asynchronous UI redraws and tab changes while editing a species.
- Saving a species uses the held draft selection, preventing the dropdown from silently reverting to an earlier/default attack.
- Loading another species or starting a new species intentionally resets the draft to that species/default selection.
- Grant Test Copy and Grant Prismatic Test Copy continue to read the saved species Signature Attack.
- All v0.15.12 Battle Type audio behavior remains unchanged.


=== v0.15.14 Candidate Notes ===

COLLECTION DETAIL PORTRAIT ALIGNMENT
- The full monster portrait in the Collection detail modal now anchors near the top of the left art column.
- Portrait height remains capped so large sprites stay contained.
- Mobile layout uses a slightly tighter top padding and max height.
- No Collection, monster, save, battle, breeding, attack, or Admin logic changed in this patch.


v0.15.20: Normal Explore wild encounters now enter combat immediately from maze movement, matching the Halloween Haunted Maze flow. Built from the known-good v0.15.18 baseline.


v0.15.21: Added Daily Expeditions with Short (1h), Extended (5h), and Long (12h) contracts, 1–5 monster teams, persistent timers, bonus-loot team scaling, mission-specific rewards, rare Lost Temple Prismatic Eggs, expedition monster lockouts, and Admin expedition test controls.


v0.15.23 adds a Home landing page with dynamic newest-monster showcase, Event status, editable News, and editable Announcements. Landing posts are managed in Admin > Landing Page and included in Admin Export/Import.


v0.15.23 public-test prep:
- Fresh saves now begin as Player accounts with 1000 currency and a newcomer flow.
- Starter choices: Moltcrag (Brute), Sludgewart (Defender), Voltalon (Speed), all Lv.5 / P3.
- New Keeper Bundle: 3 Revive Gems, 2 Incubation Catalysts, 1 Mystery Egg.
- Home includes a New Keeper Path checklist.
- Profile includes local Keeper name, local account ID, role display, reset controls, and prototype Admin access.
- Existing pre-v0.15.23 saves preserve progress, migrate as Player, and skip duplicate newcomer rewards. Admin access is unlocked locally from Profile with the project-owner test code.
- IMPORTANT: Player/Admin separation in this standalone HTML build is only for prototype testing. It is not secure authentication. Real public deployment requires server-side accounts/authorization.


v0.15.27 live-content publishing:
- Adds content/prismwild-content.js as the public live-content layer.
- The initial public content pack contains the current Admin export supplied for this build.
- Custom species can be marked Published or Draft in Admin > Monster Workshop. New species default to Draft.
- Admin > Export Live Content downloads one prismwild-content.js file containing published custom species/art plus custom attacks, shared sprites, landing posts, Silvy dialogue, and Trial data.
- To publish content without a game rebuild, replace content/prismwild-content.js in the GitHub repository, then Commit and Push Origin.
- Public clients import a new content revision once into their local species/attack registries and IndexedDB artwork cache. Player collections/progress are preserved.
- Full Admin Export/Import remains available separately for workshop backups.

v0.15.27 live-content publishing:
- Live Content is now explicitly the complete Admin-authored CONTENT layer, not just monsters.
- Sprite Workshop replacements are automatically exported, including Halloween/event/shop icons.
- Silvy Dialogue, Landing News/Announcements, Trials, Trial Captain art, and Trial Badge art are automatically exported.
- Published custom Monsters and custom Attacks retain Draft/Published gates.
- Export status and the loaded-content status now show a content manifest with category counts.
- Local test controls and player/account save state are intentionally excluded from publishing.


v0.15.28 — Navigation + Breeding Polish
-----------------------------------------
- Shop is restored as a permanent main navigation button.
- Expeditions now occupy Shop's former slot inside Explore: Battle / Expeditions / Trials.
- Profile moved into My Hideout.
- My Hideout, Explore, and Silverwind now have direct dropdown shortcuts from the main bar.
- Fixed Expedition Treasure leaking into normal Explore Field Find rolls.
- Fixed the same mixed-registry leak in Wild Gauntlet Field Find rewards.
- Breeding now has a 5% chance to improve the Mother-role monster's inherited Potential by +1 stage, capped at P12.
- The Potential improvement is rolled and persisted when pendingEgg is created, so reloads and timer catalysts cannot reroll it.
- Bred eggs display their inherited Potential; successful improvements are marked with a gold P# → P# ✦ callout.
- Hatch now uses the egg's snapshotted motherPotential as a fallback, so releasing a parent after egg collection cannot accidentally collapse offspring Potential to P1.


v0.15.29 — Navigation Dropdown Hover Hotfix
--------------------------------------------
- Fixed main navigation dropdowns closing while the cursor crossed the small visual gap between a top-bar trigger and its menu.
- Added an invisible hover bridge above each dropdown so My Hideout, Explore, and Silverwind remain open while moving the cursor into their menu options.
- Existing click/focus behavior remains intact.
- No gameplay, save, breeding, loot, content, or balance logic changed in this hotfix.



=== v0.15.32 Candidate Notes ===
- Winter Gift Calendar shortened from 31 days to 25 days.
- Existing v0.15.30 calendar data is normalized to the 25-day cap; stale Day 26-31 prize entries are pruned automatically.
- Event Workshop Calendar Day and Calendar Test Day controls respect the configured 25-day Winter calendar length.

=== v0.15.30 Candidate Notes ===

MODULAR WINTER EVENT FOUNDATION
- Winter Event is now registered as an upcoming Dec 1, 2026 through Jan 2, 2027 seasonal event using Snowflakes as its event currency.
- Added a publishable Daily Event Calendar system. Admin > Event Workshop can configure each calendar day as Money, Item, Egg, or direct Monster reward.
- Calendar configurations are now included in Live Content exports/imports (schema v8); test date overrides remain local-only.
- Calendar supports catch-up claiming for previously unlocked days by default.
- Added Calendar Test Day so future event calendars can be tested without changing the computer clock.
- Forced-active Event Tester selections now take priority over naturally active events, making Winter testable while Halloween is still live.
- Added Winter Memory, a persistent 4x4 / 8-pair monster matching mini-game.
- Each matched pair currently awards 2 Snowflakes. Matched pairs stay revealed and rewards cannot be re-earned on refresh.
- Three failed matches end the run and trigger a 20-minute cooldown; after cooldown a new randomized board is generated.
- Completing all eight pairs grants a Winter Mystery Egg and triggers a one-hour cooldown before a fresh set.
- The Mystery Egg currently uses Frostmaw/Shardback as a temporary test content pool; its final Winter pool/art can be swapped in when the Winter Mystery Egg is designed.
- Admin Event Workshop includes Reset Memory Board and Clear Memory Cooldown controls for local testing.
- Existing monsterGame_v06 saves remain compatible.


=== v0.15.32 Candidate Notes ===
- Added built-in Winter species Bouldrift, Yulemaw, and seasonal Crossbreed Briarhart with base/prismatic art and signature attacks.
- Bouldrift is registry-driven Winter Event Shop stock at 120 Snowflakes.
- Yulemaw is the built-in Winter Mystery Egg species. Additional custom species can join that pool with Obtain Method = Winter Mystery Egg.
- Winter Memory now includes a Snowflake Event Shop beneath the board.
- Monster Workshop adds Winter Event Shop Egg / Winter Mystery Egg obtain methods and a Seasonal Recipe selector for Crossbreeds.
- Seasonal Crossbreed recipe gating was repaired and generalized by event family. Recipes are active only while that seasonal event is active (including Admin Force Active); owned monsters remain usable afterward.
- Briarhart = Bouldrift × Thornjack, 15% Winter-only Crossbreed chance, authored 55m breeding / 70m hatch timers.


=== v0.15.33 Candidate Notes ===
- Winter Memory failed-match cooldown reduced from 20 minutes to 3 minutes. Completion cooldown remains 1 hour.
- Added Shop Black Market: three persistent daily standard-species requests, excluding Mythics and Crossbreeds.
- Black Market prefers eligible species already owned when possible. Normal requests only accept normal monsters.
- Very rare Prismatic request chance: 0.5% per slot, only when a matching Prismatic is owned; Prismatic payouts use a 12x premium.
- Black Market payouts scale with species P1 BST, individual Level, and Potential. Active/breeding/expedition/battle monsters cannot be sold.
- Monster Archive split into Base Monsters and Crossbreeds tabs.
- Existing prismwild-content.js preserved unchanged from the v0.15.32 CONTENT_PRESERVED package.


=== v0.15.34 ===
- Winter Daily Calendar can award event currency; Day 1 defaults/migrates to 50 Snowflakes.
- Refresh Juice: 1-hour item cooldown; +5 Halloween Maze Steps or clears Winter failed-match cooldown only.
- Capture Pod: 20 minutes, +20 percentage points to normal capturable defeat recruitment chance.
- Nature Disc: rerolls Trait once per local day per individual monster.
- DNA Splicers: Vitality / Attack / Armor / Speed; +15 permanently; exactly one DNA Splicer total per monster.
- Shop prices: Refresh Juice 1,000; Capture Pod 2,500; Nature Disc 5,000; each DNA Splicer 50,000.
- Player live-content file remains preserved from v0.15.33.
