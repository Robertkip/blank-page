# Content Map (Week 3): The Through-Line

Full version with the ten claim options and reasoning: `~/through-line/through-line.odt`.

## One-line claim
> **I build backends that don't break when the internet does, and I show you the tests that prove it.**

- **The one person:** a non-technical founder or hiring manager skimming on a phone, who needs to trust I can ship without hand-holding.
- **The one action:** Book a 20-min intro. Every page ends in it.

## Case ranking (strongest leads)
| # | Case | Why it sits here | Headline proof |
|---|------|------------------|----------------|
| 1 | Lead-Capture Platform (FlyRank backend capstone) | Proves the claim most directly: a public endpoint built to survive bad input, floods, bots and failed dependencies | 79 tests pass; 23/23 live acceptance probes pass |
| 2 | Social Media Studio (FlyRank backend capstone) | Proves reliability under crashes | Publishes exactly once across a crash and restart; 14 tests pass |
| 3 | LLM Book-Enrichment API (FlyRank W7) | Puts an unpredictable LLM behind a strict contract and reports failures honestly | 8/8 on the category eval, 7/8 cold first run reported openly |

## Page map
| Page | Sections (in order) | Call to action |
|------|---------------------|----------------|
| Home `/` | Hero (claim) → 3 featured cases → proof strip → about teaser → CTA band | Book a 20-min intro |
| Work `/work/` | Intro → case 1 → case 2 → case 3 → CTA band | Book a 20-min intro |
| Case `/work/[slug]/` | Title + result → Context → Constraint → What I did → Evidence → Outcome → Next | Book a 20-min intro + next case |
| About `/about/` | Photo + name → who I am (≤120 words) → how I work → tools → CV (secondary) | Book a 20-min intro |
| Contact `/contact/` | Heading → Cal.com booking → form → 24h reply promise → email fallback | This page *is* the action |

Utilities: `/thank-you/` (points to the Lead-Capture case) and `404` (points back to Home, Work and Contact).

## Still need to gather
- [x] Push the Lead-Capture repo *(pushed as `Robertkip/flyrank-capstone-lead-capture`)*
- [x] Make `flyrank-capstone-lead-capture` and `flyrank-w7-enrich` public
- [x] Public email on the contact page
- [ ] Cal.com booking link and Formspree form ID (placeholders in `contact/index.html`)
- [ ] Lead-Capture dashboard screenshot showing a captured, geo-enriched lead
- [ ] Social Media Studio: screenshot of a real Mastodon post, and a clip of crash → restart → published exactly once
- [ ] Book-Enrichment: eval results screenshot; fix or explain the cold-start timeout and re-run
- [ ] Capstone outcomes and one testimonial from a FlyRank mentor or reviewer
- [ ] Backend-focused CV PDF (then uncomment the link in `about/index.html`)
- [x] Replace this repo's placeholder identity kit and content map with the real ones
