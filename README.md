# The Plain Ledger — Launch Guide

This is a complete, ready-to-publish static website. No build step, no server required — it's plain HTML/CSS/JS.

## What's included

- `index.html` — homepage
- `about.html`, `contact.html`, `privacy-policy.html` — required pages for AdSense approval
- `articles/` — 3 full guides (budgeting, emergency fund, debt payoff strategy) + a listing page
- `tools/` — 2 working calculators (savings goal, debt payoff) + a listing page
- `assets/style.css`, `assets/main.js` — shared design and logic
- `robots.txt`, `sitemap.xml` — basic SEO plumbing

## Before you publish, fill in these placeholders

1. **`contact.html`** — replace `hello@REPLACE-WITH-YOUR-DOMAIN.com` with a real email address.
2. **`privacy-policy.html`** — replace `[YOUR SITE NAME]` and `[DATE YOU PUBLISH THIS SITE]`.
3. **`robots.txt`** and **`sitemap.xml`** — replace `REPLACE-WITH-YOUR-DOMAIN.com` with your actual domain once you have one.
4. Site name "The Plain Ledger" appears in the `<title>` tags and header/footer of every page — rename if you'd like something different (find-and-replace works fine).

## How to publish it (free options, no coding required)

**Option A — Cloudflare Pages (recommended, free, easy custom domain)**
1. Create a free Cloudflare account.
2. Go to Workers & Pages → Create → Pages → Upload assets.
3. Drag in this whole folder.
4. It gives you a free `*.pages.dev` URL immediately; you can attach a custom domain later under Custom Domains.

**Option B — GitHub Pages (also free)**
1. Create a free GitHub account and a new repository.
2. Upload this folder's contents to the repository.
3. In repo Settings → Pages, set the source to the main branch.
4. Your site goes live at `https://yourusername.github.io/reponame/`.

**Option C — Netlify (also free, drag-and-drop)**
1. Create a free Netlify account.
2. Go to "Add new site" → "Deploy manually" → drag this folder in.
3. Live instantly on a `*.netlify.app` URL.

A custom domain (e.g. from Namecheap or Google Domains, ~$10-15/year) makes the site look more credible and is worth buying once you're ready to apply for AdSense — but you can technically start with a free subdomain while you're still writing content.

## Before applying for AdSense

- [ ] Have at least 15-20 published pages of substantial, original content (you currently have 3 articles + 2 tools + core pages — plan to add more before applying)
- [ ] Contact page has a real, working email
- [ ] Privacy policy is filled in and accurate
- [ ] Site has been live for a few weeks with some real traffic (not required everywhere, but helps)
- [ ] No broken links, no placeholder/lorem ipsum text left anywhere
- [ ] Mobile-friendly (already handled in this build — test on your phone anyway)

## Adding AdSense once you're approved

Google will give you a snippet like this to paste into every page's `<head>`:

```html
<script async src="https://pagead2.googlesyndication.com/pagead/js/adsbygoogle.js?client=ca-pub-XXXXXXXXXXXXXXXX"
     crossorigin="anonymous"></script>
```

Then, wherever you see a `<div class="ad-slot">...</div>` placeholder in the articles or calculator pages, replace it with your actual `<ins class="adsbygoogle">` ad unit code from your AdSense dashboard.

## Adding more content later

To add a new article: copy `articles/budgeting-basics.html`, rename it, replace the title/meta description/body content, and add a link to it from `articles/index.html` and the homepage. Keep the header/nav/footer blocks identical to the other pages so the site stays consistent.
