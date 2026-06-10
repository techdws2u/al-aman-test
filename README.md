# Al-Aman Website

Multi-page static site for Al-Aman (Wasiat & Hibah). Each page is its own HTML file, sharing a single stylesheet.

## File structure

```
al-aman-website/
├── index.html         (Home)
├── about.html         (About Us)
├── services.html      (Products & Services)
├── education.html     (Education)
├── contact.html       (Contact)
├── styles.css         (shared across all pages)
├── logo-dark.png      (logo for light backgrounds)
├── logo-light.png     (logo for dark backgrounds)
└── README.md
```

## Why multi-file?

Each page is independent — you can edit the About page without worrying about breaking the Home page. All pages share `styles.css`, so a visual tweak (colour, font, spacing) updates the whole site from one place. Each page has its own URL (e.g. `/about.html`), so you can share direct links and Google can index each page individually.

## To update a page later

Just edit that page's HTML file. The styling lives in `styles.css` — only touch that file when you want a site-wide visual change.

## Deploy on GitHub Pages

1. Upload all files to your GitHub repo (drop them in the root, not inside a folder).
2. Settings → Pages → Source: `main` branch, `/ (root)`. Save.
3. Within 1–2 minutes your site will be live at `https://<your-username>.github.io/<repo-name>/`.

URLs will be:
- `<your-url>/` → Home
- `<your-url>/about.html`
- `<your-url>/services.html`
- `<your-url>/education.html`
- `<your-url>/contact.html`

## Deploy on a real subdomain later (e.g. al-aman.dws2u.com)

Same files, just upload to the web root of your subdomain via your hosting provider. No build step.

## Still to do before going live

- The EN / BM language toggle in the header is currently visual only. Bahasa Malaysia translation needs to be done and the toggle wired up.
- The Login (`#login`) and Get Started (`#start`) buttons point to anchors — replace with your real platform URLs.
- The contact form shows a success message client-side. Connect it to your email service (Formspree, EmailJS, or a backend).
- Have your Shariah advisory team verify the Quranic verse and hadith wording.
