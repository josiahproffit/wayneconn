# Wayne Conn Plumbing — Website

A fast, fully responsive, single-page marketing site for **Wayne Conn Plumbing**, a licensed & insured residential plumber serving Jacksonville, FL and surrounding communities.

Built as a static site — no build step, no framework, no dependencies. Just HTML + CSS (Google Fonts loaded from CDN). It works by opening `index.html` in any browser.

---

## 📁 What's in here

```
.
├── index.html        # The entire website (HTML + CSS + a little JS)
├── assets/           # Project photos used on the site
│   ├── master-bath-remodel.png
│   ├── pedestal-sink.png
│   └── toilet-install.jpg
├── robots.txt        # Tells search engines they can crawl everything
├── sitemap.xml       # Lists the pages/sections for search engines
└── README.md
```

> **Heads up:** `robots.txt` and `sitemap.xml` reference `https://www.wayneconnplumbing.com/`. Once your real domain is live, open both files and replace that URL so search engines crawl the right address. Then submit `sitemap.xml` in [Google Search Console](https://search.google.com/search-console) to get indexed faster.

Everything is self-contained. The service-area map, reviews, and contact card are all baked in — there are no API keys or backend services to configure.

---

## 🚀 Publish it (free) with GitHub Pages

1. Create a new repository on GitHub (e.g. `wayne-conn-plumbing`).
2. Upload **all the files in this folder** (keep `index.html` at the root and the `assets/` folder next to it).
   - Web: on the repo page click **Add file → Upload files**, drag everything in, and **Commit changes**.
   - Or with git:
     ```bash
     git init
     git add .
     git commit -m "Initial site"
     git branch -M main
     git remote add origin https://github.com/YOUR-USERNAME/wayne-conn-plumbing.git
     git push -u origin main
     ```
3. In the repo, go to **Settings → Pages**.
4. Under **Build and deployment → Source**, choose **Deploy from a branch**, pick **main** / **/ (root)**, and **Save**.
5. Wait ~1 minute. Your site goes live at:
   `https://YOUR-USERNAME.github.io/wayne-conn-plumbing/`

That's it — it's live.

> Prefer drag-and-drop? **Netlify** and **Vercel** also work: just drop this folder in and it deploys instantly.

---

## 🌐 Using a custom domain (e.g. wayneconnplumbing.com)

1. Buy the domain (Namecheap, GoDaddy, Google Domains, etc.).
2. In **Settings → Pages → Custom domain**, enter your domain and save (this creates a `CNAME` file).
3. At your domain registrar, point DNS at GitHub Pages:
   - Four `A` records on `@` → `185.199.108.153`, `185.199.109.153`, `185.199.110.153`, `185.199.111.153`
   - One `CNAME` record on `www` → `YOUR-USERNAME.github.io`
4. Back in **Settings → Pages**, tick **Enforce HTTPS** once it's available.

---

## ✏️ Editing common things

Open `index.html` in any text editor (VS Code is great and free).

| To change… | Find… |
|---|---|
| **Phone number** | Search for `9043533102` (the `tel:` links) and `(904) 353-3102` (the visible text). Replace every instance. |
| **Google reviews link** | Search for `Read all 47 reviews` — the surrounding `<a href="...">` holds the link. |
| **Review count / rating** | Search for `47` and `4.8` and update the numbers. |
| **Service-area cities** | Search for `area-list` (the checklist) and `map-pin` (the map pins). |
| **Business hours** | Search for `8AM` / `8:00` to find the hours (also in the SEO schema near the top). |
| **Services / copy** | Each service is an `<article class="svc-card">` block. |
| **Photos** | Drop new images into `assets/` and update the matching `<img src="assets/...">` paths. For best results use landscape JPG/PNG around 1200px wide. |

### SEO note
Near the top of `index.html` there's a `<script type="application/ld+json">` block (LocalBusiness / Plumber schema for Google) and `<meta>` tags. If you change the phone, address, hours, rating, or domain, update them there too so search engines stay in sync. Replace `https://www.wayneconnplumbing.com/` with your real domain throughout once you have it.

---

## 📬 Want a working contact form later?

The site currently drives everyone to **call** (the fastest path for plumbing). If you later want an email lead form, the easiest no-backend options are:

- **[Formspree](https://formspree.io)** — paste their endpoint into a `<form action="...">`.
- **[Netlify Forms](https://docs.netlify.com/forms/setup/)** — add `netlify` to a `<form>` tag if you host on Netlify.

---

© Wayne Conn Plumbing. Licensed & Insured · Jacksonville, FL
