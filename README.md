# Al-Aman Website

Bilingual (English + Bahasa Malaysia) multi-page static site for Al-Aman (Wasiat & Hibah).

## File structure

```
al-aman-website/
├── index.html         (Home — EN)
├── about.html         (About Us — EN)
├── services.html      (Products & Services — EN)
├── education.html     (Education — EN)
├── contact.html       (Contact — EN)
├── styles.css         (shared across all pages, both languages)
├── logo-dark.png      (logo for light backgrounds)
├── logo-light.png     (logo for dark backgrounds)
├── ms/
│   ├── index.html     (Home — BM)
│   ├── about.html     (About Us — BM)
│   ├── services.html  (Produk & Perkhidmatan — BM)
│   ├── education.html (Pendidikan — BM)
│   └── contact.html   (Hubungi Kami — BM)
└── README.md
```

## How the language toggle works

The EN/BM toggle in the header is a real link, not a JavaScript switcher. Clicking BM on the English About page takes the reader to `/ms/about.html` (the Malay About page). Clicking EN on the Malay About page takes them back to `/about.html`. This means:

- Users can bookmark either language version directly.
- Search engines properly index both language versions (via `hreflang` tags).
- No flicker, no localStorage dependency, no JS bugs.

## To update a page later

Edit the specific HTML file. When you change wording on an English page, remember to update the matching Malay page in `/ms/` too, to keep the two versions in sync.

Styling lives in `styles.css` — only touch that file when you want a site-wide visual change.

## Deploy on GitHub Pages

1. Upload the entire folder contents to your GitHub repo root (including the `ms/` subfolder).
2. Settings → Pages → Source: `main` branch, `/ (root)`. Save.
3. Within 1–2 minutes your site will be live.

URLs will be:

**English:**
- `<your-url>/` → Home
- `<your-url>/about.html`
- `<your-url>/services.html`
- `<your-url>/education.html`
- `<your-url>/contact.html`

**Malay:**
- `<your-url>/ms/` → Utama
- `<your-url>/ms/about.html`
- `<your-url>/ms/services.html`
- `<your-url>/ms/education.html`
- `<your-url>/ms/contact.html`

## Still to do before going live

- The Bahasa Malaysia translation was AI-drafted. Have someone fluent read through it for tone and cultural nuance before publishing to real users.
- The Login (`#login`) and Get Started (`#start`) buttons point to anchors — replace with your real platform URLs on both language sets.
- The contact form shows a client-side success message. Connect it to your email service (Formspree, EmailJS, or a backend).
- Have your Shariah advisory team verify the Quranic verse translations, especially the Malay rendering of Al-Baqarah 2:180.
- Article link buttons and blog cards currently don't lead anywhere. Wire them up when the individual article pages exist.
