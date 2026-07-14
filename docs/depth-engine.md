# The Depth Engine — how to get "a kid can win, an expert finds chess"

*This is the crux of the whole project. Long Haul and Grease are the right
spirit, but as pitched they have a low skill floor and no ceiling — "buy low,
sell high, react to events" gets solved in a few plays. This doc is about the
structural property that made M.U.L.E. deep enough to still be studied 40 years
later, and how to build it into a food-truck / smuggling economy.*

---

## What that property actually is

Two things at once, and they're in tension:

- **Low floor:** a casual player makes intuitive moves and does fine — sometimes
  wins. They're never mathematically eliminated and never need to understand the
  machine.
- **High ceiling:** an expert sees systems the casual doesn't, and those systems
  reward mastery *without ever being visible on the surface.*

The trap is thinking depth = more rules. It's the opposite. M.U.L.E. has very few
rules; the depth is **emergent** — it comes from a handful of simple systems that
interact, plus the other players. Our job is a *small* rule set that produces a
*large* strategic space.

---

## The seven mechanisms that generate the ceiling

These are the levers. M.U.L.E. used most of them; buy-low-sell-high uses none.

### 1. Endogenous, elastic prices — *the market reacts to you*
Prices move because of what players **do**, not just random events. Buy a lot of
an input and its price rises for everyone; over-serve a neighborhood and the next
unit sells for less (marginal utility). This is the single biggest source of
M.U.L.E.'s depth: every price a player can move is a **lever an expert pulls and
a casual just reacts to.** A random-price game can't be mastered; an endogenous
one can't be exhausted.

### 2. A scarce chokepoint — *the smithore lesson*
In M.U.L.E., everyone needs smithore to build mules, it's scarce, and an expert
can **corner it** and tax the whole table. One system like this adds enormous
depth for one rule. Our version: **prime locations are scarce** (one truck per
corner), and each game has **one rare "hero ingredient"** that's high-margin and
limited. Casuals don't notice the chokepoint; experts fight over it.

### 3. Interlocking loops that compound — *invest vs. cash in*
Every round: take profit now, or reinvest into capacity that pays more later. A
small early edge should **snowball** through the loops (more capacity → more
time → more development → more capacity). A casual cashes in and has fun; an
expert front-loads investment and pulls away. (Rubber-banding, below, keeps the
casual in it anyway.)

### 4. Demand you can *shape*, not just chase
The expert layer Grease was missing. Beyond serving who's hungry, you can
**manufacture demand you're positioned to satisfy** — a signature dish that
permanently bends a neighborhood's taste toward the ingredient you've cornered.
Casual: serve the crowd. Expert: build the crowd.

### 5. A semi-coop meter with a *manipulable* threshold
The shared "don't sink the ship." The city's foot traffic / vibrancy grows if
vendors keep the crowd happy and shrinks if everyone gouges or leaves blocks
unserved — a smaller pie for all. The depth isn't the meter; it's that an expert
knows **exactly how much they can free-ride or starve a rival before it tips.**
That's a social/timing read that's different with every group and never gets
solved.

### 6. Legible-but-lagged information — *foresight is a skill*
Casuals see the current board. Experts see the **trend** and the partial
**forecast** of next round's crowd and events, and pre-position. Give real but
incomplete forward info so prediction is rewarded skill, not a blind guess.

### 7. Convertibility with friction & timing
Cash → ingredients → served meals → cash → investment, each with a rate and a
timing window. Experts optimize the whole cycle; casuals do the one obvious
conversion. This is what makes it feel like an *engine* you're tuning.

---

## Instantiated: *"Night Market"* (working title)

A fusion that wears either skin — food trucks at a night market, or smugglers
working a run of ports. Same engine. Described here as the food version because
it reads best on a TV.

**Setup (procedural every game):** a city of 4–6 neighborhoods on the TV map,
each with a different demand profile, plus a wholesale district. One ingredient
is randomly the game's scarce **hero ingredient**. Map, demand, hero, and event
deck reshuffle each game.

**Resources:** 3–4 dish categories (e.g. Savory / Sweet / Spicy / Fresh), each
made from base ingredients bought wholesale. Kept few, for legibility.

**The two elastic markets:**
- *Supply:* wholesale ingredient prices **rise when the table buys heavily**,
  decaying back to baseline over rounds. (Mechanism 1)
- *Demand:* each neighborhood's hunger per category **regenerates and is
  consumed** as you serve; over-serving drops the per-unit price. (Mechanisms 1, 4)

**Geography:** your truck sits in one neighborhood per round; moving costs time.
You can't be everywhere — positioning is spatial arbitrage. (Long Haul's DNA)

