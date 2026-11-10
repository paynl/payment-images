# in-form

Self-hosted image set used by **PayParts** in its **credit-card** checkout form.

These images are **not** published on `static.pay.nl`, so PayParts ships them itself. They are
the card-payment-brand assets used inside the credit-card form (Apple Pay, Google Wallet,
Click to Pay) plus the card-network brand icons (Visa, Mastercard, Amex, etc.).

The folder mirrors the `static.pay.nl` path layout so a relative path maps 1:1 to a URL.

## Layout

| Path | What it is | Brand / notes |
| ---- | ---------- | ------------- |
| `checkout/applepay.brand.svg` | Apple Pay brand mark | Apple Pay |
| `checkout/googlewallet.brand.svg` | Google Wallet brand mark | Google Pay / Wallet |
| `checkout/click-to-pay.svg` | Click to Pay logo | Click to Pay |
| `checkout/creditcard.c2p.svg` | Credit-card "Click to Pay" mark | Click to Pay |
| `payment_profiles/100x100/{id}.png` | Card-network brand icons | Visa (`3141`), Mastercard (`3138`), Amex (`1705`), Maestro (`712`/`715`), Bancontact (`436`), PostePay (`707`/`708`), Carte Bancaire (`2268`), Carte Bleue (`710`/`711`), Dankort (`1939`), Nexi (`1945`), Visa/Mastercard combined (`706`/`709`) |

## Notes

- Only **credit-card** images are kept here. Other method/professional images (method logos,
  general payment profiles, issuers, country flags) continue to be served from `static.pay.nl`.
- Card-network icons are stored in `payment_profiles/100x100/` (the path PayParts uses as its
  card-brand fallback). Some brands also have an SVG variant (`3141.svg`, `1945.svg`).
- The `ids in the payment_methods folder are brand ids` note in the repo applies to the
  broader `payment_methods/` category; card-network icons for in-form live under `payment_profiles/100x100/`.
