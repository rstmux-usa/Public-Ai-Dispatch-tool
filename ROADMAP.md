# Roadmap: portfolio version

What's left to call the Sunset & Palms dispatch prototype done as a portfolio piece.

Status as of Oct 15, 2026: every page is built. Oct 13–15 made it deeper: the assistant was rebuilt on the dispatcher's real logic, with car, wait and lateness rules, booker search and confirmation codes. Nothing more gets built. What's left is finishing it and showing it.

## Finish line

1. [x] **Close the open decisions.** Done Oct 15: Story cards (all three styles are kept side by side in `case-study/ai-cards/shots/card-styles.png`), and the street map stays.
2. [x] **First-minute check.** Done Oct 15: the clicks worked, but a stranger had no context, so a "Start here" note now tops the assistant panel. On Oct 16 the sign-in and tour (item 5) replaced it.
3. [x] **Privacy swap.** Done Oct 15: the drivers, affiliates, client (now Lumora), client sites, record numbers and yearly figures are all made up. The public repo, `rstmux-usa/Public-Ai-Dispatch-tool`, starts from one clean commit. The private working repo keeps the real names in its history, so it never goes public.
4. [x] **Publish the prototype.** Done Oct 15: live on GitHub Pages at https://rstmux-usa.github.io/Public-Ai-Dispatch-tool/prototype/, street map included. A Claude artifact can't host the map's tile files, so Pages replaces the old artifact link.
5. [x] **Onboarding.** Done Oct 16: the link opens on the product's sign-in, filled in and read-only, over a sunset-and-palms photo. It signs in by itself, then offers a 1-minute tour or the board. The tour dims all but one part and acts it out on the real board: the situation, a row, the assistant's fix (it presses Show me, never Approve), the Map, the Inbox, then "Try it yourself". It replaces the "Start here" note. Help → Replay the tour.
6. [ ] **Write the case study.** The material is in `case-study/`:
   - The problem: one dispatcher, 64 rides, flights running late one after another (Sep 4, 2025)
   - What confused the dispatcher in the first AI cards (`ai-cards/confusion-log.md`)
   - Dispatching by hand, then turning that into rules (`ai-cards/dispatcher-logic.md`)
   - The assistant: "Show me" on the grid, approve, undo
   - Smaller decisions: Barlow (`font/`), the Golden Hour colors (`prototype/palettes.html`), confirmation codes people can say
   - What's next

After that: the resume, then job applications.

## Done

- Dispatch grid: parts of the day, statuses, quick view, right-click menu, edit reservation, grid columns
- AI assistant: decisions with suggested fixes, approve, adjust and undo
- Email intake: Gmail requests matched to rides, with drafted replies
- New reservation: one window, pickup time from the flight, paste-to-fill, payment, return trip
- Requests: web bookings (accept or decline, confirmation sent by hand) and quote requests (rate table, vehicle templates)
- Settings: 14 sections modeled on Limo Anywhere
- Driver timeline, live map, Inbox with Gmail and SMS (in the top menu)
- Office menu: close-out with account invoices, customer profiles, reports, driver app
- Dispatch by hand: the Lumora manifest as booked, family codes (3A, 3B, 3C), drag to combine
- Assistant rebuilt on the dispatcher's real moves: "Show me" on the grid, approve and undo as one group
- Car and driver rules: a bigger car is a free upgrade with a text, a smaller car never
- Wait and lateness rules: grace periods, the 15-minute on-time promise, company vs private rides
- Booker search and confirmation codes people can say (RT 33)
- Onboarding: a sign-in that fills itself in, and a 1-minute tour on the real board

## Later

- **Figma sync.** Bring the Figma board up to date with Golden Hour, the driver status chips and the Inbox. The case study uses prototype screenshots instead.

## Left out on purpose

New ideas go here instead of into the prototype, so the finish line stays put.

- Rate zones, driver payroll, the affiliate network directory, memos, the file manager and custom forms. They're a lot of work, and reviewers care much less about them than about the dispatch and AI flows.
- New pages, features or dispatch rules from Oct 15 on.
