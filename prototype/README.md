# Overboard — Greybox v0.1

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
- **The elastic market** — every sale pushes that price *down* a visible ladder;
  dump your whole hold and you watch it crash. Ice a couple for a better market.
- **The investment loop** *(v0.3)* — earnings buy gear that compounds (Sonar,
  Cold Hold, Bigger Boat), so money is *for* something and a well-timed haul lets
  you out-build rivals. Scored as net worth (cash + boat) at season's end.
- **A next-day forecast** *(v0.3)* — read tomorrow's demand and ice fish to sell
  into the spike; holding is now an informed bet, not arithmetic.
- **The commons** — grounds you strip below survival die; hammer the sea and it
  collapses, halving everyone's net worth. (Verified: reachable via greedy play,
  avoidable with care.)
- **AI chaos** — Reef Hog (greedy, hoards & dumps), Old Salt (cautious), Barnacle
  (chaos) move the market around you.

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
