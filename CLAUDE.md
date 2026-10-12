# Basecamp at Allenberry — landing page

Single-page marketing site for **Basecamp at Allenberry**, a resort community on the grounds of Allenberry Resort & Spa in Boiling Springs, PA. Static HTML, no build step. Deployed on Netlify (see `netlify.toml`).

Positioning: a historic resort that keeps growing and evolving, now adding a resort community where wellness, nature and community meet. "Basecamp" = your home base — the safe place you set out from and come back to, before and after the hard stretches of life.

## Files

```
index.html                 the whole site (inline styles + one small <script> for the waitlist)
assets/
  logo-white.webp          Allenberry logo, white (240px — replace with full-res, see TODO)
  favicon.png, apple-touch-icon.png
  hero-allenberry-sunrise.jpg   hero background
  ref-home-base-dusk.webp       "Your home base" photo — DESIGN REFERENCE (Basecamp Bend, OR)
  amenity-*.jpg                 six Allenberry amenity photos (Playhouse, fly fishing, fitness, spa, dining, creekside)
  ref-residences-1/2.webp, ref-interior.webp   Plans gallery — DESIGN REFERENCE (Basecamp Bend, OR)
  siteplan-aerial.jpg           aerial base for the site plan; parcel, lane and residences are an inline SVG overlay
docs/preview-desktop.jpg, docs/preview-mobile.jpg   screenshots of the approved design
```

## Page structure (top to bottom)

1. Header — logo | "Basecamp", nav (Why Basecamp, Care, Living Here, Plans), "Join the waitlist" pill
2. Hero `#top` — eyebrow "Where wellness, nature and community meet", H1 "The place you love, *now a place to live.*"
3. Allenberry, reimagined — "Everything you come here for is *already here.*"
4. Why Basecamp `#why` — "Your home base, *for every climb.*", home-base photo, "Less upkeep. More life.", "Is it for you?" list (ordered by life stage)
5. Care `#care` (navy) — "Support for *every season of life.*"; cards: Daily Health Shield, Care on campus (aging in place), Recovery suites (rented, not sold)
6. Living Here `#amenities` — "Not an amenities package. *Your home.*"; 3×2 photo grid alternating indoor/outdoor: Playhouse, Fly fishing, Fitness & classes / Spa, Dining, Creekside gathering
7. Plans `#plans` (navy) — $700s, coming 2027, reference gallery, site plan, two floor-plan cards
8. Waitlist `#waitlist` — copy, "Try it first" midweek-stay block, form (first, last, email)
9. Footer

## Brand (matches allenberry.com)

| Token | Value | Use |
|---|---|---|
| Navy (ink / dark sections) | `#1A2530` | text, header, Care + Plans sections |
| Navy card | `#24323F` | cards on navy |
| River blue (accent) | `#365D78` | buttons, italic accents on light |
| Light blue | `#A9C9DD` | italic accents + eyebrows on navy |
| Paper | `#F4F1EA` / `#FBF8F2` | page / raised surfaces |
| Cream | `#E8E2D2` | Why Basecamp section |
| Ink soft | `#32414E` | body copy |
| Muted label | `#5A6572` | small labels on light |
| Rule | `#D2D4CF` | dividers |

Type: **Fraunces** (display, 400; italic `<em>` for the accent phrase in each heading), **Inter** (body), **JetBrains Mono** (uppercase eyebrows, 0.22em tracking), **Poppins 500** (uppercase pill buttons, 13px, 1.8px tracking, `border-radius: 9999px`). All from Google Fonts.

## Copy rules from the client

- Don't say "the table" for dining. The restaurants are the Barn (signature restaurant), Breeches Café, the Terrace.
- No partner names on the page (no PAM Health, no York College). Don't say health-care students live on site.
- The Playhouse is a "historic theater," not a "working theater."
- Aging-in-place language belongs only on the "Care on campus" card; the rest of Care is for all life stages.
- Keep amenity descriptions roughly equal length.
- Keep indoor/outdoor amenity photos from clustering.
- "Living Here" is the nav label for the amenities section.

## TODO before launch

- [ ] **Klaviyo**: set `KLAVIYO_PUBLIC_KEY` and `KLAVIYO_LIST_ID` in the `<script>` at the bottom of `index.html`; confirm the API `revision` date. Until then the form shows the success state without sending.
- [ ] **Logo**: replace `assets/logo-white.webp` with the full-resolution file (allenberry.com uses `/assets/logo-white.png`).
- [ ] **Reference imagery**: `ref-*` images are from Basecamp Tetherow (Bend, OR) and are labeled "Design reference imagery". Swap for Allenberry renderings, then remove the captions.
- [ ] **Floor plans**: two placeholder cards ("The Cottage", "The Residence + Suite") with `[BEDS]`, `[BATHS]`, `[SQ FT]`, `[PRICE]` and `[FLOOR PLAN]` boxes.
- [ ] **Site plan**: parcel outline and residence footprints are approximations traced from a Keynote concept. Replace with the architect's plan when available.
- [ ] **Trial stay link**: "Plan a trial stay" points to `https://allenberry.com/stay`; swap for a dedicated midweek-stay booking link if one exists.
- [ ] **Mobile nav**: links wrap to two lines under ~420px. Consider a compact menu.

## Working on this file

- Styles are inline (the design was built in a visual editor). If you refactor to classes, keep the tokens above and check desktop (1440) and phone (390) widths against `docs/`.
- Grids use `repeat(auto-fit, minmax(min(Npx, 100%), 1fr))` so they collapse to one column on phones. Keep that pattern.
- Section anchors (`#why`, `#care`, `#amenities`, `#plans`, `#waitlist`) are used by the nav and buttons.
