# Family Game — Concept Exploration (Phase 1)

*Goal of this phase: find the fun on paper, before committing to a theme, rules,
or a single line of code.*

---

## 1. What we're chasing

Distilled from the brief and from what made **M.U.L.E.** great:

| Pillar | What it means for us |
|---|---|
| **Short** | One game runs **15–30 min**. Sit down, play, done. Never a 3-hour Catan slog. |
| **Easy in, deep down** | A **10-year-old has fun on turn one**; an adult finds real strategy underneath. Depth is *optional*, never a wall. |
| **Character-driven & funny** | Personality, little stories, slapstick events — over graphs and spreadsheets. |
| **Lightweight resource management** | 3–4 resources you juggle and trade. Enough to think about, not enough to stall. |
| **Different every time** | Procedural setup + shuffled events + character mix = high replayability. |
| **AI that monkeys things up** | Computer players with *personalities* who inject chaos and fill empty seats. |
| **Readable, stylized art** | Charming and clear beats high-fidelity. Not forced-8-bit, not AAA — think "cozy storybook." |

### The four things M.U.L.E. actually got right (our secret sauce)

These are the mechanics we most want to carry forward — the rest is theme:

1. **Forced interdependence.** No one can produce everything they need well, so
   players *must* trade. This is what turns an economy into a social event.
2. **A live auction.** Real-time, supply-and-demand pricing where buyers and
   sellers meet in the middle. It's tense, loud, and the highlight of every game.
3. **Semi-cooperative tension.** You're competing to win, but if the *whole
   colony* fails, everyone suffers. "Beat your neighbor, but don't sink the
   ship" is the magic.
4. **Random events as a story engine.** Sunspots, pests, wandering mules — the
   "remember when…" moments that make each game a story, plus a natural
   rubber-band to keep a losing kid in it.

---

## 2. The platform pattern (TV hub + iPad controllers)

This is the "Jackbox / Mario Party" split, and it's a genuine design gift: it
lets us separate **public drama** from **private decisions**.

**On the TV (the shared hub):**
- The valley/board, growing and changing
- The live **market ticker** during auctions
- Event announcements and dramatic reveals
- Scoreboard + the shared "prosperity" meter
- Round timers and turn drama
- The AI players, shown as characters with faces and reactions

**On each iPad (your private cockpit):**
- Your resources, money, and household status
- Your character and their quirks
- Secret plans and this round's private choices
- Your bids and asks in the market
- Optional light dexterity mini-games (tap to harvest, drag to haul)

**How the AI shows up:** each computer player is a character *on the TV* with a
portrait, a name, and a personality — they bid, trade, react, and occasionally
do something chaotic. They're opponents you can see and boo at, not invisible math.

**Tech note (for later, not now):** the lowest-friction path is a **web app**.
The TV opens a room and shows a code; iPads join in a browser — no App Store, no
installs, works on any tablet. That's a Phase 2+ decision; flagging it because it
shapes what's cheap to build.

---

## 3. Flagship concept — *"Hearth & Haul"* (working title)

> A band of animal pioneers settle a new valley every game. Claim your land, put
> goofy critter-helpers to work, weather strange seasons, and haggle in a live
> market — get your family richest without letting the whole valley go bust.

This is the most direct spiritual heir to M.U.L.E., modernized so nothing is
twitchy or punishing for a kid.

### A round (a "Season"), start to finish