**Time budget (the consumption pressure):** limited "prep actions" per round —
buy, move, cook, upgrade all cost time. The hard constraint that forces
priorities, exactly like food = time in M.U.L.E. You can **invest in capacity**
to earn more time. (Mechanisms 3, 7)

**Chokepoints:** prime corners (scarce), and the hero ingredient (rare,
high-margin). (Mechanism 2)

**Investment options** for profit: truck upgrades (more time/capacity), a
**signature dish** (permanently bends a neighborhood's demand toward your
specialty), a commissary (cheaper prep). These compound. (Mechanisms 3, 4)

**Shared meter:** the market's **vibrancy / foot traffic** — grows if the crowd's
kept happy, shrinks if vendors gouge or leave blocks starving, changing the size
of the pie for everyone. Caps final scores if it collapses. (Mechanism 5)

**Events (semi-predictable):** a festival spikes one block's demand, an
influencer fixates on one dish, an ingredient shortage (supply shock), a health
inspector who targets the leader (rubber-band). You see a partial forecast a
round ahead. (Mechanism 6)

**Win:** most Cash + asset value after N rounds — *if* the market didn't collapse.

---

## Proof it has both floor and ceiling

Same systems, two players:

| System | Casual player | Expert player |
|---|---|---|
| **Ingredient prices** | "Chili's cheap, I'll grab some." | Buys the cheap chili *because* the forecast implies a spicy-demand spike no one else is positioned for — corners supply before the price moves. |
| **Neighborhoods** | Parks in the busiest block. | Parks one block over — thin competition, unserved demand, better margins — and lets rivals saturate the prime block and crash their own price. |
| **Serving** | Sells until out of food. | Stops before saturating a block (marginal price drop); splits inventory across two demand pools to hold the per-unit price up. |
| **Profit** | Restocks and keeps rolling. | Buys a signature dish that bends a block's taste toward the hero ingredient they've cornered — demand only they can cheaply serve. |
| **Shared vibrancy** | Ignores it; just sells. | Times one round of gouging for the finale, when the meter has no rounds left to punish them. |
| **Events** | Reacts when they hit. | Pre-positions the round before, off the forecast. |

The casual is playing a perfectly fun game of "sell food to hungry people" and,
with one lucky festival, can win. The expert is playing three moves of a machine
the casual can't see. **Neither is wrong; they're at the same table.**

### The "chess move" — one worked expert combo
Early game, the expert notes chili is this game's hero ingredient and Riverside
has latent spicy demand. They (1) **corner cheap chili** while no one's competing
so the price stays low, (2) **invest in a signature spicy dish** that bends
Riverside's taste toward spicy over the next rounds, and (3) now Riverside
*craves* spicy and the expert owns the only cheap chili to serve it — a
self-reinforcing loop rivals can't cheaply break, because chili is now expensive.
That's an engine built from three simple, legal moves. A casual never sees it —
and still might beat them if the health inspector (leader-targeting event) walks
into the expert's truck at the wrong time.

---

## Why it stays deep for years (long-term playability)

The ceiling doesn't get "solved" because:

- **The market is game-theoretic, not a puzzle.** Cornering only works if others
  don't contest it; the right move depends on what the *table* does. Reading
  opponents is a skill that never bottoms out — this is exactly why M.U.L.E. is
  still dissected decades on.
- **Procedural setup** changes the optimal engine each game — a different hero
  ingredient and demand map means last game's winning line is this game's trap.
- **The semi-coop read** is different with every group and mood.

Depth that lives in *dynamic player interaction* is inexhaustible in a way that
depth living in a fixed optimal strategy never is.

---

## How the floor stays low (so a kid still wins)

- **Variance** from events and crowd randomness.
- **Rubber-banding** — leader-targeting events, demand redistributing toward
  under-served (often trailing) players.
- **Good-enough heuristics** that genuinely work: buy cheap, serve the hungry,
  don't run out, don't be greedy.
- **The shared meter** stops the leader from scorching the earth.
- **A high-margin luck play** available to anyone who reads a single event right —
  a catch-up lane that doesn't require understanding the whole machine.

---

## Open question for you

Is *Night Market* (the fusion) the right vessel for this engine, or do you want
the engine dropped into a straighter **Long Haul / smuggling** frame (ports
instead of neighborhoods, patrol risk instead of a health inspector)? The seven
mechanisms port cleanly to either — the choice is which world your family wants
to spend game night in. Once that's picked, the next step is to **paper-prototype
just the elastic market + one chokepoint** and confirm the depth is real before
anything gets built.
