# 🌿 Verdant Vale

![Engine: Three.js r160](https://img.shields.io/badge/engine-Three.js%20r160-black.svg)
![Architecture: Single File](https://img.shields.io/badge/architecture-single--file%20HTML-blue.svg)
![Size](https://img.shields.io/badge/size-9.1%20MB-lightgrey.svg)
![License: MIT](https://img.shields.io/badge/license-MIT-green.svg)

**A full, 31-chapter open-world action RPG — running entirely inside one HTML file.**
No installer, no build step, no server, no network call. Open it in a browser and you're standing at a well in a dying valley.

> **▶️ [Play Verdant Vale Live](https://padmanavamukhopadhyay.github.io/Verdant-vale-Open-world-First-Game-created-by-Me-/)**
> **▶️ [Support Verdant Vale on itch.io](https://sensei-minato.itch.io/verdant-vale)**

---

## Table of Contents

- [Part 1 — Inside Verdant Vale](#part-1--inside-verdant-vale)
  - [The Premise](#the-premise)
  - [The World](#the-world)
  - [Villains & Bosses](#villains--bosses)
  - [The Key Hunt](#the-key-hunt)
  - [Combat & Gear](#combat--gear)
  - [Economy & Enterprise](#economy--enterprise)
  - [Controls](#controls)
  - [Content, Counted](#content-counted)
- [Part 2 — How We Built It](#part-2--how-we-built-it)
  - [The Shape of One File](#the-shape-of-one-file)
  - [Mapping a 22,600-Line Codebase](#mapping-a-22600-line-codebase)
  - [Data Tables, Not Special Cases](#data-tables-not-special-cases)
  - [A Procedural, Zero-Asset-File Pipeline](#a-procedural-zero-asset-file-pipeline)
  - [Calibrating for Performance](#calibrating-for-performance)
  - [A Save File That Survives Its Own Future](#a-save-file-that-survives-its-own-future)
  - [Verification Discipline](#verification-discipline)
  - [Shipping Readiness](#shipping-readiness)

---

## Part 1 — Inside Verdant Vale

### The Premise

You are **Sigrid**, and you slept through the beginning of the end.

The Vale is a bowl roughly four kilometres across, walled in by white mountain. Something underneath it is hurting, and it's leaking — the dead don't stay down, and the husks that used to turn back at the hedge line have stopped turning back.

**Elder Rowan** meets you at the well and tells you the whole of it (press **T** anytime to replay it). **Halvard Stray** joins as your companion from Act I — he rides with you, and what he comes to think of your choices gets read back to you at the end.

**31 chapters, 6 acts**, closing on one decision at the last door — three different endings depending on how you got there.

### The World

A **4,000 m box** of noise-shaped terrain, with **seven settlements**, each built around a forge, a stable, an inn and a pelter:

| Village | Location | Character |
|---|---|---|
| **Wold Cross** | centre | Rowan, the well, the Tradehouse, the altar |
| **Thornwick** | east | Under the crags; ore and stone |
| **Harrowgate** | west | The last gate before the waste |
| **Greyhollow** | north | Cold and rich — trades upward |
| **Saltmere** | south-west | Built on a drained lake bed |
| **Emberfall** | south-east | Charcoal burners, a forge that never goes out |
| **Stonewatch** | north-west | The old garrison |

Four roads connect them; raiders ambush the roads but never within a hundred metres of a village. Landmarks: the **Hollow Fort**, the **Dragon's Den**, six barrow/shrine Key sites, a dozen-plus raider camps, the **Altar**, and the white mountain rim where the rare **Vale-Crystal Beasts** roam.

### Villains & Bosses

Two threats: **the Warden**, an ancient presence whose corrupted rest leaks out as the Blight, and **the Chapter**, a cult that's been deliberately widening that wound for forty years.

| Boss | Where |
|---|---|
| **Bramblemaw** | Act I — the Seal of Root |
| **The Stone Guardian** | Act II |
| **The Drowned Warden** | Act IV — the marsh |
| **The Warden, Bound** | Act V — the Rite of the Vale |
| **Magister Voss** | Act VI — keeper of a 240-name ledger |
| **The Hollow Celebrant** | Act VI — wrote the Rite |
| **The Warden, Unbound** | The last fight — 5 phases |
| **The Dragon** | Guards the Dragon's Den |

The ending is binary at the door — **Awaken it** (→ *The Wild Vale*) or **Bind it** (→ *The Quiet Vale*) — with a third, **Warden of the Vale**, reachable depending on how Halvard read you along the way.

### The Key Hunt

Optional, available from Act I — six beast-guarded Keys, any order, any level you dare:

| Key | Keeper | Reward |
|---|---|---|
| **The Bough Key** | Greater Wolf | Warden's Recurve (bow) |
| **The Cairn Key** | Greater Bear | Valescythe (180° sweep) |
| **The Ford Key** | Centaur | Valebreaker Warbow |
| **The Mire Key** | Mire Serpent | Serpentbane |
| **The Ash Key** | Greater Tiger | The Polished Shield (fireproof) |
| **The Dragon's Den** | The Dragon | Dragon-scale Armour |

One ordering is forced: the Den refuses anyone not carrying the Polished Shield, so the Ash Key comes first. Every Key also grants an Ancient Rune, spent at the Altar.

### Combat & Gear

Six axes — melee, a two-handed heave, a guard, the bow, stealth, and mounted combat — all resolved through one damage function, so a boss's phase multiplier, a rune's fire damage and an armour piece's mitigation all compose correctly together.

The bow is rated by **reach** (60–120 m); inside it, the crosshair turns red and a headshot kills outright, except four tougher animals that are headshot-proof. Gear runs five ladders: **19 melee weapons, 9 bows, 15 armour pieces, 7 shields**, plus enchantments, wards and armour runes at the Altar — most items can also be forged at any anvil.

### Economy & Enterprise

- **Hunting** — hides and meat sold over the counter, prices varying village to village; ore comes only from kills and raider strongboxes — there is no mining
- **The Tradehouse** (3,000 coin, Wold Cross) — six ores traded live across all seven villages
- **Deeds** — twelve buyable properties, each paying rent on a timer
- **Escort contracts** — ride shotgun on a wagon; what survives the raid decides the payout
- **Ten standing jobs** from named villagers, offered only between chapters
- **Five horses**, each a step up in price, speed and charge damage
- Two tavern minigames at the Ale House — poker and a dice hare-and-hound race

### Controls

- **Mouse** — pointer-locked third-person camera; **V** cycles views
- **E** — interact · **F** — fast travel (closed mid-chapter or mid-escort)
- **N** — toggle minimap orientation · **T** — replay the tutorial
- **MMB / Q** — heave attack · **RMB** — guard

### Content, Counted

| | |
|---|---|
| Campaign chapters | **31**, across 6 acts |
| Bosses | **8** |
| Keys / side jobs | **6** / **10** |
| Named NPCs | **76** |
| Enemy / animal kinds | **23** / **10** |
| Settlements | **7**, plus the Fort |
| Melee weapons / bows | **19** / **9** |
| Armour pieces / shields | **15** / **7** |
| Buyable properties | **13** |
| Endings | **3** |
| File size | **9.1 MB**, one `.html` file |
| Est. completionist playtime | **~3 hours** |

---

## Part 2 — How We Built It

Verdant Vale took shape across many sessions between Sensei and Claude, under an engineering discipline built around one constraint that never moved.

### The Shape of One File

The entire game is `Verdant_Vale_version_FINAL(2).html` — **9.1 MB, 22,600 lines**, opening straight from `file://` with no server and no network request. It's four concatenated sections, kept editable only because a toolchain exists to split, edit and losslessly reassemble them:

| Section | Size | Contents |
|---|---|---|
| `p1_head.html` | 708 lines | DOM, CSS — HUD, radar, every modal |
| `p2_three.html` | 3,685 lines | Three.js r160, minified, inline |
| `p3_assets.html` | 4 lines | 101 GLB models (2.3 MB) + 23 textures (5.1 MB), base64 |
| `p4_game.js` | 18,200 lines | All gameplay logic, one module body |

No bundler, no module system — `file://` blocks cross-origin module loads for a single-file deliverable, so it's one script, organized by banner comments (`§ COMBAT RESOLUTION`, `§ THE TRADING COMPANY`) that double as the file's navigation.

### Mapping a 22,600-Line Codebase

One rule held throughout: **never load the whole file.** Instead:

- `split.sh` → `build.sh` → `check.sh` — a round-trip toolchain that finds section boundaries by **markers, not line numbers** (an earlier line-number version once silently truncated the game logic once the file outgrew its baseline; it now verifies every split byte-identical before trusting it)
- A static linter (`tdz.mjs`), written after a declaration-order bug silently killed the page twice with nothing but a blank timeout to show for it — now gates 381 top-level content-table declarations
- Every edit is an **anchored replacement** — asserts its target text appears exactly once before changing anything, so a bad match fails loudly instead of corrupting the build
- Generalized afterward into a standalone `HOW_TO_HANDLE_LARGE_FILE.md`, reused across every other large single-file game project in the portfolio

### Data Tables, Not Special Cases

Almost every system is **a table of plain objects, read by one resolver function** — `MISSIONS` (31), `WEAPONS`/`BOWS` (19/9), `ARMOR`/`SHIELDS` (15/7), `ENEMY_KINDS`/`ANIMAL_KINDS` (23/10), `SIDEQUESTS` (10), `VILLAGES`/`ESTATES` (7/12). Adding content means adding a row, not a new system. One materials map drives every forge recipe, one event stream (`missionEvent()`) feeds both the campaign and the side-quest tracker, and one damage resolver composes steel, arrows, enchantments and boss phase multipliers correctly by construction.

### A Procedural, Zero-Asset-File Pipeline

No asset files ship separately. Terrain is a noise field evaluated at runtime, not a mesh. The **101 GLB models** are generated entirely by a custom Python toolchain matched to the game's own inline GLB parser — `meshlib.py` (flat-shaded GLB writer), `hero.py`, `animals.py`, `buildings.py`, `weapons.py`, `guardians.py`, `wagon.py`, `audit.py` (geometry sanity checks), `render.py` (offline preview renders), and `inject.py` (base64-encodes the model set into the HTML). A couple of asset types skip the pipeline entirely — signs and sun/moon sprites are painted straight onto a canvas at runtime, no font file, no extra payload.

### Calibrating for Performance

- **Chunk streaming** — the 4 km world is never fully resident; terrain builds and releases around the player
- **Quality tiers chosen at boot**, driving shadow resolution, **draw distance**, and render resolution
- **Shared material sets**, one per surface type
- A **fixed arrow pool** (26) instead of spawning a mesh per shot
- 40-minute timers run through a **frequency scheduler** at 1 Hz, never per frame
- Radar redraws at **12 Hz**, the map at **~4.5 Hz** — not 60 Hz

Typical boot figure: **~396 draw calls, ~67k triangles**.

### A Save File That Survives Its Own Future

Four slots plus an autosave in `localStorage`, schema-versioned, every bump shipping **with a migration** — an older save is upgraded on load, never refused. Long timers are stored as absolute due times, not countdowns, so they keep ticking while the tab's closed, with offline catch-up capped. Mission state is **derived, not trusted**, on load — recomputed from progress rather than restored verbatim, so an old save carrying a long-fixed bug quietly heals itself.

### Verification Discipline

**29 automated test suites, ~1,040 assertions**, run against the real build with Playwright:

- **Play the game, don't read the tables** — the main suite walks all 31 chapters through real player affordances, not table cross-checks
- **Poll state, never sleep a fixed duration**
- **Read the data, not the animation** — dialogue is parked as data the instant it starts typing, so nothing races the typewriter effect
- **Reproduce before fixing, always**

Change discipline sits above all of it: every change is classified as a content-table edit, a new pipeline asset, a new system, or a structural change — each tier carrying its own required verification before it's done.

### Shipping Readiness

Before going public: zero external network calls, no `eval` or dynamic code execution, no free-text fields feeding an `innerHTML` sink, no URL-derived XSS vectors, every `localStorage` access guarded in `try/catch` — confirmed safe to host and share as-is.