A game is **4–6 Seasons** (4 ≈ 15 min, 6 ≈ 25 min — that's your length dial).

1. **Claim.** The TV shows a freshly generated valley — a grid of plots with
   terrain: rich soil, windy ridges, ore veins, ponds. Everyone picks a plot to
   claim *at the same time* on their iPad, with a short timer. Light land-grab
   tension, no reflex contest. Ties settle with a quick coin-flip or micro-bid.

2. **Outfit.** You drop a **Critter Helper** (our goofy "MULE") onto your plot,
   tuned to make one resource: **Food**, **Spark** (energy), **Ore**, or the
   luxury **Gleam**. Terrain multiplies output, so matching helper to land is the
   core little puzzle. Costs money + ore to build.

3. **Work.** Resources auto-produce (plot × helper × terrain). An *optional*
   iPad mini-game — tap-to-harvest, keep-your-critter-happy — gives a small
   boost. Skippable, so a distracted kid isn't punished; rewarding for an
   engaged one. Your household **eats Food**; go hungry and you get fewer actions
   next Season. (That's M.U.L.E.'s time-pressure, made gentle.)

4. **Event.** The TV rolls a **Valley Event**: a sunny spell (Spark ×2), a berry
   glut (Food price crashes), a traveling merchant, a raccoon bandit who nabs
   ore, a festival that spikes Gleam demand. Some hit everyone, some target the
   leader (rubber-band), some are pure opportunity. This is the chaos + story engine.

5. **Market — the star.** A **live, real-time auction** on the TV. Each resource
   has a price that rises and falls with supply and demand. Players and AIs set
   bids/asks on their iPads; the TV shows a moving ticker and matches trades as
   they happen. Because nobody can make everything, you *must* trade. The town
   store is a backstop at bad prices. A ~90-second cap keeps it snappy and loud.

6. **Tally.** Scores update on the TV — *and* a shared **Valley Prosperity**
   meter. If the colony's prosperity sinks too low (famine), everyone's final
   score gets capped. You want to win, but not by burning the village down.

**Winning:** most personal **Wealth** after the final Season — *but only if the
Valley survived.* That single rule preserves M.U.L.E.'s "compete hard, keep the
colony alive" tension, which is what makes the trading feel like it matters.

### Characters (asymmetry = identity + replay)

Pick a critter family; each has a fun perk and an honest downside:

- 🦡 **Moles** — dig Ore faster, but eat more Food.
- 🦉 **Owls** — peek at one upcoming event, but are slow to claim land.
- 🐸 **Toads** — thrive on wet plots and get a market discount, but make less Gleam.
- 🦊 **Foxes** — glimpse one hidden bid, but villagers distrust them (small prosperity ding).
- 🦔 **Hedgehogs** — start with extra Ore, but can't be robbed while curled up (skip one event).

Kids latch onto an identity ("I'm always the Owl"); adults find the strategy in the trade-offs.

### Why a 10-year-old has fun *and* there's real depth

- **Surface game:** grab a spot, plop a cute helper, sell your stuff, laugh at
  the events. Completely playable while ignoring all optimization.
- **Deep game:** terrain matching, timing the market, cornering a resource,
  reading events early, feeding your household, catch-up plays. The adults find
  it; the kids find the toys and the auction drama. Same table, different games.

---

## 4. Alternate concepts (or: modes of one engine)

A key insight: these aren't five separate games to build. The flagship's engine —
**hub + controllers + live market + event deck + prosperity meter** — can expose
most of these as **modes** or **dials**. That's the real Phase 2 recommendation:
build *one* engine, ship *several* experiences.

### B. *"Market Day"* — the party-mode, trading-frenzy version
Strip out the map. Everyone runs a festival stall; each round you get random
goods and secret orders to fill, and the **live auction is 80% of the game.**
Fastest to learn, most social, most Jackbox-like. **10–15 min.** Great as the
gateway mode — and honestly the easiest thing to prototype first.

### C. *"Sky Barons"* — airship logistics
Floating islands whose needs shift; you run cargo blimps doing pickup-and-
deliver plus market. More spatial/planning brain, still light. Skews a bit older
(maybe 12+). Good if the family wants more to chew on.

### D. *"The Undercurrent"* — hidden-saboteur mode (spicy)
Same colony, but one player (or an AI) is secretly the **Blight**, trying to make
the valley fail while looking helpful. Adds bluffing and social deduction on top
of the economy. A blast with the right table — but **read the room**: traitor
games can produce tears with younger or sensitive kids. Offer it as an optional
spicy mode, never the core.

### E. *"Seasons of Plenty"* — cozy co-op-leaning mode
Turn the confrontation dial way down: you're mostly carrying a shared town
through a hard year, competing only for "MVP of the Valley." Lowest conflict,
best for the youngest players or mixed-ability tables. It's the flagship with the
co-op dial turned up.

**The dials that turn one game into all of these:** map on/off, confrontation
level, hidden roles on/off, session length, and market volatility.

---

## 5. Mechanics worth stealing from M.U.L.E. (a toolbox)

Pick and mix as we prototype:

- **The double auction.** Buyers' price rises, sellers' falls, they meet in the
  middle; a store backstops both ends. The single best idea in the game.
- **Interdependent production.** Deliberately make each player good at making
  *some* things and short on others, so trade is forced, not optional.
- **The land-grab.** A quick, simultaneous claim phase with just enough
  competition to matter — without a reflex/dexterity gate.
- **Consumption pressure.** Something you must spend each round (food = time/
  actions) so hoarding has a cost and the clock feels real.
- **The colony meter.** A shared success bar that caps everyone's score if it
  fails — the semi-coop tension.
- **Escalating events.** Calm early rounds, wilder late ones — a natural
  "act structure" so the game builds to a climax.
- **Gentle rubber-banding.** Some events target the leader or help the trailer,
  so a kid is never mathematically eliminated before the end.
- **Asymmetric characters.** Small perk + small downside per character = identity
  and replay value for near-zero rules cost.

---

## 6. The replayability engine (why it's different every time)

- **Procedural valley:** terrain layout and resource richness reshuffle each game.
- **Shuffled, escalating event deck:** never the same sequence, always builds.
- **Character + AI line-up:** who's at the table changes the whole dynamic.
- **Variable win modifiers:** "this valley prizes Gleam double," etc.
- **Market volatility seed:** some games are calm markets, some are wild.

Any one of these alone gives variety; together they mean no two nights feel the same.

---

## 7. The AI "chaos player" cast

Fill empty seats *and* season the game with personality. You dial the table to
taste:

- 🦡 **Bramble the Badger** (hoarder) — buys up Ore and won't sell, spiking prices.
- 🐿️ **Pip the Squirrel** (gremlin) — random overbids and fire-sales; pure chaos. *Your "monkey up the works" pick.*
- 🐹 **Granny Vole** (steady) — plays it safe and stabilizes the market. A calm 3rd/4th seat.
- 🦦 **Slick the Weasel** (shark) — ruthless arbitrage that punishes bad trades. The "hard mode" opponent.

Example tables: *3 humans + Pip* for chaos night; *2 humans + Granny + Bramble*
for a fuller, calmer game.

---

## 8. Open questions to decide as a family

These shape everything downstream — worth a quick family vote:

1. **Who's playing, and what ages?** Sets the youngest-player floor and how spicy
   we can go (e.g. hidden-saboteur mode or not).
2. **How many at once?** 4 players + AIs? Do we ever need 5–6?
3. **Theme vote.** Cozy critters? Sky pirates? Space frontier? Undersea reef?
   The mechanics don't care — pick what your family will *love the look of*.
4. **How competitive vs. cozy?** Where's the confrontation dial for your family?
5. **Device reality.** How many iPads, and what's the TV situation (smart TV,
   Apple TV, a laptop plugged in)? Decides the lowest-friction build.

---

## 9. Suggested next steps

1. **Family theme + vibe vote** on the questions above.
2. **Paper-prototype the market first.** You can test the auction and the event
   feel *tonight* with index cards, poker chips, and a kitchen timer — no code
   needed. If the trading is fun on paper, we have a game. If it isn't, we saved
   ourselves months.
3. **Lock the flagship's core loop** (probably a trimmed *Market Day* to start),
   then decide the smallest fun thing to build first.

*Everything here is a starting point. Phase 1 is for finding the fun — react to
any of it and we'll push the good ideas further and drop the rest.*
