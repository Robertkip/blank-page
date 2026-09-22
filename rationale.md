# Week 4 — Three Roads: Stack Rationale

> **In one sentence:** I'm building my portfolio in plain HTML and CSS, written with AI and hosted free on GitHub Pages, because it's the smallest stack that shows my evidence properly, I can maintain it alone, and the repo is itself proof that I ship.

---

## 1. The four constraints I gave AI

| Constraint | My answer |
|---|---|
| **Free only** | Yes. No paid plans, no custom domain for now, no trial that expires. |
| **Honest skill level** | Backend developer on the FlyRank backend track: Python, FastAPI, PostgreSQL, SQLAlchemy, Docker, pytest. I've shipped three tested backend systems. I'm not a front-end specialist or a designer. The risk for me isn't *can I build it*; it's overbuilding it. |
| **What the site needs to do** | Prove one claim: *"I build backends that don't break when the internet does, and I show you the tests that prove it."* 4 pages: Home, Work, About, Contact. Work holds exactly **3 case studies** on one shared template: Lead-Capture Platform, Social Media Studio, Book-Enrichment API. Two utility pages: `/thank-you` and `404`. No blog, no pricing, no services page. That's 9 small HTML files. *(Source: my Week 3 content map in `through-line/` + `Portfolio-Sitemap-Toolkit/sitemap.md`)* |
| **How my work must be shown** | As **evidence**, not adjectives: **real terminal output** from test runs and live probes, **a real screenshot** of the widget, and **a link to each public repo** so a reviewer can run the tests themselves. My systems are backends, so I don't need an embedded live demo. The tests *are* the demo. |
| **Anything dynamic at launch?** | **One thing: the contact form.** It posts to Formspree's free tier, so I still run no backend of my own. Booking (Cal.com) and email are plain links. |

I asked for **three options, simplest to most powerful**, and told the AI not to pick for me.

---

## 2. Three options

### Option A: No-code builder (Carrd / Framer)
- **How I'd build it:** Pick a template, drag in text and images, publish.
- **Free host:** Built in (a `carrd.co` or `framer.website` subdomain, with the builder's branding).
- **Backend?** No. Forms are a paid add-on or come through a third-party embed.
- **How it shows my work:** Poorly for my kind of proof. My terminal output would become screenshots of text, which is blurry on phones and can't be selected or searched. There's no repo behind the site.
- **Real trade-off:** Fastest to publish, but the builder owns the site. Carrd's free tier is one-page sites, and my sitemap has 4 pages plus a case-study template. Leaving later means rebuilding, not moving files. For a backend claim it's the wrong shape: the site itself would prove nothing about how I build.

### Option B: Plain HTML + CSS with AI, on a free static host ✅ *chosen*
- **How I'd build it:** 9 hand-written HTML pages in folders (`work/lead-capture/`, `about/`, `contact/`, …) and one `style.css` that carries my identity kit as CSS variables. AI writes with me, not instead of me. Deploying is `git push`.
- **Free host:** GitHub Pages. Netlify Drop is the fallback and takes the same folder, no rewrite.
- **Backend?** No. The contact form posts straight to Formspree.
- **How it shows my work:** Test output goes in as **real text** in `<pre>` blocks, so it's sharp at any size, selectable and readable by screen readers. The widget screenshot is a `<figure>` with a caption and fixed dimensions. Every case links to its repo. The site's own repo is proof too.
- **Real trade-off:** I own and can explain every line, but I also write and maintain every line. There's no templating, so the header and footer are copy-pasted across 9 files.

### Option C: Framework (Astro, static output, on Vercel / Netlify / Cloudflare Pages)
- **How I'd build it:** `npm create astro`, one shared layout component, case studies as Markdown files rendered through one template, a build step, deploy the output.
- **Free host:** Vercel, Netlify or Cloudflare Pages all build Astro for free.
- **Backend?** Not needed for static output. Serverless functions would be available if I ever wanted them.
- **How it shows my work:** Excellent. It solves my one real plain-HTML pain: the nav is written once and every case study uses one template. Code highlighting and image optimisation are built in.
- **Real trade-off:** A real toolchain: Node version, `node_modules`, a lockfile, dependency updates, framework upgrades, and a build that can fail at deploy time. It's powerful, but for 3 case studies that's upkeep no visitor will ever see.

---

## 3. Pressure-testing the front-runner (Option B)

**What breaks if I pick the simplest (A, no-code)?**
The structure and the proof both break. My sitemap is 4 pages plus a case-study template, and a free one-page builder can't hold that without hacks. My evidence (test output) turns into pictures of text, and there's no repo showing how I build.

**And where does B itself bend?** Four things, all of which I've hit:
1. **Copy-pasted nav/footer across 9 files.** A nav change means editing every page. At 9 files that's a two-minute find-and-replace, not a real problem. It *would* become one past ~6 case studies or with a blog.
2. **No forms on a static host.** Solved without a backend: the form posts to Formspree's free tier.
3. **The 404 page broke on a sub-path.** GitHub Pages serves `404.html` at *whatever* URL was missing, so its links pointed nowhere under `/blank-page/`. Fixed with a short script that points links at the site root, and tested on both a github.io sub-path and a root domain.
4. **GitHub Pages only serves public repos on the free plan.** When I checked on 2026-09-22, my Week 4 URL returned 404 because the repo is private. So are 2 of my 3 case-study repos, which means their "View the repo" links 404 for visitors. For a claim built on "run the tests yourself," that's the one failure that matters. Fix: make the repos public, then turn on Pages.

**What do I maintain if I pick the most powerful (C)?**
Node and npm versions, dependency and security updates, Astro major-version upgrades, build config, and a deploy that can go red for reasons unrelated to my content. I *can* do all that. I just don't want to spend my two weeks on it.

**Can I finish in two weeks?**
With B, yes. It's already built: all 9 pages exist with real content. What's left is three placeholders (Cal.com link, Formspree ID, public email) and making the repos public. A framework would mean rebuilding pages that already work.

**Does it show my work the way it needs to be shown?**
Yes. My proof is test output, one screenshot and public repos. Static HTML shows real terminal text better than any builder, and it needs no demo server because the tests are the demo.

---

## 4. My decision

**I chose Option B: plain HTML + CSS, written with AI, on GitHub Pages.**

I didn't choose **no-code** because my site is four pages with a case-study template, and my claim is about *how* I build. A builder would turn my test output into screenshots and hide the one thing I most want to show: real code, in a real repo, that I shipped.

I didn't choose **a framework** even though I could build it. It solves a problem I don't have yet (templating lots of pages) and hands me a toolchain to babysit from day one. For three case studies, that's a bulldozer for a flower.

**Can I maintain this?** Yes. There's no install, no build and no dependencies. A colour change is one CSS variable, and a deploy is one `git push`. If I disappear for a month, nothing will have broken when I come back.

**Does it show my work well?** Yes. Real test output, a real screenshot and public repos are exactly what plain HTML does best, and the site's own repo is part of the proof.

**What would make me switch:** more than ~6 case studies or a blog → move the same content into Astro. Needing form handling beyond Formspree's free tier → move hosting to Netlify and use Netlify Forms. Neither needs a rewrite.

---

## 5. Backend: the honest answer

**Not yet.** Nothing on the site needs a server of my own:
- **The contact form** posts straight to Formspree's free tier. If JavaScript is off, it still posts normally.
- **Booking and email** are a Cal.com link and a `mailto:` link.
- **Week 8 ("Wire One Real Thing")** is when I'll revisit. One option is pointing the form at my own Lead-Capture API, which would make the contact form a fourth piece of proof.
