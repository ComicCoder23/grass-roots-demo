# Illustrative before-state faults — Grass Roots Gardening

This file documents a **fictional, deliberately dated portfolio baseline**. It is not a recovered historic website and is not evidence about a real client.

## Deliberate faults shown

| Fault | Why it weakens a small-trade site | Improvement in the live demo |
| --- | --- | --- |
| Fixed 960 px layout | Forces horizontal scrolling or unreadably small text on phones | Responsive mobile-first layout |
| No viewport meta tag | Mobile browsers render a desktop-width page | `width=device-width, initial-scale=1.0` |
| Contact details are plain text | A visitor must copy, remember, or manually type them | One-tap `tel:`, WhatsApp, and email routes |
| No prices | Visitors must enquire before knowing whether the service is in range | Clear from-prices above the fold |
| Text navigation and weak visual hierarchy | The next action is hard to spot | Clear primary contact actions and grouped content |
| Small, inconsistent interaction areas | Difficult to use on touch screens | Measured 44 px+ targets |
| No services scoped for scanning | Visitors cannot quickly decide if the business fits | Clear service cards and concise descriptions |

## Comparison rule

The live demo and its existing `MEASURED.md` remain the source of truth for after-state measurements. This illustrative baseline supports a qualitative UX comparison only; it must not be used to invent historic traffic, conversion, load-time, or client results.
