# Sunset & Palms Dispatch

It's the screen a dispatcher lives in all day, designed for the moment the schedule falls apart.

A clickable prototype of a live dispatch board for a Seattle limo and car service, with an AI assistant that suggests fixes when flights run late.

Open `prototype/index.html` in a browser. It is one self-contained file with no build step.

## What you can try

- **Schedule** in the header: pick today, tomorrow or any date, and filter by Upcoming, Done, Quotes, All, vehicle type and in-house or affiliate.
- **Grid**: rides are split into Overnight, Morning, Afternoon and Evening. Click a ride's driver status to move it along: Assigned, En route, Arrived, Picked up, Done. Green means the driver is on time, amber a little late, red late past the wait limit. Click a ride for its quick view, right-click it for actions.
- **Assistant** (left panel): approve, adjust or undo the suggested fixes for broken shared vans and late drivers. The Email tab ties incoming requests to rides and drafts the reply.
- **Timeline, Map, Inbox, Requests and Office** in the top menu: drag rides between drivers, see cars on a Seattle map, answer Gmail requests and SMS in one inbox (filtered by channel), accept web bookings and send quotes, close out rides, customers, reports and the driver app.
- **New** (or the N key): book a ride in one window.
- **Settings** (gear icon): 14 sections modeled on Limo Anywhere.

`prototype/palettes.html` is the Palette Lab used to pick the Golden Hour colors. `case-study/` collects material for the case study.

## About the data

- The scenario is a real day: Thursday, September 4, 2025 at 09:50 Seattle time, 64 trips from a Limo Anywhere grid, 31 of them for a corporate group to the Fairmont Olympic. The timing, the flights and the dispatcher's moves are from that day.
- Every name and number is made up: passengers, drivers, affiliates, the Lumora group, client sites, confirmation and record numbers, phones and the yearly figures.
- Pickup and drop-off places are real Seattle-area addresses, including SEA, BFI, Paine Field (PAE), Pier 66 and Pier 91.
