# Product

<!-- impeccable:product-schema 1 -->

## Platform

web

## Users

- **The live dispatcher (primary).** Runs today's board, often alone, on a big
  desktop screen through a long shift, with phone calls, texts and email
  coming in at the same time. Their job is to get every passenger picked up on
  time, keep every family together, and keep the work in-house when a flight
  runs late or a car breaks down. The designer dispatches this way for a real
  Seattle company while working from Florida, so every time on the board is
  Seattle time.
- **The owner, planning.** Builds and checks tomorrow the night before, and
  looks at the schedule 20+ times a day. Their rules are the product's logic.
- **The first-day dispatcher.** The person we design for: they should be able
  to run the board almost like a veteran, because the tool carries the owner's
  logic and explains it.
- **People who evaluate it.** Hiring managers and recruiters who click through
  on their own, interview audiences the designer walks through it live, and
  possibly Limo Anywhere itself.
- **People it touches.** Drivers accept jobs and tap their status in the
  driver app. Customers book, email and text, and get confirmations and
  replies.

When a choice seems to help one audience at another's cost, the answer
(Oct 13, 2026) is everybody: if the work gets super fast and easy, that
convinces all of them.

## Product Purpose

A full dispatch system for a small premium chauffeur company, Sunset & Palms
in Seattle (most jobs are SeaTac transfers). It covers what Limo Anywhere
does, and an assistant does the legwork. It carries what one person can't
hold in their head at once across 60+ rides: flights, families, bags, drivers
and timing. When the plan breaks, it prepares the fix and the customer's
reply, and the dispatcher approves.

Every page works, so it reads as a real replacement for Limo Anywhere. The
assistant is the hero: polish and the case study center on the flow where
something breaks, the assistant prepares the fix, and the dispatcher
approves.

Success: on a day like Sep 4, 2025 (64 trips, a 31-ride corporate group,
flights running late one after another, one dispatcher), nobody waits past the
wait limit, no family is split, jobs stay in-house, and a newcomer can tell
what to do and why.

## Positioning

The incumbent grid lists trips. This board carries one owner's validated
judgment and works next to the dispatcher. It notices what broke, prepares the
move (our own drivers first, then a trusted affiliate, then asking the
customer, then Uber Black), drafts what the customer will read, and says why
in plain words. It changes nothing until the dispatcher approves. Email and
SMS requests get the same treatment: the assistant finds the ride, prepares
the change and the reply, and the dispatcher approves.

Beyond the assistant, the redesign is many basic quality-of-life improvements
over Limo Anywhere. Examples:
- one reservation window for everything
- web bookings accepted in one click
- flight status in the grid
- families sharing a van shown in one row
- Gmail and SMS in one inbox

## Operating Context

- **Incumbent:** Limo Anywhere (classic and LA Web 2.0). Its account is live
  production and is only observed, never edited. How the team really uses it:
  they always open the whole reservation and never use Detailed Edit or Edit
  Routing. They accept web bookings without its confirmation pop-up, and send
  the confirmation by hand, because web bookings usually arrive with no price.
  Quote response templates by vehicle are the designer's favorite part.
- **The scenario is a real day.** "Today" is Thursday, Sep 4, 2025, 09:50
  Seattle time. It has the 64 trips from the real Limo Anywhere grid. 31 of
  them are the Lumora group going from SEA to the Fairmont Olympic. The board
  is staged as a mess at 09:50: about 10 flights are late, one van group is
  broken, two flights are held at the gate, two rides have no driver, and one
  driver is running late. Past days open finished; future days are generated.
- **The real moves on that day:** (1) a family is late for its van, so two
  ready families share the van and an SUV is held for the late family;
  (2) two sedan jobs of 2 passengers each go out as one SUV.
- **Workflow:** ideas are tried first in the clickable prototype
  (`prototype/index.html`), then settled decisions go to Figma, which stays
  the source of truth. The prototype is shared as a claude.ai artifact so
  people can click through on their own.
- **How it will be shown:** the portfolio case study will include images
  and videos of the product, plus the live prototype for hiring managers or
  anyone else who wants to try it. All of them use the made-up names below.
- **Times:** the grid uses 24-hour time; customer emails use 12-hour time.

## Capabilities and Constraints

- **Built in the prototype:** the dispatch grid split into Overnight, Morning,
  Afternoon and Evening, with driver status, quick view, right-click actions,
  one reservation window and draggable columns. The assistant rail has
  decisions with approve, adjust and undo, plus an Email tab. Also built: the
  Schedule menu (any day, filters), New reservation (pickup time from the
  flight, fill from a pasted message, payment, return trip), Timeline (drag to
  reassign), Map, Inbox (Gmail and SMS with a channel filter), Requests (web
  bookings and quotes with vehicle templates), Office (close-out and invoices,
  customers, reports, driver app) and Settings (14 sections modeled on Limo
  Anywhere).
