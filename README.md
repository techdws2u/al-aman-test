# Al-Aman Website

Static landing page for Al-Aman (Wasiat & Hibah). Single-file HTML with two logo assets.

## Files

- `index.html` — the entire site (Home, About, Products & Services, Education, Contact)
- `logo-dark.png` — Al-Aman logo for light backgrounds (header, light sections)
- `logo-light.png` — Al-Aman logo for dark backgrounds (hero card, footer)

## Deploy on GitHub Pages (test)

1. Create a new GitHub repository (e.g. `al-aman-test`).
2. Upload all three files to the repo root.
3. Go to **Settings → Pages**.
4. Under **Source**, select **Deploy from a branch**, branch `main` / folder `/ (root)`. Save.
5. Wait ~1 minute. Your site will be live at `https://<your-username>.github.io/al-aman-test/`.

## Deploy to a subdomain (e.g. al-aman.dws2u.com)

When you're ready to go live, just upload these same three files to the web root of the subdomain on your hosting provider. No build step needed.

## Compatibility

- Responsive: works on desktop, tablet, and mobile (down to 360px width).
- Tested layouts at: 1440px (desktop), 768px (tablet), 414px / 375px (mobile).
- Modern browsers: Chrome, Safari, Edge, Firefox (current versions).

## Notes

- The EN / BM language toggle in the header is a visual placeholder — wire it up when the Bahasa Malaysia translation is finalised.
- The Login (`#login`) and Get Started (`#start`) buttons currently point to anchors. Replace these with the real platform URLs before publishing.
- The contact form shows a success message client-side — connect it to your email service (Formspree, EmailJS, or a backend) before publishing.
- Verify the Quranic verse and hadith wording with your Shariah advisory team before going live.
