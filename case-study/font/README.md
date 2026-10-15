# Why the board uses Barlow

**Decision (Oct 12, 2026):** keep Barlow. Barlow Semi Condensed is used for words and Barlow Condensed for times, flight numbers and places.

## What we tried

SF Pro, the macOS and iPhone font, was the obvious alternative: it's calm, familiar and well made. We tried it on the real board next to its closest relatives, using the Font Lab (`font-lab.html`). The Font Lab switches the prototype's two font settings live.

| Font | Words vs Barlow | Numbers vs Barlow | Shows on |
|---|---|---|---|
| **Barlow** | — | — | every computer |
| SF Pro | +23% wider | +35% wider | Apple devices only |
| SF Pro + SF Pro Condensed for numbers | +23% | +15% | Apple devices only |
| Inter | +25% | +37% | every computer |
| Geist | +21% | +34% | every computer |

All fonts were measured at the same size in Chrome on macOS. "Words" is one sentence from an assistant card at 14px. "Numbers" is a line of pickup times and flight numbers at 16px semibold.

## Why Barlow won

1. **The grid is the job.** A dispatcher scans 60+ rides a day in one table. With every SF-style font, names and addresses started getting cut off at the same size. In SF Pro, "Lakeside Clinic Bellevue" lost its town ("Bellev…"), Inter cut the driver name "Manveer", and the long home address lost more text. See `shots/compare-barlow-vs-sf-pro.png`.
2. **It fits the theme.** The board borrows from airport departure boards: a split-flap clock, landing-time chips and flight numbers. Barlow's narrow, DIN-like shapes belong to that world. SF Pro is a general-purpose system font, so it doesn't carry that feel.
3. **One family, two widths.** Semi Condensed for reading and Condensed for numbers. It reads as one voice, the way SF Pro and SF Pro Condensed would.
4. **It looks the same everywhere.** Barlow is a free Google Font and built into Figma. Apple's license doesn't allow putting SF Pro on a website, so a browser only borrows it from an Apple device. Windows PCs, which many dispatch desks run, would see Segoe UI instead.

The closest call was SF Pro with SF Pro Condensed for the numbers. It kept the times and flight numbers almost as compact as Barlow. But the words were still 23% wider, and it only works on Apple devices.

## Files

- `font-lab.html`: the lab. Press 1–5 to switch the font on the real board. The side-by-side close-ups are further down the page.
- `shots/compare-barlow-vs-sf-pro.png`: the morning grid in Barlow and SF Pro, labeled. Ready for the case study.
- `shots/grid-*.png`: the same grid close-up in all five fonts.
- `shots/board-*.png`: the whole board in all five fonts, at 1600 × 1000 and 2× resolution.

The shots were retaken on Oct 15, after every name and number on the board was swapped for made-up ones.

To open the lab with the live board, serve the project folder, then go to http://127.0.0.1:8767/case-study/font/font-lab.html. The "project-root" entry in `.claude/launch.json` does this. Opened as a plain file, only the close-ups work.
