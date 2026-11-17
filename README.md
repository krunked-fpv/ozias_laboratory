# ⚡🐉👑 Ozias's PokéMath League! 👑🐉⚡

### *Multi-Grade RPG Battle Arena, Speed-Catch Matrix & Living Pokédex Quest*

[](https://krunked-fpv.github.io/ozias_laboratory/)
[](https://github.com/krunked-fpv/ozias_laboratory)
[](https://github.com/krunked-fpv/ozias_laboratory)
[](https://krunked-fpv.github.io/ozias_laboratory/)

**[🎮 LAUNCH OZIAS'S POKÉMATH LEAGUE (krunked-fpv.github.io/ozias_laboratory) 🚀](https://krunked-fpv.github.io/ozias_laboratory/)** • **[📦 GitHub Repository (`krunked-fpv/ozias_laboratory`)](https://github.com/krunked-fpv/ozias_laboratory)**

## 🌟 What Is This Repo?

Welcome to **`ozias_laboratory`**—a custom-built, Pokémon-inspired math RPG and interactive training arcade engineered for **Trainer Ozias** (and his co-op tag-team partner, **Mom Marisa**)!

Because Ozias is a 3rd grader who loves math and is already excelling well beyond standard classroom worksheets, this app features a live **Multi-Grade League Difficulty Dial** right in the top bar and Command Center. With one click, Ozias or Marisa can dial the math engine from **3rd Grade Core (Lv.30)** all the way up through **4th Grade Boost (Lv.40)**, **5th Grade Challenger (Lv.50)**, **6th Grade Master League (Lv.60+)**, or turn on **⚡ Adaptive Evolution Mode** so questions automatically scale up as his winning streak grows!

## 🛡️ 3-Tier Persistence Architecture (`Local Sync` + `HTML Baker` + `Shadow-Cookie Auto-Healer`)

To guarantee that Ozias's **16-Creature Living Pokédex**, **5 Official League Gym Badges**, **Trainer XP**, **PokéCoins**, **12×12 Power Matrix gold cells**, and **Ozias & Mom Tag-Team Log** are never lost on page refresh or tablet/phone browser cache cleanups, `index.html` runs a 3-tier self-healing persistence system:

| Persistence Layer | Header Control / Engine | How It Protects Ozias & Marisa's League Progress |
| :--- | :--- | :--- |
| **1. Top-Bar `🔄 Reset Daily` & Session Controls** | Top-Bar Controls & `📋 Trainer & Mom Hub` | Resets daily warmups, active sprint timers, and scratchpad canvases for a fresh training session while **preserving** cumulative Trainer XP, PokéCoins, Partner Evolution stage, 5 Gym Badges, 16-Creature Pokédex catches, and Ozias & Mom Co-Op logs. |
| **2. Self-Contained `💾 Local Sync` & HTML Baker** | `🟢 Local Sync Ready` pill + `💾 Local Sync` button + `<form id="ozias-inline-state-form">` + `window.__OZIAS_POKEMATH_STATE__` | Modeled after the [Discogs Vinyl Vault](https://github.com/krunked-fpv/discogs_collection) and [Violet's Championship Quest](https://github.com/krunked-fpv/violets_homework). Click **💾 Download Updated Game HTML (Bake Progress In)** to download a self-contained `index.html` with Ozias's latest catches, XP, and badges permanently baked into the file, or export/import `ozias_pokemath_sync.json` and clipboard sync codes. |
| **3. Shadow-Cookie Auto-Healer (`kv1_*`)** | `<script id="krunked-cookie-vault-v1">` in `<head>` (400-day `SameSite=Lax` cookies) | Injected into `<head>` before the RPG script runs. Hooks `Storage.prototype.setItem`, `removeItem`, and `clear`, automatically strips transient base64 Battle Scratchpad `<canvas>` buffers (`data:image/...`) to stay under the browser's 4 KB per-cookie limit, chunks `ozias_pokemath_league_v1` into 3.2 KB cookies (`Max-Age=34560000`), automatically restores `localStorage` at boot if evicted by a tablet or phone OS, and updates the shared root `krunked_family_pulse` (`Path=/`) cookie across `krunked-fpv.github.io`. |

### Patching, Rollback & Console Diagnostics

* **One-Command Ad-Hoc Patcher (`bolt_on_cookie_persistence.py`):**
  ```bash
  # Patch ozias_laboratory index.html with automatic .cookie_bak backup
  python bolt_on_cookie_persistence.py C:\path\to\ozias_laboratory

  # Restore from .cookie_bak backup if needed
  python bolt_on_cookie_persistence.py --rollback C:\path\to\ozias_laboratory
  ```
* **Browser Console Telemetry:** Run `window.__KRUNKED_COOKIE_VAULT__.status()` in the browser console anytime to inspect active `kv1_*` shadow cookie chunks, byte sizes, and the shared `krunked_family_pulse` summary across [ozias_laboratory](https://krunked-fpv.github.io/ozias_laboratory/), [violets_homework](https://krunked-fpv.github.io/violets_homework/), and [discogs_collection](https://krunked-fpv.github.io/discogs_collection/).

## 🎚️ The 5-Mode Grade Level Difficulty Dial

| League Tier | Level | Core Math Skills Unlocked |
| :--- | :--- | :--- |
| 🪨 **Boulder League (3rd Grade Core)** | **Lv. 30** | Multiplication & division facts ($0\text{–}10$), 3-digit addition & subtraction with regrouping, unit fractions, and area/perimeter of rectangles. |
| 🌊 **Cascade League (4th Grade Boost)** | **Lv. 40** | Full $12 \times 12$ fact mastery, 2-digit $\times$ 1-digit multiplication, division with remainders, equivalent fractions, 4-digit operations, and 1-step $x$-variable puzzles. |
| ⚡ **Thunder League (5th Grade Challenger)** | **Lv. 50** | 2-digit $\times$ 2-digit partial products, long division, decimal operations, percentages ($10\%, 20\%, 25\%, 50\%, 75\%$), order of operations (PEMDAS), and 3D prism volume. |
| 🐉 **Dragon League (6th Grade Master)** | **Lv. 60+** | Exponents ($2^5, 4^3, 11^2$), negative integer operations, ratios & unit rates, percentage discounts, and 2-step algebraic equations ($4x + 20 = 100$). |
| 🌟 **Adaptive Auto-Dial Mode** | **⚡ AUTO** | Starts at 3rd Grade Core and automatically evolves up to 4th, 5th, and 6th Grade Master problems as Ozias builds a $3+$, $6+$, and $9+$ streak! |

## 🕹️ Inside the 6 PokéMath League Arenas

### 🎛️ Arena 0: League HQ, Grade Dial & Starter Partner Evolution
* **4 Starter Partner Lines (3 Evolution Stages Each at `150 XP` & `350 XP`):** Pick **Voltchu** ($\rightarrow$ *Thunderpounce* $\rightarrow$ *Stormlux Rex*), **Pyrokit** ($\rightarrow$ *Blazefang* $\rightarrow$ *Infernodrake*), **Aquafin** ($\rightarrow$ *Torrentshell* $\rightarrow$ *Hydroleviathan*), or **Leafsprout** ($\rightarrow$ *Verdantclaw* $\rightarrow$ *Terradon Prime*).
* **👩‍👦 Ozias & Mom (Marisa) Tag-Team Mode:** Toggle between **Solo Trainer Mode** and **Pass & Play Co-Op Mode** where Ozias and Mom alternate turns launching attacks and racking up team points!
* **⚡ Elemental Power Surge Orbs:** 4 instant mental-math warmup cards across Electric ($\times / \div$), Fire ($+ / -$), Water (Fractions/$\%$), and Psychic (Algebra/Geometry).

### ⚔️ Arena 1: Wild Creature & Gym Boss Battle Arena
* **Turn-Based RPG Math Combat:** Battle wild elemental creatures and summon **Epic Gym Leader Bosses**! Answering in under 8 seconds lands a **CRITICAL HIT ($1.5\times$ Damage + Bonus PokéCoins)**.
* **Choose Your Attack Move Type:** Filter your attacks by **⚡ Bolt Strike ($\times / \div$)**, **🔥 Flame Charge ($+ / -$ & Place Value)**, **🌊 Hydro Pulse (Fractions & Percents)**, **🔮 Psychic Beam (Algebra & Geometry)**, or **🌟 All Moves**.
* **🔍 Poké-Scanner Visual Strategy Hints:** Reveals non-spoiler mental-math strategies (Area Splits, Fact Families, PEMDAS rules, or Algebra Balance Scales) without breaking your streak.
* **✏️ Built-In Digital Scratchpad Canvas:** Work out multi-step calculations right beside the battle screen using a mouse, finger, or tablet stylus!

### 🔴 Arena 2: Poké-Ball Speed Catch & Interactive $12 \times 12$ Power Matrix
* **Mode 1 — Speed-Catch Blitz:** Run a **60s Quick Ball**, **90s Great Ball**, **3-Minute Ultra Ball**, or **Untimed Zen Mode** sprint to build your combo multiplier and high score.
* **Mode 2 — Interactive $12 \times 12$ Power Matrix:** Click any cell on the 144-fact board (or hit *Challenge $\times 6, \times 7, \times 8, \times 9$*) to solve fact families and light up both commutative twins in gold! Lighting up 12 cells unlocks the **Cascade Badge**!

### 🧪 Arena 3: Professor's Lab — Mega-Split, Fraction Reactor & Story Quests
* **💥 Part 1 — Mega-Evolution Area Split:** Visual SVG area model blueprint that splits 2-digit multiplication into Friendly Tens + Ones boxes (e.g., $24 \times 7 = (20 \times 7) + (4 \times 7) = 140 + 28 = 168$).
* **🧪 Part 2 — Potion Fraction & Ratio Reactor:** Dual visual Hyper Potion energy bars for comparing, adding, and converting fractions, decimals, and percentages.
* **🗺️ Part 3 — Ozias & Marisa Gym Leader Story Quests:** Multi-step Pokémon adventure word problems tailored to the active Grade Dial, complete with a step-by-step blueprint detector.

### 🎮 Arena 4: Volt-Runner Arcade Mini-Game (`<canvas>`)
* Steer Ozias's active Partner across **3 Sky Lanes** (Up / Middle / Bottom) using **Up/Down Arrow Keys**, **W/S**, or the on-screen touch lane buttons to fly through the gate displaying the correct solution to the live equation at the top of the screen!

### 📖 Arena 5: Living Pokédex (16 Creatures) & 5 League Gym Badges
* **16 Collectible Creatures:** Every creature defeated in the Battle Arena (or unlocked via **100-Coin Mystery Capsules**) joins Ozias's Living Pokédex with custom SVG artwork and spoken math lore.
* **5 Official Gym Badges:** Earn the **Boulder**, **Cascade**, **Thunder**, **Rainbow**, and **Master Dragon** badges to awaken **#016 Legendary Astralux**!

## 🛠️ Tech Stack & Zero-Dependency Portability

* **100% Single-File HTML5 (`index.html`):** Self-contained HTML, CSS, custom SVG creature artwork, and Vanilla JavaScript—zero build steps or external dependencies required.
* **3-Tier Offline & Cookie Persistence:** Combines `localStorage`, inline hidden `<form id="ozias-inline-state-form">` HTML baking (`window.__OZIAS_POKEMATH_STATE__`), JSON export/import (`ozias_pokemath_sync.json`), and the `<script id="krunked-cookie-vault-v1">` Shadow-Cookie Auto-Healer.
* **Web Audio API Synthesizer & Web Speech API:** Custom retro RPG attack sounds, Poké-Ball catch fanfare, and text-to-speech question/lore reading with a one-click mute toggle.

## 🚀 Quick Start & GitHub Pages Deployment

1. **Play Online:** Visit **[krunked-fpv.github.io/ozias_laboratory](https://krunked-fpv.github.io/ozias_laboratory/)** on any laptop, tablet, or phone.
2. **Run Locally (Zero Install):**
   ```bash
   git clone https://github.com/krunked-fpv/ozias_laboratory.git
   cd ozias_laboratory
   open index.html
   ```
3. **Save or Transfer Progress Across Devices:** Click **`💾 Local Sync`** in the top header bar to download an updated `index.html` with all current progress baked inside, or export/import `ozias_pokemath_sync.json`.

### ⚡ Built with Love for Trainer Ozias & Mom Marisa • Gotta Solve 'Em All! 🐉🏆
