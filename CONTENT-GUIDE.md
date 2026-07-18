# Earth Doctors — Owner's Guide

Everything you need to put your own pictures, words, and contact details on the
site. The whole website lives in **one file**: `public/index.html`.
After any change: commit and push to GitHub, and the site republishes itself
automatically within a couple of minutes.

---

## 1. Your Photos

No code needed — just drop correctly named files into folders:

- **Page banners** → put JPGs in `public/images/`
  (`hero-home.jpg`, `hero-retreats.jpg`, `hero-bookings.jpg`, … full list in
  [public/images/README.md](public/images/README.md))
- **Product photos** → put JPGs in `public/images/products/`
  (`shio-koji.jpg`, `hatcho-style-miso.jpg`, … full list in
  [public/images/products/README.md](public/images/products/README.md))

Until a photo exists, the site shows its current look (colored gradients, and a
stock forest photo on the home banner), so nothing ever looks broken.

## 2. Your Words

Open `public/index.html` in any editor and search for the text you want to
change — every headline, price, product description, retreat detail, and
journal entry is plain text in that file:

- **Products & prices**: search for `const products` (one block per product —
  name, price, description, pairing notes).
- **Retreat offerings & prices**: search for `Weekend Immersion`.
- **Courses & prices**: search for `Fermentation Foundations`.
- **Journal entries**: search for `PAGE 6: JOURNAL`.
- **Testimonial**: search for `Words from Guests`.

## 3. Correspondence (contact, bookings, newsletter)

All three forms (Contact, Bookings, Newsletter) deliver to
**Earthdoctors@protonmail.com** via [FormSubmit](https://formsubmit.co) — free,
no account needed.

**One-time activation:** the first time anyone submits a form, FormSubmit
emails Earthdoctors@protonmail.com a confirmation link. Click it once and all
future submissions arrive normally. Do this yourself right after the site goes
live: submit the contact form, then check the inbox (and spam folder).

**Recommended after activation (spam protection):** FormSubmit's activation
email includes a random-string alias for your address (it also appears in your
FormSubmit dashboard). Swap it into the three form actions in
`public/index.html` — replace `formsubmit.co/Earthdoctors@protonmail.com`
with `formsubmit.co/YOUR-ALIAS-STRING` — so spam bots can't harvest the form
endpoint. Everything else keeps working unchanged.

**To change the destination email:** in `public/index.html`, find-and-replace
every occurrence of `Earthdoctors@protonmail.com` with the new address
(9 occurrences: 3 FormSubmit form actions plus 3 mailto links where the
address appears in both the link target and the visible text), then complete
the FormSubmit activation again from the new inbox.

**Social links:** the Facebook/Instagram links in the footer are placeholders.
Search the file for `<a>Facebook</a>` and add your URLs:
`<a href="https://facebook.com/yourpage" target="_blank">Facebook</a>`.

## 4. Bookings

The **Bookings** page (in the top navigation) sends booking requests to your
email with the guest's chosen experience, preferred dates, party size, and
contact details. You reply personally to confirm — no payment is collected
through the site.

If you later want calendar-based self-scheduling (e.g. Calendly), create a free
account there and we can embed it on the Bookings page.

## 5. Domain & Hosting

The site is hosted free on **GitHub Pages** and published automatically by
`.github/workflows/deploy-pages.yml` on every push to `main`.
Domain setup instructions are in [README.md](README.md).
