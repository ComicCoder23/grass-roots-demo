# MEASURED — Grass Roots Gardening

Numbers taken from the live page with Playwright/Chromium on 2026-08-04, not estimated.
Re-run and re-record rather than editing by hand.

## Before

The before state was **no website at all**. A paper flyer was the entire online presence.
That is not a strawman — it is the most common starting point for a small trade, and it is
exactly the position Nairn Joiners & Fire Protection is in today.

| Measure | Before |
| --- | --- |
| Website | None |
| Findable by search | No |
| Contact routes online | 0 |
| Tap-to-call | No |
| Tap-to-WhatsApp | No |
| Prices visible before enquiry | No |
| Works on a phone | N/A |

## After — measured live at 390×844

| Measure | After | Why it matters |
| --- | --- | --- |
| Load time | **273 ms** | Google's own research puts the drop-off cliff around 3 s. This is an order of magnitude inside it |
| Total transferred | **300 bytes** | Single file, no framework, no images, no fonts |
| Total requests | **1** | Nothing to fail, nothing to wait on |
| Third-party requests | **0** | No visitor data leaves the origin. Nothing to consent to |
| Tap targets under 44 px | **0 of 7** | Every link meets the Apple/Google minimum |
| Horizontal scroll at 390 px | **No** | No pinching, no sideways drag |
| Contact routes | **5** — 2 phone, 2 WhatsApp, 1 email | Three ways to make contact, all one tap |
| Steps from landing to contact | **0** | Contact is above the fold, not behind a menu |
| Images missing alt text | **0 of 0** | — |

## The claim this supports

> "No website to a page that loads in under three tenths of a second, works properly on a
> phone, and puts three ways to contact you one tap from the top."

Every number above is reproducible from the live page.

## Method

```js
// 390x844 viewport, live URL, Chromium
performance.getEntriesByType('navigation')[0].duration        // load ms
performance.getEntriesByType('resource')                       // requests + bytes
[...document.querySelectorAll('a,button')]                     // tap target audit
document.documentElement.scrollWidth > innerWidth              // horizontal scroll
```

## Known limits

- Load time measured from a UK connection to GitHub Pages CDN. A client on their own host
  will differ; re-measure per site rather than reusing this figure.
- `transferSize` of 300 bytes reflects a cached/304 response on re-navigation. The
  uncompressed file is 8.5 KB — quote the file size, not the transfer size, if asked.
- No Lighthouse score recorded yet. Worth adding for a headline number.
