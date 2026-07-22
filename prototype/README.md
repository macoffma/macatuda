# Playable greyboxes

Self-contained, single-file prototypes. Open any in a browser (phone, iPad,
laptop) — no build, no install.

- **`the-block.html` — The Block, integrated build (current, v0.9).** The real
  loop, with the haul-and-claim woven in. The "drum up work" phase is a **canvas
  neighborhood** — winding streets, building graphics, parks and vacation lots
  (unplayable) — packed with **~12 houses** (so the block doesn't run dry across a
  multi-trip day) and **corner lemonade stands** you haul to and run yourself
  (your own venture, not a job at a house). You **haul your cart** to a house to
  claim its job (that *is* your knock) or to a stand to set up. Travel spends
  daylight (street distance), so *which* node you pick is the strategic cost.
  Hiring → the work beat (mowing micro-game / touch-for-tips) → payday; not hiring
  → a bust; a stand → sell over the afternoon. Rivals take their turns between
  yours and glide to their spots as nodes grey out. Day ends → **garage sale: a
  live, timed auction** — one scarce item at a time (one of each tool on the
  block — win it and that niche is yours), a countdown, and the other kids bidding
  against you — → **end-of-day reveal** (stacked earnings bars) → end-of-summer
  scoring. Keeps the whole economy (earned skills, tools, weather-hot double-pay
  jobs, goodwill, fair AI). Verified headless across many full summers: zero
  errors, loop always completes, rivals competitive, tools stay exclusive. Still
  deferred: the *live simultaneous* swarm (rivals move between your trips, not all
  at once). Built on the feel-test in **`the-block-haul-demo.html`** (v0.6).
- **`the-block-greybox.html` — The Block, pre-haul greybox (v0.4/0.7).** A
  neighborhood summer hustle on a **procedural map** — you *drum up* work, you
  don't pick it off a board. Key systems: **knock on doors** to prospect (read a
  house's cues — 🌿 lawn, 🧸 kids, 🐕 dog, 🍂 leaves, 🚗 car — plus the weather to
  guess who's hiring; a bad read gets "not today" and a wasted walk); **set up
  your own stand** (lemonade/cider) at a corner as your weather-driven venture;
  base pay is a safe floor with **tips as the press-your-luck**; a **Daylight
  budget** is the master scarcity (travel + jobs + each polish all spend it);
  the map's **distances and house quirks** are learned each game; **door/corner
  races** (closest rival wins — the M.U.L.E. plot-grab); and **Neighborhood
  Goodwill** as the commons. New in v0.4: **skill tracks** per work type that
  level up as you *do* the work (more pay, fewer flubs — getting good is earned,
  not bought); a **store that sells tools** mapped to each track (mower, lemonade
  cart, wagon), so purchases follow what you're becoming good at; and a
  **M.U.L.E.-style end-of-day reveal** — everyone's earnings broken down by work
  type as stacked bars, what you left on the table (flubbed tips, wasted walks,
  jobs undone), and your skills leveling up. v0.5 fixes: tools now light a **gold
  dot** on their track (so a tool visibly boosts that capability), rivals now
  **prospect with the same uncertainty you do** (they read cues and sometimes
  strike out, instead of having perfect info), and a **fair-clock fix** so rivals
  advance by daylight spent rather than by your number of turns — verified fair
  (symmetric play ≈ even; a tool-buying human gets a gentle edge). v0.6 adds a
  **mowing micro-game** (one job type, as a test): instead of a dice-roll tip,
  tap when the mower's in the green to lay a neat stripe — the zone narrows and
  speeds up each stripe (press-your-luck as *skill*), and a miss veers into the
  flowerbed. Only the tip layer is skill-based; base pay and the map/economy
  strategy are untouched. The other jobs still use the dice tip, so you can feel
  the difference side by side.
- **`overboard-greybox.html` — Overboard (earlier fishing version).** Kept for
  reference; same core loop with a fishing skin. The notes below describe it.

---

# Overboard — Greybox v0.4

`overboard-greybox.html` is a **self-contained, playable slice** of the Overboard
core loop. One HTML file, no build step, no dependencies — open it in any browser
(phone, iPad, laptop) and play. You skipper against AI rivals.

## What it's for

To answer the only questions paper can't: **does the loop feel fun, and does the
economy feel alive?** Specifically it puts these in your hands:

- **Blind spot-picking** — you read a rumor of the water but can't see the exact
  catch until you fish it.
- **Press-your-luck reeling** — cast for one more fish or bank your hold; three
  snags and the line snaps and you lose your best catch.
- **Catch of the Day** *(v0.4)* — the economy, felt not calculated. Each day the
  town craves one fish (shown as dots, à la M.U.L.E.) that pays double until their
  appetite's full. Chase it, and race rivals to the dock — no forecasts, no price
  ladders, no spreadsheets.
- **Fun-first fishing** *(v0.4)* — the catch is the star: reveals with a bit of
  delight ("A TUNA! The big one!"), the snap is "the one that got away," fish are
  icons not columns of numbers, and money buys *fun boat gear* (Fish Finder,
  Strong Line, Bigger Boat) — bought with coins, not financial instruments.
- **The commons** — spots you strip below survival die; hammer the bay and it
  collapses, halving everyone's coins. (Verified: reachable via greedy play,
  avoidable with care.)
- **AI rivals** — Reef Hog (greedy), Old Salt (steady), Barnacle (chaos).

> **v0.4 note:** this was a deliberate *simplify + fun* pass. Earlier builds
> (v0.2–v0.3) grew a finance layer — price forecasts, ladders, net-worth math,
> overnight holding — that made it read like a trading terminal. v0.4 strips that
> out and puts the joy of fishing first, keeping the depth (read the water, chase
> the wanted fish, press your luck, mind the bay) but *felt*, not computed.

## Deliberately NOT in this version

This is a *mechanics* greybox. Out of scope on purpose, until the loop proves fun:

- **Multi-device play** (the real TV-hub + iPad vision). This runs on one screen
  vs. AI. Networking is the expensive, least-informative thing to build first.
- **Hidden-info hotseat** for multiple humans (secret simultaneous spot-picking).
- **Art, sound, characters** — and deeper economy modules (a cannery /
  demand-shaping, quotas) beyond the three starter upgrades.

The engine (`STATE` + rule functions) is kept separate from `render()` on purpose,
so it can later be lifted onto a server for the networked build.

## How it was checked

Driven headless through 20+ full seasons (2–4 players): zero JS errors, the loop
always completes, prices move on dumps, and the sea collapses only under
sustained overfishing — never in careful play.

## What to notice while you play (the real test)

- Do you *instinctively* stop dumping to protect a price — without being told to?
- Does "cast again?" make you wince and grin?
- Do you start eyeing the sea-health bar and easing off?
- Could a kid coast on steady Cod money while you chase the Trench's tuna?

Jot down what felt great and what dragged. That's the input to v0.2.
