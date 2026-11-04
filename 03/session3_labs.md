# Session 3 Labs: Semantic HTML
**CM-501 Frontend Web Development · EPA 2**

**Names:** Timothy Philemond Mbobbo Lule

---

## Activity · Tag that box (teams, 10 min)

Write the HTML element(s) you would use for every number. More than one element per box is allowed (e.g. `nav` + `ul`).

### The wireframe (described)

```
┌─ 1 ─────────────────────────────────────────────────────────────────┐
│  [2] ☕ UniCafé (logo)   [3] Home · Menu · Events · Contact   [4] [search…] (Go) │
└─────────────────────────────────────────────────────────────────────┘
┌─ 5 ─ Home › News › Campus life ─────────────────────────────────────┐
┌─ 6 ───────────────────────────────────────┐ ┌─ 14 ────────────────┐
│ [7] News from campus (page title)          │ │ Exam dates          │
│ ┌─ 8 ───────────────────────────────────┐ │ │ ┌─ 15 ───────────┐  │
│ │ [9] [photo] + caption                 │ │ │ │ Course   Date  │  │
│ │ [10] New study lounge opens           │ │ │ │ CM-501   3 Feb │  │
│ │ [11] 12 Oct 2026                      │ │ │ │ CM-201   5 Feb │  │
│ │ The new lounge has 80 seats, quiet…   │ │ │ │ CM-205   9 Feb │  │
│ │ [12] Read more →                      │ │ │ └────────────────┘  │
│ └───────────────────────────────────────┘ │ │ [16] Subscribe to   │
│ ┌─ 8b ─ (more teasers like 8) ──────────┐ │ │      newsletter     │
│ └───────────────────────────────────────┘ │ │                     │
│            [13] Load more news             │ │                     │
└────────────────────────────────────────────┘ └─────────────────────┘
┌─ 17 ─ UniCafé · Example Street 1 · 80000 Munich · Imprint · Privacy ┐
```

### Answers

| # | What it is | Element(s) |
|---|---|---|
| 1 | Top bar (contains 2, 3, 4) | |
| 2 | ☕ UniCafé (logo) | |
| 3 | Home · Menu · Events · Contact | |
| 4 | [search…] (Go) | |
| 5 | Home › News › Campus life | |
| 6 | Main left column (contains 7–13) | |
| 7 | News from campus (page title) | |
| 8 | One news teaser (contains 9–12) | |
| 8b | More teasers like 8 | |
| 9 | Photo + caption | |
| 10 | New study lounge opens | |
| 11 | 12 Oct 2026 | |
| 12 | Read more → | |
| 13 | Load more news | |
| 14 | Right column, "Exam dates" | |
| 15 | Course / Date grid (CM-501 3 Feb, CM-201 5 Feb, CM-205 9 Feb) | |
| 16 | Subscribe to newsletter | |
| 17 | UniCafé · Example Street 1 · 80000 Munich · Imprint · Privacy | |

---

## Lab D · Div-soup surgery (pairs, 20 min)

File: `lab-files/events-divsoup.html` (course page). One laptop per pair; switch the driver after 10 minutes.

**Your job:** make the page semantic. It should look almost the same afterwards. You may change the selectors in the `<style>` block when you change elements (e.g. `.header` → `header`).

### Checklist

- [ ] `<html lang="en">`, a meaningful `<title>` (page · site), viewport meta tag
- [ ] landmarks: `header`, `nav` (with `aria-label`), `main` (exactly one), `aside`, `footer`
- [ ] one `h1`, then `h2` (no skipped levels)
- [ ] navigation = list of real links (`<a href>`), no `onclick`
- [ ] every event is an `<article>` with a heading
- [ ] dates in `<time datetime="…">`
- [ ] "Reserve a seat": link or button? Decide and justify:
- [ ] opening hours: which element fits name–value pairs?
- [ ] address in `<address>`, phone number as a `tel:` link
- [ ] bonus: a skip link to `main`

### Check your result

1. validator.w3.org/nu → "Check by file upload": errors: _0 _ warnings: _2__
2. DevTools → Elements → Accessibility pane (Chrome: enable full-page accessibility tree). Sketch the top level of the tree:

   ```
   
   ```

3. Disable CSS (`for (const s of document.styleSheets) s.disabled = true;` in the Console). Does the page still make sense?

---

## Lab E · Before vs after, without looking (pairs, 25 min)

**Tester:** uses a screen reader (or keyboard only, if no screen reader works). Eyes closed or screen covered.
**Observer:** reads the task aloud, measures the time, writes down what happened. Swap roles after task 2.

Pages: https://rathmayers.github.io/campus-cafe-demo/before/ and …/after/

| | macOS VoiceOver | Windows NVDA | Keyboard only |
|---|---|---|---|
| on / off | Cmd + F5 | Ctrl + Alt + N / Insert + Q | – |
| next heading | rotor VO + U, choose Headings | H | – |
| next landmark | rotor → Landmarks | D | – |
| list of links | rotor → Links | Insert + F7 | – |
| next element / activate | VO + → / VO + Space | ↓ / Enter | Tab / Enter, Space |

VO = Ctrl + Option. Stop the task after 3 minutes and write "not done".

| Task | Version | Done? | Time | What got in the way? |
|---|---|---|---|---|
| 1. What is today's special and what does it cost? (start: home page) | before | | | |
| | after | | | |
| 2. Go to the menu. How much is a flat white? | before | | | |
| | after | | | |
| 3. Find the café's phone number. | before | | | |
| | after | | | |
| 4. Keyboard only: from the home page, reach the contact form and put the focus in the first field. Can you see where the focus is? | before | | | |
| | after | | | |

**Our three biggest barriers on "before" and the WCAG principle** (Perceivable, Operable, Understandable, Robust):

1. ________________________________ (P / O / U / R)
2. ________________________________ (P / O / U / R)
3. ________________________________ (P / O / U / R)

---

## Activity · Alt text or not? (teams, 10 min)

For each image: write the alt text, or `alt=""` if it is decorative, and say why in one sentence.

| | Image and context | `alt="…"` | Why? |
|---|---|---|---|
| A | "Today's special" image with text, on the menu page | | |
| B | Image with phone number and e-mail, on the contact page | | |
| C | Croissant photo next to the heading "Fresh every morning" | | |
| D | Microphone on a stage, in the teaser "Open Mic Night" | | |
| E | Big hero image behind the text "Good coffee for long study days" | | |
| F | Instagram icon, the only content of a link | | |

**Which two of these images should not be images at all? Why?**