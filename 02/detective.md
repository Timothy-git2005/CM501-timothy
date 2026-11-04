# Six Lenses — Website Review
**CM-501 · Team:** Timothy Philemond Mbobbo Lule
**Round 1:** Campus Café before / after   **Round 2:** gov.uk / ____________

Scoring: +1 visible · +2 hidden (needed a tool/test) · +1 evidence bonus. Good findings count too.
Look, don't touch: no scanners, no logins, no real data in forms.

Finding pattern: *what exactly + where + the evidence (number, header, screenshot)*

---

## Lens 5 · Performance

- [ ] Lighthouse Performance score (mobile, incognito)
- [ ] LCP (Largest Contentful Paint)
- [ ] CLS (Cumulative Layout Shift)
- [ ] TBT (Total Blocking Time)
- [ ] Page weight (transferred)
- [ ] Number of requests
- [ ] Largest single file
- [ ] Slow 4G feel
- [ ] Image formats (JPG/PNG vs WebP/AVIF)
- [ ] Content visible without JavaScript?

| Measure | Café before | Café after | gov.uk | Bahn.de |
|---|---|---|---|---|
| Lighthouse score (mobile) | | | | |
| LCP | | | | |
| CLS | | | | |
| TBT | | | | |
| Transferred | 23.7 MB | 1.2 MB | | |
| Requests | 28 | 23 | | |
| Largest file | hero.png 6958 kB | | | |
| Load on Slow 4G | 2.1 min | 2.15 s | | |
| Image formats | | | | |
| Works without JS? | | | | |

| # | Finding (be specific!) | Site | Good/Bad | Vis./Hidden | Evidence | Pts |
|---|---|---|---|---|---|---|
| 1 |Requests are blocking the intial rendering of a site hence user sees a white screen even when data is already there |bahn.de | bad  |Visual&hidden |Presence of <scripts> in the header hence blocking|4 |
| 2 |unnecessary image size causing an increased download time  |before |bad |Hidden |Lighthouse report |3 |
| 3 |few images needed to load and requires less time to load the site |after |good|visual |load time  |3 |
| 4 |uses png image formating that comes off to large for photos |before |bad |hidden |img format |3 |
| 5 | proper image formting using webp as it cuts the image size by 10x|after|good |hidden |img format |3
| 6 |content is built using html and not javascript hence does not crash when javascript is disabled |after |good |visual |site reloads without javascript enabled |3 |
| | | | | | **Total** | |

---

## Lens 6 · Security & privacy

- [ ] HTTPS + valid certificate (padlock / site info)
- [ ] `http://` redirects to HTTPS?
- [ ] Cookie banner: Reject as easy as Accept?
- [ ] Cookies set before consent? (incognito → Application → Cookies)
- [ ] Third-party domains (Network → Domain column)
- [ ] Security headers: Strict-Transport-Security, Content-Security-Policy, X-Content-Type-Options
- [ ] Mixed content / warnings (Console)
- [ ] Impressum & Datenschutzerklärung
- [ ] Forms send over HTTPS (`<form action="…">`)

| # | Finding (be specific!) | Site | Good/Bad | Vis./Hidden | Evidence | Pts |
|---|---|---|---|---|---|---|
| 1 | | | | | | |
| 2 | | | | | | |
| 3 | | | | | | |
| 4 | | | | | | |
| 5 | | | | | | |
| 6 | | | | | | |
| | | | | | **Total** | |

---

## Lens 1 · Content & UX

- [ ] 5-second test: what is it for, who is it for?
- [ ] Contact info in < 3 clicks
- [ ] Navigation clear, always know where you are (3 pages)
- [ ] Text readable: short paragraphs, clear headings, plain language
- [ ] Clear calls to action
- [ ] Meaningful `<title>` on every page
- [ ] Meta description (view-source)
- [ ] `<html lang="…">`
- [ ] Broken links / dead ends (404)
- [ ] Impressum (German sites)

| # | Finding (be specific!) | Site | Good/Bad | Vis./Hidden | Evidence | Pts |
|---|---|---|---|---|---|---|
| 1 | | | | | | |
| 2 | | | | | | |
| 3 | | | | | | |
| 4 | | | | | | |
| 5 | | | | | | |
| 6 | | | | | | |
| | | | | | **Total** | |

---

## Lens 4 · Accessibility

- [ ] Keyboard only (Tab, Shift+Tab, Enter, Space)
- [ ] Focus always visible
- [ ] "Skip to content" link (Tab once after load)
- [ ] Works at 200 % zoom
- [ ] Meaningful alt texts on images
- [ ] Logical heading structure (h1 → h2 → h3)
- [ ] Form fields have labels
- [ ] Text contrast sufficient
- [ ] Nothing moving/blinking that can't be stopped
- [ ] Page language set

| # | Finding (be specific!) | Site | Good/Bad | Vis./Hidden | Evidence | Pts |
|---|---|---|---|---|---|---|
| 1 | | | | | | |
| 2 | | | | | | |
| 3 | | | | | | |
| 4 | | | | | | |
| 5 | | | | | | |
| 6 | | | | | | |
| | | | | | **Total** | |

---

## Lens 3 · Responsiveness

- [ ] Test at 375 px / 768 px / 1440 px (device toolbar, Ctrl+Shift+M)
- [ ] Horizontal scrolling at 375 px and 320 px?
- [ ] Navigation works on phone (menu button)
- [ ] Text readable without zoom on phone
- [ ] Tap targets ≥ 44 × 44 px
- [ ] Images scale / don't overflow
- [ ] Landscape mode
- [ ] Viewport meta tag
- [ ] Media queries / Flexbox / Grid in CSS

| # | Finding (be specific!) | Site | Good/Bad | Vis./Hidden | Evidence | Pts |
|---|---|---|---|---|---|---|
| 1 | | | | | | |
| 2 | | | | | | |
| 3 | | | | | | |
| 4 | | | | | | |
| 5 | | | | | | |
| 6 | | | | | | |
| | | | | | **Total** | |

---

## Lens 2 · Visual design

- [ ] Visual hierarchy (squint test): 1st, 2nd, 3rd
- [ ] Typography: number of fonts, body size, line length (Computed)
- [ ] Colour palette consistent, contrast ratio (colour picker)
- [ ] Whitespace
- [ ] Consistency across 3 pages
- [ ] Images: sharp, relevant, text inside images?
- [ ] Obvious what's clickable
- [ ] Where fonts come from (Network → Font → Domain)
- [ ] Image file size vs displayed size

| # | Finding (be specific!) | Site | Good/Bad | Vis./Hidden | Evidence | Pts |
|---|---|---|---|---|---|---|
| 1 | | | | | | |
| 2 | | | | | | |
| 3 | | | | | | |
| 4 | | | | | | |
| 5 | | | | | | |
| 6 | | | | | | |
| | | | | | **Total** | |