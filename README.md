# Wired Coffee Co. — wiredcoffee.org

Single-page site + Square checkout. Deploys on Netlify (same site that already serves wiredcoffee.org).

- `index.html` — the whole site (design, menu, Dial-In, builder, cart). Edit and push; Netlify redeploys.
- `img/` — site photography (compressed for web).
- `netlify/functions/process-order.js` — charges the card via Square and creates the order in the Square POS. Needs env vars on the Netlify site (already set there): `SQUARE_ACCESS_TOKEN`, `SQUARE_ENVIRONMENT=production`, `SQUARE_LOCATION_ID`.
- `netlify.toml` — build config (static publish + functions dir).

Menu prices: tax included. Menu source of truth = the printed menu boards (Aug 2026).
Member 10% and Power Hour (12-2pm, 20% select items) are applied at the counter, not by the online checkout.
