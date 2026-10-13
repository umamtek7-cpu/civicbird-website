# CivicBird website (GitHub Pages frontend)

A mobile-responsive static website prototype for CivicBird, initially serving Bhagalpur, Bihar.

## Pages
- `index.html` — homepage
- `services.html` — service categories
- `pricing.html` — ₹300 + 18% GST = ₹354 standard service fee
- `how-it-works.html`
- `about.html`
- `safety.html`
- `support.html`
- `booking.html` — frontend booking request draft
- `join.html` — frontend Bird application draft
- `privacy.html` — prototype privacy notice
- `css/style.css`
- `js/script.js`

## Important limitations
This is a static frontend. Forms do not send or store data, no admin dashboard exists, and online payments are not connected. The booking form can create a request draft and copy it. WhatsApp only works after the official number is configured in `js/script.js`. Do not collect sensitive documents through this static site. Connect a secure backend, access controls, proper privacy policy, and a payment gateway before accepting live bookings/payments.

## Configure official WhatsApp number later
Open `js/script.js` and set:
```js
whatsappNumber: "91XXXXXXXXXX"
```
Use the official business number in international digits-only format. Do not put API keys, payment secrets, passwords, or private credentials in frontend JavaScript.

## Publish on GitHub Pages
1. Create a GitHub repository, e.g. `civicbird-website`.
2. Upload all files and folders from this package to the repository root (ensure `index.html` is at the root).
3. Open repository **Settings → Pages**.
4. Under **Build and deployment**, choose **Deploy from a branch**, select `main` and `/(root)`, then Save.
5. Wait for the published URL, usually `https://YOUR-USERNAME.github.io/civicbird-website/`.
6. Test the homepage, navigation, language toggle, booking draft and mobile layout.

## Connect civicbird.com later
1. First add/verify the custom domain in GitHub Pages settings.
2. In your domain registrar's DNS, configure GitHub Pages records as documented by GitHub. For apex domain `@`, GitHub currently documents A records `185.199.108.153`, `185.199.109.153`, `185.199.110.153`, `185.199.111.153`; configure `www` as a CNAME to `YOUR-USERNAME.github.io`.
3. Follow the current GitHub documentation and your registrar's interface; DNS changes may take up to 24 hours.
4. Enable **Enforce HTTPS** when available.

Official documentation:
- https://docs.github.com/en/pages/getting-started-with-github-pages
- https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site/managing-a-custom-domain-for-your-github-pages-site
- https://docs.github.com/en/pages/getting-started-with-github-pages/securing-your-github-pages-site-with-https

## Before public launch
- Confirm business contact details and support/grievance contact.
- Verify GST applicability, GSTIN, invoicing and pricing with a tax professional.
- Confirm which tasks each office allows an authorised representative to perform.
- Add a secure backend and admin workflow for real bookings.
- Integrate a payment provider using server-side verification; never expose secret keys in browser code.
- Replace the prototype privacy notice with a reviewed, accurate policy.
