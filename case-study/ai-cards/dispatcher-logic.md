# How the dispatcher really combines late groups

Told on Oct 13, 2026, after stopping the AI card review. This is the source for the assistant's rules.

## In the dispatcher's words

> 1. Okay, so let's say we have a whole alphabet of groups. A group is at least 2 people. So groups A, B, C are riding together, but C is falling short. We have an SUV booked for a sedan job, who is only driving group D. What we can do is combine C and D together, because they're from Lumora and all of those people are colleagues. So that is the first problem.
> 2. E and F, both of them are late, so that driver is not going to be able to make his second ride. Thankfully we have a van that came back, which is doing G, H, I: 6 pax total. But a van is either for 11 pax or 14, which can easily accommodate E (2) and F. So the driver who wasn't able to make it on time, because E-F and J-K were coming at the same time, now will easily do J-K.
> 3. And that goes on and on. I had to combine...

## The rules, in plain words (draft, to confirm)

**Case 1: the late family rides with a car that has empty seats.**
A, B and C share a van, and C is late. The van leaves with A and B. C rides with D, whose car is already going and has empty seats: here, an SUV sent on a sedan job. No extra car is needed.

**Case 2: move the late families into a van with room, so their driver makes his next ride.**
E and F are late, and their driver also has J-K at the same time, so he can't do both. A van just back at the airport is taking G, H and I (6 people in an 11- or 14-seat van). E and F ride in that van. Their driver is now free and does J-K on time.

**Case 3: it chains.**
Each move frees a seat or a driver, and that opens the next fix.

## What has to be true to combine (draft)

- **Same company.** They're colleagues (Lumora), so they can share a car.
- **Same drop-off.** Everyone goes to the same hotel.
- **Ready at about the same time.** Nobody waits past the 25 min limit.
- **Enough seats.** SUV 6, van 11 or 14.
- **A car already going comes first.** Use empty seats before adding a car. Then an extra in-house car, then an affiliate, then Uber Black.

## Answers (Oct 13)

1. **Sharing is only for colleagues (Lumora).** Everybody else rides separately, unless the company that booked says it's OK, for example a travel company that's fine with putting strangers together.
   > "We arrange private car always, it's up to the people who book."
2. **D can wait for C up to 25 min.**
   > "That is the limit, after that it's too much and frustration is going to crawl up."
3. **An affiliate's van can take them too.**
   > "Yes, of course they can."

So the sharing rule belongs to the account: Lumora says yes, and a private booking is always its own car.

## Case 3: nobody to share with, so add a ride (Oct 14)

> "Answer is simple: we will just create a new ride, because there is no one to combine with. Other people over there booked a car for themselves. We will schedule a new sedan ride for them, and we will look for our driver to make that ride."

When the late family has no colleague's car with empty seats nearby (around 3C on AS 920, everyone else booked a private car):
- give them their own ride, the smallest car that fits (a sedan for 2);
- then find an in-house driver who is free for it.

This is the last step before an affiliate or Uber Black.

## Which driver can take a ride: bigger is fine, smaller never (Oct 14)

> "For example, Tarun drives a Cadillac Escalade. Even if the ride is booked for an MKT, if that job is good and on time for Tarun, we will send it to the customers as a free upgrade, so they're getting an Escalade for the price of an MKT. The schedule is not super strict when it comes to assigning drivers. But the key part is not to send a smaller vehicle. For example, if the ride is booked for an MKT and Manveer is the one who's driving, then we cannot send him, because simply the luggage would not fit. Usually that's why people are booking bigger cars."

- The booked vehicle sets the price. The car that goes can be the same size or bigger.
- **Bigger is a free upgrade.** The customer pays the booked price.
- **Smaller is never OK,** even if the people fit. The bags won't, and that's why they booked the bigger car.
- Pick the driver whose timing works. The car type comes second, as long as it isn't smaller.

> "Whenever we're giving a free upgrade, the message is gonna be sent automatically, so people are gonna be more happy about it."

**A free upgrade always sends an automatic text to the passenger.**

**Booked vs going.** The grid shows what the passenger booked, so it matches what they say on the phone ("we booked a sedan"). Opening the reservation shows the driver and the car actually going.

**The fleet (Oct 14):**

| Driver | Car | Class |
|---|---|---|
| Mila, Manveer, Daria | Cadillac XTS | luxury sedan |
| Oleg, Jaswant, Nate | Chevy Suburban | luxury SUV |
| Tarun, Levon | Cadillac Escalade | executive SUV |
| Teo | Mercedes Sprinter | van |

- **No shared cars**, so an MKT job always goes out as a free upgrade in a Suburban or an Escalade.

**The booked class decides, not the head count (Oct 14).**

> "A sedan can be fine for 3 people if they would like to book it. We have customers who say we don't have any checked bags, three passengers, and we're booking a sedan, so one of them sits in the front, two in the back. But if a passenger booked an MKT, we cannot send a sedan; we'll have to send either an MKT or an SUV."

On the Sep 4 grid, Gregory Lamb's MKT job (3 people, 22:07) sits on Manveer's XTS. The board marks it red as a ride that can't go as assigned.
- **Affiliates** (Cedar, Alder, Madrona) follow the same rule: the booked size or bigger, never smaller. Their actual cars aren't known.

## Codes instead of names

> "Let's mark those groups with something like I just explained, so when you're looking at the grid you see a code word, or a letter, or a letter along with a number. It's gonna be easier to navigate and find it in the grid, because right now it's too many names on top of flight numbers and everything being late. It's gonna be simple: group A is late, so B and C are gonna be going, and A is gonna be combined with D. You see how simple it is compared to the names."

- **How the codes work.** Each Lumora family gets a seat-style code: the manifest group number plus a letter, so Group 3 is 3A, 3B, 3C. Bookings made on their own continue after 24.
- **The code stays with the family.** A combined car reads "13A 10D 10E".
- **Colors.** Red is the family that breaks its van. Amber is a late flight in a car with mixed flights. Three or more families in a row read as a range, like 7A–F.
- **How a move reads:** "10D rides with 13A". The names go on the line under it.

## The two cases on the Sep 4 board (prototype, by-hand mode)

- **Case 1.** DL 889 took off 40 min late, so 10B would wait 40 min for 10D + 10E. 13A is a sedan job in Oleg's SUV, ready 14:06. Fix: 10D + 10E ride with 13A, 6 of 6 seats, and Group 10's van leaves at 13:35.
- **Case 2.** UA 2089 is also 40 min late, so 8A + 8B are both late and Teo would be 35 min late for 27A at 14:21. 9A is a party of 6 in Alder's Sprinter. Fix: 8A + 8B ride with 9A, 10 of 14 seats, and Teo makes 27A on time.
- **Still open:** 3C breaks Group 3 (AS 920, real delay), and Tarun is about 16 min late for 11A after Marisol Vega's ride (amber, inside the limit).

## Evidence from the real day

The Sep 4 manifest has notes beside the groups that look like the moves made that day. For example:
- A family from Group 10's late DL 889 is written next to Group 15, a sedan job that ended the day as an SUV for 4 (case 1).
- Group 17's two DL 877 families are written next to Group 18's van (6 people) (case 2).
