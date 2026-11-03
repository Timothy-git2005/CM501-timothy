# Session 2 Labs — HTTP, your first page, Git
**CM-501 Frontend Web Development · EPA 1**

**Team / names:** Timothy Philemond Mbobbo Lule

---

## Lab A · Read real HTTP traffic

Setup: Chrome/Edge, incognito, DevTools → Network, **Disable cache** ticked.
Site: https://rathmayers.github.io/campus-cafe-demo/

### A1 · The main document (`…/after/`)

| Question | My answer |
|---|---|
| Request URL and method | https://rathmayers.github.io/campus-cafe-demo/after/ · GET |
| Status code | 200 |
| Protocol (h2? h3?) | TODO |
| Remote address (IP:port) | [2606:…]:443 |
| `content-type` of the response | text/html |
| `cache-control` of the response | max-age=600 — TODO: explain in own words |
| `etag` or `last-modified` present? | TODO: which one(s) + value |
| One request header that tells the server something about you | user-agent — TODO: what does it reveal? |

### A2 · Before vs after

| | before | after |
|---|---|---|
| Number of requests | 28 | 23 |
| Transferred (MB / kB) | 23.7 MB | 1.2 MB |
| DOMContentLoaded | 719 ms | 137 ms |
| Load | 2.71 s | 316 ms |
| Largest file (name + size) | hero.png (6958 kB) | AdobeClean-Bold.otf (254 kB) — TODO: check if it's from an extension |
| Number of different domains | 5 | 2 |
| Load with throttling Slow 4G | 2.1 min | 2.15 s |

**Which three requests on *before* would you remove first? Why?**
Pattern: *name, size, why it's a problem, what I'd do.*

1. pastry.png — size: TODO — reason: TODO
2. event.png — size: TODO — reason: TODO
3. hero.png — size: 6958 kB — reason: TODO

### A3 · Provoke status codes

| Try this | Status I see | What it means |
|---|---|---|
| `…/campus-cafe-demo/does-not-exist/` | | |
| `http://rathmayers.github.io/campus-cafe-demo/` (http) — first request | | |
| Reload `…/after/` **without** "Disable cache" | | |

### A4 · The terminal view

Command used:
```
curl -I https://rathmayers.github.io/campus-cafe-demo/after/
```

Three header lines, explained in my own words:

1. `` —
2. `` —
3. `` —

*If fast:* `curl -I http://…` → status: ____ · location: ____
Security headers, café site vs gov.uk:

---

## Lab B · My first page, by hand

**4. Why does an edit in DevTools Elements disappear on reload?**
It disappeared because the original fetched HTML contains something different, hence whenever it fetches, the changes disappear.

**5. How many requests does my page need? Why so few?**
TODO: recount in incognito (expected 1–2) — Our site does not contain any CSS or require image fetching of any sort.

**6. about.html linked to index.html and back:** ✅
Status code seen when opening `about.html` with `serve`: 301 (Moved Permanently → `/about`)

*If fast — `slow.js` without/with `defer`:*
- Without defer:
- With defer:

### My websites (for index.html)
Pattern: *what I observed + the number + why it matters to a visitor*

| Site | Love / hate | Requests | Transferred | Domains | Load (normal / Slow 4G) | Reason (my words) |
|---|---|---|---|---|---|---|
| | love | | | | | |
| | love | | | | | |
| | hate | | | | | |

---

## Lab C · Ship it to GitHub

**Config (once per computer, in WSL):**
```
git config --global user.name "…"
git config --global user.email "…"
git config --global init.defaultBranch main
```

| # | Do | Done |
|---|---|---|
| 1 | `git init` | ☐ |
| 2 | `git status` | ☐ |
| 3 | Commit 1 | ☐ |
| 4 | Commit 2 | ☐ |
| 5 | Commit 3 | ☐ |
| 6 | `git log --oneline` | ☐ |
| 7 | New repo on github.com: `cm501-timothy` (public, no README, no .gitignore) | ☐ |
| 8 | `git remote add origin …` → `git push -u origin main` | ☐ |
| 9 | 3 commits visible on GitHub? | ☐ |

Repo URL:

*If fast:* README.md + .gitignore (`.DS_Store`, `node_modules/`) committed ☐