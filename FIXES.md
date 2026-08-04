# FIXES — Grass Roots Gardening

What was delivered, mapped to the TTM ladder. This is the commercial document: every
change carries the tier or add-on it belongs to, so the demo doubles as a price list a
customer can see working.

**Job type:** B — new website (no prior site)
**Rung delivered:** Silver — £149 equivalent
**Delivered:** 2026-07-28 · **Published:** 2026-08-04

---

## What was included at Silver — £149

| Fix | What it does | Evidence |
| --- | --- | --- |
| One-page mobile-first build | Loads in 273 ms, no horizontal scroll at 390 px | `MEASURED.md` |
| Tap-to-call | Phone number is a `tel:` link, not text to copy out | Tap-tested on a real Android phone |
| WhatsApp contact route | `wa.me` deep link with a pre-filled message | Tap-tested — opened WhatsApp directly |
| Email route | `mailto:` link | Tap-tested — opened the app chooser |
| Visible pricing | Service table with honest from-prices | On page, above the fold on desktop |
| 44 px tap targets | All seven links meet the Apple/Google minimum | 0 of 7 under 44 px |
| Zero dependencies | No framework, no fonts, no external scripts | 0 third-party requests |

## What was deliberately NOT included

Named here because honest scope is part of the sale, and because each one is a separate
line on the price list rather than something quietly withheld.

| Not included | Belongs to | Price |
| --- | --- | --- |
| WhatsApp Lead Button (fixed, tracked) | Add-on | £29 |
| Google Review Booster | Add-on | £39 |
| Quote Form Upgrade | Add-on | £49 |
| Before/After Gallery Block | Add-on | £59 |
| After-Hours Auto Reply | Add-on | £79 |
| Missed Call Text Back | Add-on | £99 |
| Booking system, calendar, admin dashboard | Platinum | £749+ |

## Bugs caught before the client would have seen them

Recorded because the process finding its own faults is part of what is being sold.

1. **Email link pointed to the wrong address.** Display text said one address, the
   `mailto:` href said another. A tap would have composed to nowhere. Found by an
   automated bench, not by eye.
2. **Four contact links measured 19 px tall**, and the header call button 41 px — all
   under the 44 px minimum. Fixed to 44–54 px and re-measured.
3. **Double-encoded characters** after a PowerShell edit read UTF-8 as cp1252 — every
   "£" became "Â£". Caught on re-render, file rewritten clean.

## Verification

- Rendered at 390×844 and 1280×900
- All four contact routes tap-tested on a real phone, all four pass
- Signed off by Alan, 2026-07-28

## Status of this demo

Fictional. The business is retired. Name, phone and email are placeholders — the number
is in Ofcom's reserved drama range and can never belong to a real subscriber. A DEMO
BUILD banner sits above the fold.

**Live:** https://comiccoder23.github.io/grass-roots-demo/
