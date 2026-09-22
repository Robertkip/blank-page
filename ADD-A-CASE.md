# How to add the next case

**Where it goes:** `work/<slug>/index.html` in this repo (`~/blank-page`, live at https://robertkip.github.io/blank-page/). One folder per case. The next one is `work/travel-assistant/`.

**Shape:** use the Week 2 three beats. They map onto the sections the case pages already have, so the template doesn't change:

| Beat | Page sections |
|---|---|
| Problem | h1 result line, Context, Constraint |
| What I did | What I did, Evidence (real test output or a real screenshot, never an AI stand-in) |
| What came of it | Outcome, including one honest limit |

**Steps** (about an hour, once the evidence exists):

1. Copy the last case: `cp -r work/book-enrichment-api work/<slug>`. The folder depth is the same, so every `../../` path still works.
2. In the copy, rewrite the `<title>`, the meta description, the eyebrow (`Case 4 · …`), the h1 and `case-meta` (stack · headline number · repo link). Then write the three beats. Images go in `assets/<slug>-*.png`, with real `width`/`height` and alt text.
3. Chain it: in `work/book-enrichment-api/index.html`, change the CTA link to `Next case: <name>`. On the new page, the CTA link reads `Back to case 1: Lead-Capture Platform`.
4. Add a card to `work/index.html`, and change "Three" to "Four" in its h1 and meta description. The home page keeps its three strongest cases. Swap one out only if the new case beats it.
5. Preview with `python3 -m http.server 8000` and click every link on the new page.
6. Commit, push to `main`, and check that the live URL loads (Pages redeploys on every push).
7. Tick the case off in `content-map.md`.

**Shortcut:** open the Claude Project (it holds the claim, identity kit, content map and this note). Paste in the three beats and the evidence, and ask it for `work/<slug>/index.html` following this note.
