# blank-page

> Robert Kiptoo's portfolio: *I build backends that don't break when the internet does, and I show you the tests that prove it.* Started as the Week 4 "empty but live" page; now holds the full site built from the Week 3 content map.

Plain HTML + CSS for GitHub Pages. No build step. See `rationale.md` for why.

```
index.html                       Home: claim, 3 featured cases, receipts, about teaser, CTA
work/index.html                  Work: the 3 cases, strongest first
work/lead-capture/               Case 1
work/social-media-studio/        Case 2
work/book-enrichment-api/        Case 3
about/index.html                 About
contact/index.html               Contact: the one action (Book a 20-min intro)
thank-you/index.html             After the form is sent
404.html                         Missing pages
style.css                        The identity kit as CSS variables
```

Docs: `rationale.md` (stack choice), `identity-kit.md`, `content-map.md`.

## Before going live

1. In `contact/index.html`, replace the three placeholders listed in the SETUP comment:
   - `cal.com/YOUR-HANDLE/20min` → your Cal.com booking link
   - `formspree.io/f/YOUR_FORM_ID` → your Formspree form endpoint
   - `you@example.com` → your public contact email
2. Make the case-study repos public, or their "View the repo" links 404 for visitors:
   - `Robertkip/flyrank-capstone-lead-capture` (Case 1)
   - `Robertkip/flyrank-w7-enrich` (Case 3)
   - `Robertkip/flyrank-capstone-social-studio` (Case 2) is already public.
3. When a backend-focused CV exists, uncomment the CV link in `about/index.html`.

`404.html` works on Netlify, a custom domain, or a `username.github.io/<repo>/` project site with no edits. Only a `username.github.io` root site needs its base set to `/` by hand (see the comment in the file).

## Preview locally

```bash
python3 -m http.server 8000   # then open http://localhost:8000
```

## Deploy

GitHub Pages on a free account only serves **public** repos. Make this repo public, then Settings → Pages → Deploy from branch → `main` / root. The site is at `https://robertkip.github.io/blank-page/` and redeploys on every push to `main`. `.nojekyll` tells Pages to serve the files as-is.

No-git fallback: drag this folder onto [app.netlify.com/drop](https://app.netlify.com/drop).
