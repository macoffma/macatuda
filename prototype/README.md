# Playable greyboxes

Two self-contained, single-file prototypes of the same tuned engine, different
skins. Open either in any browser (phone, iPad, laptop) — no build, no install.

- **`the-block-greybox.html` — The Block (current direction, v0.3).** A
  neighborhood summer hustle on a **procedural map** — you *drum up* work, you
  don't pick it off a board. Key systems: **knock on doors** to prospect (read a
  house's cues — 🌿 lawn, 🧸 kids, 🐕 dog, 🍂 leaves, 🚗 car — plus the weather to
  guess who's hiring; a bad read gets "not today" and a wasted walk); **set up
  your own stand** (lemonade/cider) at a corner as your weather-driven venture;
  base pay is a safe floor with **tips as the press-your-luck**; a **Daylight
  budget** is the master scarcity (travel + jobs + each polish all spend it, so
  milking a neighbor trades against reaching another); the map's **distances and
  house quirks** are learned each game; heading for the **same door/corner as a
  rival is a race** (closest wins — the M.U.L.E. plot-grab); and the commons is
  **Neighborhood Goodwill** (a happy block pays everyone more).
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
