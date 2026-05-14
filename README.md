# NorCal Holistics — Daily Push Sponsorship LP

Single-file HTML landing page. Brands book a daily push notification slot ($99 flat, 1 brand per day) to NorCal Holistics' 6,000+ Sacramento cannabis app subscribers.

## Stack
- Single `index.html` (no build, no framework)
- FormSubmit.co for booking form (no backend)
- Stripe Payment Link for $99 checkout
- Vercel for hosting

## Configuration (edit in `index.html` `<script>` block at bottom)

| Constant | Purpose |
|----------|---------|
| `BOOKED_DATES` | Set of `'YYYY-MM-DD'` strings — add after each confirmed sale |
| `STRIPE_PAYMENT_LINK` | $99 Stripe Payment Link URL — replace placeholder before launch |
| `FORM_EMAIL_PRIMARY` | `seth@norcalholistics.org` (form recipient) |
| `FORM_EMAIL_CC` | `jobany@norcalholistics.org` (cc) |
| `MIN_LEAD_DAYS` | Default `2` — minimum days out a brand can book |
| `MONTHS_TO_SHOW` | Default `3` — calendar lookahead |

## Pre-launch checklist
1. Create Stripe Payment Link → paste into `STRIPE_PAYMENT_LINK`
2. First form submission triggers FormSubmit activation email to `seth@norcalholistics.org` — click the link once to activate
3. Test booking flow end-to-end on staging URL
4. Point domain (if applicable) — `pushsponsor.norcalholistics.org` or similar

## Manage bookings
After each paid sale, add the booked date to `BOOKED_DATES` and redeploy (git push triggers Vercel auto-deploy).
