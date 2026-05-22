# Leads Landing Page

Single-file static landing page to sell the South India music-industry leads database.

## Preview locally

```powershell
python -m http.server 8080 --directory landing
```
Open http://localhost:8080

## Before going live — 3 things to do

1. **Replace payment links** in `index.html`. Search for `REPLACE_WITH_RAZORPAY_LINK_` and paste your three Razorpay payment links (Starter ₹999, Growth ₹2,499, Pro ₹4,999/mo).
   - Create them at https://dashboard.razorpay.com/app/payment-links
   - Alternatively use Stripe Payment Links or Gumroad product URLs.

2. **Update the stat bar** if your `data/leads.csv` count changes. Currently shows 165+ leads, 82% with phone — re-run the count and edit the hero numbers when you grow the list.

3. **Set up delivery automation** (manual is fine to start):
   - Buyer pays → Razorpay sends you email → you reply with CSV attachment + Google Sheet share link.
   - Once you have 10+ sales, automate via Zapier (Razorpay → Gmail send with CSV).

## Deploy options (free)

- **Netlify Drop**: drag the `landing/` folder onto https://app.netlify.com/drop — live in 30 seconds with a `*.netlify.app` URL.
- **Vercel**: `vercel deploy` from this folder.
- **Cloudflare Pages**: connect this repo, set output dir to `landing`.

## First-day promotion checklist

- [ ] Post on r/IndianMusic, r/WeAreTheMusicMakers with a discount code
- [ ] DM 20 indie musicians on Instagram offering Starter pack
- [ ] Post in 5 South Indian music Facebook groups
- [ ] List on Gumroad as a second sales channel
- [ ] Add link to your roshmusik.com site footer
