# Al-Aman — Wasiat & Hibah

Islamic legacy planning platform landing site. Shariah-compliant Wasiat and Hibah services for Muslim families in Malaysia.

**Operated by:** DWS Wealth Partners Sdn. Bhd. (Company Reg. No. 202301038491 / 1532413-X), a subsidiary of Global Asset Trustee (M) Berhad.

**Live site:** [https://techdws2u.github.io/al-aman-test/](https://techdws2u.github.io/al-aman-test/)
*(Will move to `al-aman.dws2u.com` when the site goes to production.)*

---

## Site architecture

**Bahasa Malaysia is the default language.** English lives in the `/en/` subfolder.

```
/                          ← Bahasa Malaysia (default)
├── index.html             Home
├── about.html             Tentang Kami (About Us)
├── services.html          Produk & Perkhidmatan (Products & Services)
├── how-it-works.html      Cara Ia Berfungsi (How It Works)
├── contact.html           Hubungi Kami (Contact)
├── refund.html            Dasar Bayaran Balik (Refund Policy)
├── terms.html             Terma dan Syarat (Terms and Conditions)
├── privacy.html           Dasar Privasi (Privacy Policy)
│
├── styles.css             Shared stylesheet for all 16 pages
│
├── logo-dark.png          Logo variants
├── logo-light.png
├── gat-logo.png
├── hero-family.jpg        Content images
├── about-story.jpg
├── how-it-works.jpeg
├── journey-01.jpg … journey-04.jpeg
├── sarah-ali-team.jpeg
├── sarah-ali-founder.jpeg
│
├── en/                    ← English mirrors
│   ├── index.html
│   ├── about.html
│   ├── services.html
│   ├── how-it-works.html
│   ├── contact.html
│   ├── refund.html
│   ├── terms.html
│   └── privacy.html
│
└── ms/                    Legacy redirect stubs (forward to root)
```

**16 pages in total:** 8 BM at root + 8 EN inside `/en/`.

**Legal pages note:** Each legal page (refund, terms, privacy) is a **single file containing both languages** — BM section first, divider ornament, then EN section — with a jump-to-English button in the hero. The `/en/` versions are the same file reversed (EN first, then BM) with English nav and footer.

---

## Design system

**Colour palette:**
- Emerald deep: `#0d3b2e` (primary brand)
- Gold deep: `#c9a24a` (accents, ornaments)
- Cream warm: `#faf6ee` (section backgrounds)

**Typography:**
- **Cormorant Garamond** — serif, used for headlines
- **Outfit** — sans-serif, used for body text, buttons, nav
- **Amiri** — Arabic calligraphy (Quranic verse)

**Terminology conventions:**
- "Islamic Legacy Planning" (EN) / "Perancangan Legasi Islam" (BM)
- "Shariah" (EN) / "Syariah" (BM)
- "wasiyy" spelling for Wasiat-related references
- "wasi sokongan" = backup executor
- "DWS Wealth Partners Sdn. Bhd." = formal legal entity
- "DWS2U" = consumer-facing brand name

---

## Technology

**Plain static HTML, CSS, and vanilla JavaScript.** No build step, no framework, no server-side code.

- Hosted on **GitHub Pages**
- No dependencies to install — just edit the files and push
- Fonts loaded from Google Fonts CDN

---

## How to make common edits

### Change copy on a page
Open the relevant `.html` file in any text editor, find the text, change it, commit the file. If you change BM copy, remember to change the matching EN copy in the mirror file at `/en/`.

### Change the "Last updated" date on legal pages
The three legal pages (`refund.html`, `terms.html`, `privacy.html` in both BM and EN) currently show **"Last updated: 30 September 2026"** as a placeholder. Search each file for that string and replace with the actual date. Six files to update in total.

### Add a new link to a footer
Every page has the same four-column footer. If you add a new link to one page's footer (e.g., a new legal page), you need to add it to **all 16 pages** to keep them consistent — 8 BM at root + 8 EN in `/en/`.

### Update contact details
Phone number, email, and office address live inside `contact.html` (BM) and `en/contact.html` (EN). The contact form uses `mailto:hello@al-aman.com.my` and opens the visitor's own email client with the form data pre-filled.

### Change the YouTube video on the Services page
Search `services.html` and `en/services.html` for the current video ID (`mKqgR5rnvKA`) and swap it with the new YouTube video ID.

### Update the Shariah panel or GAT partner section
These live inside `about.html` and `en/about.html`, anchored at `#shariah-panel` and `#gat` respectively.

---

## Mobile responsive notes

- **Breakpoints:** `≤980px` (tablet), `≤720px` (phone), `≤380px` (small phone)
- **Hero on mobile home page:** uses separate inline elements (`.hero-photo-mobile` and `.hero-verse-mobile`) that only show on screens ≤720px; the desktop hero visual is hidden on mobile
- **iOS phone-number auto-linking** is disabled via `<meta name="format-detection" content="telephone=no">` on every page to prevent iOS Safari from turning the registration number into a blue phone link in the footer
- **Horizontal scroll guard** — `html, body { overflow-x: hidden; max-width: 100vw }` prevents stray overflow on any page

---

## Deployment

Push changes to the GitHub repository (`techdws2u/al-aman-test`) and GitHub Pages redeploys automatically within 1–2 minutes.

**iOS Safari caches CSS aggressively.** After pushing a style change, if the site still looks old on iPhone:
1. Close Safari fully (swipe up on the app card)
2. Reopen Safari and visit the site
3. If still cached: Settings app → Safari → **Clear History and Website Data**

Testing in Chrome or another browser is a good control if you're unsure whether the fix deployed or iOS cached the old version.

---

## Known pending items

- [ ] Wire real login/signup URLs — currently `#login` and `#start` placeholders across all 16 pages
- [ ] Deploy to production subdomain `al-aman.dws2u.com`
- [ ] Replace "Last updated: 30 September 2026" placeholder on all 6 legal pages with the actual date
- [ ] Standardize contact email — Refund page uses `hello@al-aman.com.my`, Terms and Privacy use `aisyah@al-aman.com.my` (preserved from source legal docs)
- [ ] Blog / articles page (future)
- [ ] Replace temporary YouTube video (currently unlisted) when the public version is ready
- [ ] Receive final transparent logo files from designer and swap `logo-dark.png` / `logo-light.png`
- [ ] (Optional) Replace mailto contact form with a server-side form service (Formspree, Web3Forms) for better delivery reliability

---

## Contact

**Careline:** Aisyah — [+60 12-206 7931](https://wa.me/60122067931)
**General enquiries:** [hello@al-aman.com.my](mailto:hello@al-aman.com.my)
**Office:**
CT3-13, Level 13, Corporate Tower 3,
Pavilion Damansara Heights, 3, Jalan Damanlela,
Bukit Damansara, 50490 Kuala Lumpur
