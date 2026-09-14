# Westside Tattoo Mermaid Beach

Booking system concept for Westside Tattoo Mermaid Beach, Gold Coast.
Built by The Service Edit.

## What's here

A single-page build containing both sides of one enquiry:

- **Customer site** — homepage, the tattooists, FAQ (their own words), find us
- **Booking request** — 13 steps, three ways in, image upload, review, submit
- **The Book** — what the artist sees: requests, request detail, approve, ask,
  hand over, their own calendar, offering times, payouts
- **The Counter** — studio pipeline view, assignment, waiting times

Everything is reachable by using the site. Start a request, submit it, then
follow "see what lands on Bob's screen".

## Status

Concept build. Operational data is mock and marked as such.
Real content used throughout: artist bios, FAQ answers, pricing, policies and
studio details are taken from the studio's own site and the artists' own
Instagram accounts. Nothing about an artist is invented.

Outstanding, needed from the studio:

- Confirm the current roster — the shop's Instagram has highlights for
  Ben Kendall and Alexis Hepburn who are not on the website
- 6–8 pieces of work per artist
- Full day rate: the FAQ says $1000, "things to know" says $1100–1300
- A response time the studio can actually hold
- Whether the artists or the shop absorb card fees on booking fees

## Assets

- `assets/shop.jpg` — studio interior, supplied by the client
- `assets/stickers/` — flash stickers, supplied by the client

## Running it

Static. Open `index.html`, or serve the folder.

    python3 -m http.server

For GitHub Pages, serve from the repo root. `.nojekyll` is present so the
assets folder is published as-is.
