# Finish Line Home Repair — Website

Static marketing site for **Finish Line Home Repair** (Lafayette, IN). Built as the
first instance of a reusable small-business website template. No build step — plain
HTML/CSS/JS, hosted free on GitHub Pages.

**Live preview:** https://dealerplateguy.github.io/finish-line-home-repair/

---

## Stack
- Plain HTML5 + CSS (one stylesheet) + a tiny vanilla JS file. Zero dependencies, zero build.
- Hosted on **GitHub Pages** (free). `.nojekyll` makes Pages serve files as-is.
- Lead forms via **Formspree** (free tier) — see setup below.
- SEO/GEO baked in: per-page titles/meta, Open Graph, JSON-LD (LocalBusiness, Service,
  FAQPage), `sitemap.xml`, `robots.txt` (AI crawlers welcomed), and `llms.txt`.

## Pages
| File | Purpose |
|------|---------|
| `index.html` | Home — hero, why-choose, services preview, realtor band, about preview, CTA |
| `services.html` | All services as individual SEO sections |
| `realtor-partnerships.html` | The differentiator — realtor value proposition |
| `about.html` | Story, experience, trust signals |
| `contact.html` | Quote form (+ inspection-report upload) and FAQ |
| `thank-you.html` | Post-submit confirmation (form redirect target) |

---

## ✅ Go-live checklist (Finish Line)
Replace the placeholders before sharing publicly:

- [ ] **Phone** — every `(765) 555-0100` and `tel:+17655550100` → the real number.
- [ ] **Email** — every `info@finishlinehomerepair.com` → the real public inbox.
- [ ] **Formspree** — create a free form, paste its endpoint into `contact.html`
      (replace `YOUR_FORM_ID`). See below.
- [ ] **Real photos** — drop the 6/13 photo-shoot images into `/assets` and reference them
      (hero background, services, gallery).
- [ ] **Transparent-PNG logo** — swap `assets/logo.jpg` for a transparent version when available.
- [ ] **Custom domain** (optional) — point `finishlinehomerepair.com` at Pages + add a `CNAME` file.

### Formspree setup (2 minutes, free)
1. Sign up at https://formspree.io and create a new form.
2. Copy the form endpoint (looks like `https://formspree.io/f/abcdwxyz`).
3. In `contact.html`, replace `https://formspree.io/f/YOUR_FORM_ID` with it.
4. Submissions now email straight to the connected inbox.
> File uploads (the inspection report) require Formspree's paid tier, or the planned
> Phase-2 Supabase uploader. Until then, the field is shown and clients can email reports.

---

## ♻️ Reuse this template for the next client
The whole design is token-driven, so a new client is mostly find-and-replace:

1. **Copy the folder** → new repo (e.g. `acme-plumbing`).
2. **Re-brand** in `css/styles.css` → edit the `:root` tokens only:
   `--navy`, `--gold` (+ variants), and the two `--font-*` values.
3. **Swap assets** → `assets/logo.jpg` and `assets/headshot.jpg`.
4. **Edit copy** → the five HTML pages. Each shares the same `<header>`/`<footer>` block;
   update nav labels only if the page set changes.
5. **Update SEO** → titles, meta descriptions, canonical URLs, `sitemap.xml`, `robots.txt`,
   `llms.txt`, and the JSON-LD blocks (name, area served, services, phone, email).
6. **Deploy** → push to a new public repo and enable Pages (Settings → Pages → Deploy from
   `main` / root).

### Where this is headed (platform)
This hand-built version proves the model with client #1. Next step is to move the
per-client content into a single data file and generate the HTML from shared components
(Astro), so onboarding becomes: **client fills an intake form → content file → site builds
itself.** That intake form is the same set of fields already collected on this site.
