# Qilbo — the brain behind your store

Qilbo reads an independent store's daily sales reports and distributor invoices every night, finds the money slipping through the cracks (prices under cost, missed deals, cost increases, stock running out), and sends the owner a short list to approve in the morning.

Built inside a working liquor store. Made for liquor stores, convenience stores, and smoke and vape shops across the USA.

**Qilbo is read-only.** It never changes the register, never places orders, and never moves money. It suggests; the owner decides.

---

## What's in this repo

| Path | What it is |
|---|---|
| `index.html` | The marketing website (single page, no build step) |
| `privacy.html` | Privacy Policy |
| `terms.html` | Terms of Service |

The website is plain HTML, CSS and JavaScript. Animations use GSAP + ScrollTrigger from cdnjs; fonts are Gabarito, Inter and JetBrains Mono from Google Fonts. Images and logos are embedded in the page, so there is nothing to build.

### Page sections

1. **Hero** — "The brain behind your store", with a phone showing the morning brief
2. **Real catches strip** — mistakes found in the pilot store
3. **See it** — a real alert (Crown Royal rang up at $0.00) walked through 6 steps: Found → Checked → Suggested → You approve → Done → Verified, with optional voice narration
4. **What it catches** — 8 checks (price mistakes, invoice check, missed deals, reorder, break-pack, customer requests, UPCs and barcodes, morning brief)
5. **How it works** — connect, nightly check, morning approval
6. **Built for** — Liquor / Convenience / Smoke & vape tabs
7. **Founder story**
8. **Connections and security** — Gmail, photo/PDF, CSV/Excel in; Telegram, WhatsApp (soon), Google Drive out; 6 security promises
9. **Margin calculator**, **Pricing** (60-day free pilot, then $99 per store per month), **FAQ**, **Join the pilot** form

---

## Run it locally

No install needed. Open `index.html` in a browser, or serve the folder:

```bash
npx serve .
# or
python3 -m http.server 8080
```

## Deploy (Cloudflare Pages)

The site is hosted on Cloudflare Pages, connected to this repo. Every push to `main` deploys automatically.

One-time setup in the Cloudflare dashboard:

1. **Workers & Pages → Create → Pages → Connect to Git**, pick `QilboGloabl`
2. Production branch: `main`
3. Framework preset: **None**. Build command: *(leave empty)*. Build output directory: `/`
4. Save and deploy. The site goes live at `https://<project>.pages.dev`
5. Later: **Custom domains → add `qilbo.com`** once the domain is bought

---

## Still to do

- [ ] Buy `qilbo.com` and connect it in Cloudflare Pages
- [ ] Make the Join form send requests (Pages Function → Telegram alert + saved in D1)
- [ ] Set up `hello@qilbo.com` (Cloudflare Email Routing → Gmail)
- [ ] Add phone / WhatsApp number
- [ ] Add founder photo and the 3 store videos (liquor, convenience, smoke & vape)
- [ ] Optional: recorded voice clips for the 6-step walkthrough
- [ ] Have a lawyer review `privacy.html` and `terms.html`
- [ ] Next: the multi-store Qilbo product (per-store IDs, nightly checks, morning brief)

---

© 2026 Qilbo
