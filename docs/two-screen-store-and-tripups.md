# Design turn — two screens, the garage sale, and where players trip up

*The mechanics are landing. Now: strip words, split the game across the TV and
the phone, fix the store, and pressure-test for confusion. The bar you set:
"playable with a map and a listing of the competitors," like M.U.L.E.*

---

## 1. The two-screen split — the core idea

**The TV holds what's SHARED, AMBIENT, and DRAMATIC (everyone looks up).
The phone holds what's PRIVATE, TACTILE, and yours (you look down).**

The current greybox feels cramped because *one* screen is doing *both* jobs. Split
them and each gets to breathe — the TV becomes a game-show board, the phone becomes
three big buttons.

| Current element | Lives on… | Why |
|---|---|---|
| The neighborhood **map** | **TV** | The shared board. Everyone watches kids move, jobs light up and grey out. |
| **Competitor standings** (coins, avatars) | **TV** | Your "listing of the competitors." Big, glanceable. |
| **Weather / what's hot today** | **TV** | Shared context; one big icon. |
| **Day + the shared clock** | **TV** | Everyone's on the same day. |
| **Door-races & event drama** | **TV** | Animate it: a kid sprints to a house, "SNIPED!" pops. |
| **Garage-sale auction** | **TV** (+ phone paddles) | The centerpiece social moment (see §3). |
| **End-of-day reveal** (stacked bars) | **TV** | A great shared payoff — everyone sees who earned what. |
| Your **money / tools** | **phone** | Private, small. |
| **Where to go next** (pick a house) | **phone** | Tap your own mini-map; secret until revealed. |
| The **micro-game** (mowing, tips) | **phone** | Tactile, yours. |
| Your **bid** in the auction | **phone** | A paddle; secret until it lands. |

The phone stops being a whole dashboard and becomes *your cockpit for this one
decision.* The TV carries the state — so neither screen needs the wall of text the
single-screen greybox does.

---

## 2. De-wordify: "a map and a list of competitors"

Principles for the whole game:

- **Icon + color + position over words** — the M.U.L.E. dots. A house's job is a
  glyph, not a sentence.
- **Kill the prose log.** Replace "Chip babysat at the Reyes' for $8" with an
  animation on the TV: Chip's avatar at the house, coins pop, done.
- **Announce each phase BIG on the TV**, few words: `PICK A JOB` · `GARAGE SALE!` ·
  `PAYDAY`. That replaces paragraphs of instructions.
- **Numbers only where they're a decision** — your money, your bid, a job's pay.
  Not travel-times and percentages scattered everywhere.
- **Teach by watching, not reading.** First-timers learn the loop by seeing one
  round happen on the TV. One-time tooltips only; no standing hint text.

Litmus test: mute all the words and can you still play from the map + the
competitor list? That's the target.

---

## 3. The store is wrong — make it a Garage Sale (auction)

You couldn't name it, so here it is: **"why get better at leaf-blowing?" fails
because tool/skill investment is a lonely menu with no scarcity and no drama.**
There's no reason to commit to a niche.

**Your instinct — bid on tools like M.U.L.E. — fixes all of it at once:**

- **Scarcity → exclusivity.** There's *one* leaf blower at the sale. Win it and you
  *own* raking on this block. *That's* why you specialize — you hold the tool no one
  else has, so rake jobs are yours.
- **A shared, dramatic TV moment.** The auction was M.U.L.E.'s best beat. A garage-
  sale table on the TV, a mower up for bid, the price ticking, everyone leaning in.
- **Real depth for free** — bluffing, reading opponents, "do I let them have the
  mower and grab the wagon cheap?" That's the chess.
- **Emergent roles.** Limited tools mean the family naturally divides the block —
  you're the mower, your kid's the sitter, Dad runs stands. Very M.U.L.E.

**Keep it family-fast:** 3–4 items per sale, a quick ascending bid (or one-shot
sealed bids for the youngest), a spend cap so no one bankrupts themselves, ~60–90s
on the TV. A sale every couple of days, not daily.

**Simplification bonus:** this lets us **retire the murky XP skill-grind**. Tools
become the whole progression — scarce, visible, won in public. (Keep a *tiny*
"you've done this a lot, small bonus" if we want, but it's no longer the point.)
Fewer systems, more drama.

---

## 4. Where would a family trip up? (and the fix)

Walking a family — adults + a 10-year-old — through it:

1. **"Which screen do I look at?"** → Hard role separation: the phone *pushes* you
   to the TV at the right time ("👀 Look up — Garage Sale!"), and goes quiet
   (one button) when the action's on the TV.
2. **"Is it my turn?"** → The TV blasts the current phase and who it's waiting on.
   No ambiguity about act-vs-wait. (M.U.L.E. had crisp phases; keep that.)
3. **"Why didn't I get the job?"** (a blind-knock dud) → Make the cue-read
   *teachable* (🌿 on a sunny day = almost surely mowing) and the miss *funny*, not
   punishing. Show it on the TV so it reads as "bad luck/bad read," not a bug.
4. **"Why can't I do everything?"** (daylight) → A big shared sun/clock on the TV
   crossing the sky; when it's low, the TV says so. Kids feel time visually.
5. **"The auction is scary"** (young kids overbid) → Simple paddle (+$1 / hold),
   a spend cap, and the TV showing exactly what you'd win. Optionally a "buy-it-now"
   for the timid.
6. **"Why do I care if the block is grumpy?"** (the goodwill commons) → Make it a
   big, obvious face/mood on the TV that everyone sees change, tied to visible
   coins ("grumpy block = everyone earns less").
7. **Micro-game whiplash** → switching from map-strategy to a twitch bar. Keep
   micro-games short and only on *some* jobs so they're a treat, not a tax (we're
   keeping mowing's for now — watch whether it drags).
8. **Contention feels unfair** → when two kids race a door, *animate the race on the
   TV* so the loser sees "they were closer," not "the game took it from me."
9. **Too much on the map** → cues, quirks, travel, avatars can overwhelm. Strict
   icon budget per house; details on your phone when you consider a specific house.
10. **The reveal is a wall of bars** → keep it to the one question kids care about
    ("who won today, and who's ahead") with the breakdown as a secondary layer.

---

## 5. What to prototype next

1. **A visual two-screen mockup** (this turn) — a design comp of the TV board and
   the phone cockpit across a few moments (pick-a-job, the micro-game, the garage
   sale, the reveal), so we can *see* the coordinated visualization before building.
2. Then a **networked greybox**: a TV screen (a browser window) + phone controllers
   (join by room code), starting with the map + standings + the **garage sale** as
   the first shared moment. That's the real architecture, tested on the simplest
   dramatic beat.
