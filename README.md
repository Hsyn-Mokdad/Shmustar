# Chmustar Municipality Website · موقع بلدية شمسطار

Official website of Chmustar Municipality (شمسطار), Baalbek-Hermel, Lebanon, in **English** and **Arabic**.

A static site (HTML + one CSS file, no JavaScript). It works on phones, tablets and computers.

## Structure

```
website/
├── index.html, about.html, …   English pages (12)
├── ar/                         Arabic pages (same 12 file names, right-to-left)
├── css/style.css               One stylesheet for both languages
├── images/                     Photos, logo, favicon
└── video/                      Town tour video
```

- Every page has a language button (**العربية** / **English**) that opens the same page in the other language.
- Arabic pages use `<html lang="ar" dir="rtl">`. The stylesheet uses logical CSS properties (`inline-start` / `inline-end`), so the whole layout mirrors automatically.
- When you change a page, make the same change in its twin: `website/<page>.html` ↔ `website/ar/<page>.html`.

## View locally

Open `website/index.html` in a browser.

## Publish (GitHub Pages)

The workflow in `.github/workflows/pages.yml` publishes the `website/` folder on every push to `main`.
One-time setup on GitHub: **Settings → Pages → Build and deployment → Source: GitHub Actions**.

---

Made by Hsyn Mekdad.
