# Westside Tattoo Mermaid Beach

Booking system concept for Westside Tattoo Mermaid Beach, Gold Coast.
Built by The Service Edit.

## What's here

A single-page build containing both sides of one enquiry:

- **Customer site** — homepage, the tattooists, FAQ (their own words), find us
- **Book now** — 13 steps, three ways in, image upload, review, submit
- **The Book** — what the artist sees: requests, request detail, approve, ask,
  hand over, their own calendar, offering times, payouts
- **The Counter** — studio pipeline view, assignment, waiting times

Everything is reachable by using the site. Hit Book now, send it through, then
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

## A note on the images

`index.html` is fully self-contained — the shop photo and the three stickers
are embedded in the file. Open it anywhere, on its own, with no server and no
assets folder, and it renders complete.

The same images are also kept as real files in `assets/` so they can be
swapped, re-cropped or reused. If you move to separate files later, point
`HERO_SHOT` and `STICKERS` in `index.html` at those paths instead.

## Routing

Every screen has its own URL (hash routes, so it works under `/westside-tattoo/`
on GitHub Pages and when opened from disk). Browser Back/Forward, refresh and
direct links all work:

    #/                     home            #/book/<step>       a booking step
    #/artists #/faq #/find home, section   #/book?artist=zarra booking, artist preset
    #/artist/<id>          tattooist       #/sent/<ref>        confirmation

Booking answers are kept in sessionStorage (`ws-site-v2`) so a refresh mid-form
keeps them; photos are downscaled to 1600px before storing. Nothing is sent to a
server yet — see "Status".
