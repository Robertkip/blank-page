# Week 4 — Stack Rationale: "Empty but Live"

## The decision, in one sentence

I'm building the portfolio as **plain HTML + CSS written with AI, hosted on GitHub Pages**. It is the smallest stack that gets a real URL live today, that I can fully maintain and explain, and whose git repo doubles as proof that I can ship.

## Three options I asked AI to lay out (simplest → most powerful)

### 1. No-code (Carrd / Framer)
- **How I would build it:** Sign in, pick a template, drag a text block with my name onto the canvas, hit publish.
- **Where to host free:** Built into the platform (Carrd free tier, Framer free tier).
- **Backend needed:** No.
- **How it shows my work:** Very good for a clean one-page visual portfolio; image blocks and prototypes are first-class.
- **The real trade-off:** Fast and pretty, but the site lives inside the builder. I cannot point to a code repo as proof of shipping, and migrating off it later means rebuilding, not moving a repo. Lock-in, not ownership.

### 2. Plain code with AI (HTML + CSS on a free host) — **CHOSEN**
- **How I would build it:** I write `index.html` and a small `style.css` with AI at my side (not AI instead of me), commit to git, and push.
- **Where to host free:** GitHub Pages (free, straight from the repo). Also Netlify / Cloudflare Pages / Vercel if I outgrow it — all accept the same files.
- **Backend needed:** Not at launch. The page is static. The one future backend need (a contact form) can be handled later by a free service (Netlify Forms / Formspree) with no custom backend now.
- **How it shows my work:** Perfect for the dev track: clean, fast, readable, fully readable source. The repo *is* the portfolio piece — "code on a free host doubles as proof you can ship."
- **The real trade-off:** I own every line and can explain it, but I write and maintain that code. For a portfolio that is a feature, not a bug.

### 3. Framework (React / Vite / Next.js on a free host)
- **How I would build it:** `npm create`, component files, dev server, build step, deploy the build bundle.
- **Where to host free:** Vercel / Netlify / Cloudflare Pages (all have first-class framework support).
- **Backend needed:** No for static parts; "yes" if I need server-side logic.
- **How it shows my work:** Full interactivity when genuinely needed.
- **The real trade-off:** A real toolchain that can break: dependency installs, build errors, config drift. For a portfolio this is almost always overkill, and the complexity would eat the "finish in time and explain every part" goal.

## Why I chose option 2 and not the others

- **Cheapest path to "done":** one `index.html` file, no install step, no build step that can fail. The hardest part of any site is going from nothing to "live on a URL"; this removes every avoidable obstacle.
- **Matches the work I need to show:** my proof is code that ships and reads. A hand-written, commented `.html` is literally readable evidence of what I can do — stronger proof than a builder's template could ever be.
- **Free forever and mine:** GitHub Pages is free, and the repo stays mine and moveable. I can change hosts tomorrow and the pages move with the files.
- **Can I maintain this?** Yes. It's the smallest thing that works. I can change a color in one place and redeploy with a git push. When I outgrow it, I take the same files to Netlify or into a framework without rewriting content.

## Backend: honesty

**Not yet.** The page is static and read-only. I will add a real backend only when a case study needs a live demo or a contact form, at which point I'll re-evaluate rather than assume.

## Pressure-test of the front-runner

- *What breaks if I pick the simplest?* Nothing for launch — a single static page has nothing to break.
- *What do I maintain if I pick the most powerful?* Node modules, a build config, a framework to keep learning — maintenance debt on day one for a portfolio that has no real need for state or reactivity yet.
- *Can I finish in time?* Yes — the "empty but live" milestone is one file and a git push.
- *Does it show my work the way it needs to be shown?* Yes — readable source on the dev track is itself the evidence.
