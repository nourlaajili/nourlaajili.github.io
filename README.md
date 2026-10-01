# Portfolio — Nour el Houda Laajili

Single-file static site. No build step, no dependencies.

```
index.html   the whole site (HTML + CSS + a little JS)
assets/      Nour_el_houda_LAAJILI_Resume.pdf (EN) and Nour_el_houda_LAAJILI_CV.pdf (FR)
```

The site is bilingual (EN/FR toggle, top right) and has a light/dark toggle
next to it. Both preferences are remembered per visitor via `localStorage`.

## Preview locally

Open `index.html` in a browser. That's it.

## Deploy to GitHub Pages

Run once, from this folder:

```bash
git init
git add .
git commit -m "Portfolio site"
git branch -M main
git remote add origin https://github.com/<your-username>/<your-username>.github.io.git
git push -u origin main
```

Create the repo first at github.com/new, named exactly `<your-username>.github.io`
(public). GitHub Pages turns on automatically for that repo name — the site is
live at `https://<your-username>.github.io` in about a minute.

To publish a change later:

```bash
git add .
git commit -m "Update"
git push
```

## Before going live — checklist

- [x] Résumé/CV PDFs are in `assets/` and linked (English button → Resume PDF,
      French button → CV PDF)
- [x] GitHub button points at github.com/nourlaajili
- [ ] Decide whether to keep the phone number in the Contact section — it is
      public on this page, unlike on a CV you hand out
- [ ] Add repo links to the two projects once those repos are public

## Custom domain (optional)

Buy a domain, then create a file named `CNAME` in this folder containing just
the domain (e.g. `nourlaajili.com`), push it, and point these DNS records at
GitHub:

```
A     @    185.199.108.153
A     @    185.199.109.153
A     @    185.199.110.153
A     @    185.199.111.153
CNAME www  <your-username>.github.io
```

Then Settings → Pages → Custom domain → enter it → tick "Enforce HTTPS".