- **The owner's rules (hard):**
  - Never split a family.
  - Nothing is replanned until the flight takes off.
  - The customer wait limit is 25 minutes.
  - Use our own drivers first, then a trusted affiliate, then ask the
    customer, then Uber Black, and never Uber Black if it would split a
    family.
  - Pickup time is landing plus the time to reach the curb.
  - Possible double bookings are confirmed, never merged or cancelled.
  - Never auto-send a confirmation without a price.
  - Card numbers are never taken by email.
- **Approval:** nothing is sent and no ride changes without the dispatcher's
  approval. The assistant does only two things alone: labeling and filing.
- **Technical:** there are no real APIs (flights, maps, AI). Pattern matching
  stands in for a language model, and the map is drawn by hand. The prototype
  is one self-contained file with no build step, and it must run as an
  artifact.
- **Terminology:**
  - Driver status: Assigned, En route, Arrived, Picked up, Done.
  - Decisions (not "needs you").
  - PU / DO location, conf #, pax.
  - In-house / farm-out / farm-in, affiliate.
  - Wheels up, curb time, wait limit.
  - Meet & greet, shared van ("+N families").
  - Quote, web booking, close-out.
- **Open decisions:**
  - **The assistant rework is next.** The dispatcher's own walkthrough says
    the cards are too vague. They should lead with a one-line story of what
    happened and the move, and the reasons (wait limit, policy) belong in the
    detail view. See `case-study/ai-cards/confusion-log.md`.
  - Whether the rail's Email tab folds into Inbox.
  - Whether planning (the owner, the night before) becomes its own mode.
    Today, tomorrow is just another day in Schedule.
  - Approved in Phase 1 but not in the prototype yet: the double-booking
    confirm flag, the fast-mover flag and the learning loop that tightens each
    passenger's curb time.

## Brand Commitments

- **Name:** Sunset & Palms, a working name for the product and the company it
  serves. The sunset imagery comes from the designer's own photos.
- **Voice: a calm veteran colleague.** Short, plain sentences that say what to
  do and why. It is never alarmist, even when things break.
- **Customer scripts are questions** ("Would it be alright if…"). They cite
  unforeseen circumstances and never decide for the customer. They never
  mention that a job went to an affiliate.
- **Premium service is part of the product:** meet & greet, comfort-first
  vehicles, never cramped.
- **The data must feel real.** Use real Seattle-area places, real airlines and
  plausible flights. Don't bring back made-up accounts.

## Evidence on Hand

- **The real day:** the Sep 4, 2025 Limo Anywhere grid (64 trips) and the
  Lumora manifest (24 groups, 60 parties). The source files stay outside the
  repo.
- **Every name and number is made up.** Since Oct 15 the drivers,
  affiliates, the client (Lumora), the client sites, the record numbers and
  the yearly figures are made up, like the passengers. The day itself is real:
  its timing, flights, groups and the dispatcher's moves. The private working
  repo keeps the real names in its history, so it never goes public. The
  public repo starts from one clean commit of these files.
- **Owner validation:** the owner reviewed the rules and called them "the
  right way of doing things."
- **Case-study material in `case-study/`:**
  - `font/`: why the board keeps Barlow, with measurements and shots
  - `ai-cards/confusion-log.md`: the dispatcher's walkthrough of the
    assistant
- **The Palette Lab:** `prototype/palettes.html`.
- **The unmerged `phase-1-foundations` branch:** the first PRODUCT.md and
  CLAUDE.md, rules as tested TypeScript functions (`src/rules/`, 41 tests),
  `docs/rules.md`, `docs/data-model.md`, the early comps in
  `.impeccable/mocks/` and the brand photo. Ask before merging it.
- **Not on hand, so don't invent it:** usability test results, testimonials,
  or measured results of the new tool. Any "assistant saved" figure in
  Reports is staged.

## Product Principles

1. **Fast and easy for everyone.** The bar for every screen is that the
   dispatcher's work gets faster and easier. That is also what convinces a
   hiring manager or Limo Anywhere, so don't trade one audience against
   another.
2. **The move first, the why one click away.** Every assistant item opens
   with one plain sentence: what happened and what to do. The reasons, policy
   and cost of each option sit in the detail view. A suggestion with no reason
   available is still a bug.
3. **The assistant prepares, the dispatcher decides.** Nothing is sent or
   changed without approval, and every approval can be undone. Late flights
   are watched until wheels-up, and possible double bookings are confirmed,
   never fixed.
4. **Efficiency serves the experience.** Respect the wait limit, keep
   families together, choose comfort over cramming, and keep jobs in-house,
   even when the delay isn't our fault.
5. **Familiar first, minus the friction.** Experienced dispatchers recognize
   the one-row-per-trip grid and Limo Anywhere's terms on day one. Drop what
   the team already skips (Detailed Edit, Edit Routing, confirmation pop-ups),
   and use one reservation window for new rides, edits, quotes and web
   bookings.

## Accessibility & Inclusion

- Never use color alone: every status color also has an icon and words, so
  the board works for color-blind dispatchers.
- Status colors must pass WCAG AA contrast on their tinted backgrounds.
- Desktop-first. Dispatchers work on big screens through long shifts.
