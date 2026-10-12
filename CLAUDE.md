# Basecamp at Allenberry: website

A two-page marketing site for **Basecamp at Allenberry**, a multigenerational community of homes on the grounds of Allenberry Resort & Spa in Boiling Springs, PA. It's static HTML with no build step, and it deploys on Netlify (see `netlify.toml`).

**Positioning, in priority order:**

1. The homes come first. The architecture, integrated suites, elevators and flexible living arrangements are the main selling points.
2. The resort lifestyle is the setting. Everything people come to Allenberry for is already here.
3. Care is an optional benefit. It sits lower on the landing page and gets its own page.

Basecamp should read as a place people choose for how they want to live, not for how old they are.

"Basecamp" means your home base: where every adventure begins and where you always feel at home. Keep it optimistic, with no "scary" framing.

## Files

```
index.html     landing page (inline styles + Klaviyo waitlist <script> at the bottom)
care.html      Care interior page (linked from the Care band on index.html)
assets/
  basecamp-logo-white.webp       Basecamp at Allenberry logo, white, used in the header of both pages
  allenberry-logo-white.webp     Allenberry resort logo, used in the footer (240px, so replace with a full-res file)
  favicon.png, apple-touch-icon.png   leaf mark on the logo green
  hero-allenberry-sunrise.jpg    landing hero
  ref-home-base-dusk.webp        Why Basecamp photo: DESIGN REFERENCE (Basecamp Bend, OR)
  ref-townhomes-dusk.webp        Residences photo: DESIGN REFERENCE
  ref-residences-1/2.webp, ref-interior.webp   Plans gallery: DESIGN REFERENCE
  amenity-*.jpg                  six Allenberry amenity photos
  siteplan-aerial.jpg            aerial base for the site plan (inline SVG overlay)
docs/   screenshots of the approved design (desktop landing, desktop care, mobile landing)
```

## index.html: section order

1. **Header:** Basecamp logo; nav links The Homes, Why Basecamp, Living Here, Plans; "Join the waitlist" pill.
2. **Hero `#top`:**
   - Eyebrow: "Where wellness, nature and community meet"
   - H1: "The place you love, *now a place to live.*"
   - Buttons: Join the waitlist, Explore the homes.
3. **Allenberry, reimagined:** "Everything you come here for is *already here.*"
4. **Why Basecamp `#why`** (cream):
   - Heading: "Your home base, *for every adventure.*"
   - "Less upkeep. More life."
   - "Is it for you? Basecamp is for every generation…" list, in life order: young family → age in place.
5. **The residences `#residences`** (navy):
   - Heading: "A home designed to *evolve with you.*"
   - Wide photo, then six cards: Architecture, Integrated suites, Elevators, Flexible living, Ownership (primary/second home), Rental program.
6. **Living Here `#amenities`:** "Not an amenities package. *Your home.*" Six photo cards: Playhouse, Fly fishing, Fitness & classes / Spa, Dining, Creekside gathering.
7. **Care band `#care`:** a slim band, "Support for *every season of life.*", with a "Learn more about care →" link to `care.html`.
8. **Plans `#plans`** (navy): $700s, 2027, reference gallery, site plan, two floor-plan placeholder cards. **On hold until the architect delivers updated floor plans and site plan renderings.**
9. **Waitlist `#waitlist`:** copy, a "Try it first" midweek-stay block, and the form (first name, last name, email).
10. **Footer**

## care.html: section order

1. **Header:** same as index; nav links point to `index.html#…`.
2. **Hero:** "Back to Basecamp" link, "Support for *every season of life.*". `[HERO PHOTO]` placeholder.
3. **Our approach:** "Wellness first. *Support when you want it.*" Three principles: Stay well, Choose what you need, Stay close.
4. **Care options `#care-services`** (cream): three rows, each with a `[PHOTO]` placeholder.
   - Daily Health Shield: concierge functional medicine.
   - Care on campus: health-care students, à la carte, aging in place.
   - Recovery suites: rented, not sold.
5. **The acute safety net `#care-partners`:** an expedited alliance with a post-acute provider (long-term acute care and inpatient rehabilitation hospitals). Three steps: Expedited placement, Specialized care, Recovery at home.
6. **For families** (navy): "Caring for someone you love, *without carrying it alone.*" Ties to integrated suites and elevators.
7. **FAQ `#care-faq`:** `<details>` accordions.
8. **CTA band** (logo green): Join the waitlist (`index.html#waitlist`), Plan a trial stay.
9. **Footer:** "Care services are in development."

## Brand

| Token | Value | Use |
|---|---|---|
| Logo green (accent) | `#595C3B` | buttons, eyebrows and italic accents on light backgrounds, care CTA band |
| Sage | `#C5C9A4` | italic accents, eyebrows and site-plan parcel on navy |
| Navy | `#1A2530` | text, header, dark sections |
| Navy card | `#24323F` | cards on navy |
| Paper | `#F4F1EA` / `#FBF8F2` | page / raised surfaces |
| Cream | `#E8E2D2` | Why Basecamp, care options |
| Ink soft | `#32414E` | body copy |
| Muted | `#5A6572` | small labels |
| Rule | `#D2D4CF` | dividers |

**Type** (all from Google Fonts):

- **Fraunces** for display, weight 400. Every heading has one italic `<em>` accent phrase.
- **Inter** for body copy.
- **JetBrains Mono** for uppercase eyebrows, with 0.22em letter spacing.
- **Poppins 500** for uppercase pill buttons: 13px, 1.8px letter spacing, radius 9999px.

## Copy rules from the client

- **Partner names:** never name PAM Health or York College. Describe the post-acute partner generically ("a leading provider of long-term acute care and inpatient rehabilitation hospitals").
- **Health-care students:** don't say they live on site. They are "available for basic care on site."
- **Aging-in-place wording:** "grow older without growing apart" belongs on Care on campus only.
- **Dining:** don't say "the table." The restaurants are the Barn, Breeches Café and the Terrace.
- **The Playhouse:** a "historic theater," not a "working theater."
- **Amenity cards:** keep descriptions about equal in length, and don't cluster the indoor or outdoor photos together.
- **Tone:**
  - Keep healthcare low on the landing page.
  - Lead with the homes and multigenerational living.
  - No "scary" or anxiety framing.
- **Retired copy:** the "this place has so much potential" line was removed. Don't bring it back.
- **Open question:** use "nursing students" or "health-care students"? The client hasn't confirmed, and the copy currently uses both.

## TODO before launch

- [ ] **Klaviyo:** set `KLAVIYO_PUBLIC_KEY` and `KLAVIYO_LIST_ID` in the `<script>` at the bottom of `index.html`, and confirm the API `revision`. Until then, the form shows the success state but doesn't send anything.
- [ ] **Footer logo:** add a full-resolution Allenberry logo.
- [ ] **Photos:** replace the `ref-*` design reference images with Basecamp renderings, then remove the "Design reference imagery" captions.
- [ ] **Care photos:** add photos for the care.html hero and the three care options (currently dashed placeholders).
- [ ] **Floor plans:** "The Cottage" and "The Residence + Suite" have `[BEDS]`, `[BATHS]`, `[SQ FT]`, `[PRICE]` and `[FLOOR PLAN]` placeholders.
- [ ] **Site plan:** the parcel and footprints are traced approximations. Replace them with the architect's plan.
- [ ] **Verify claims:** $700s pricing, 2027 timing, exterior maintenance, amenity access, the rental program, elevators and suites per residence, and care services and partner terms.
- [ ] **Trial stay link:** currently `https://allenberry.com/stay`. Swap it for a dedicated midweek booking link if one exists.
- [ ] **Mobile nav:** the links wrap under ~420px. Consider a compact menu.

## Working notes

- Styles are inline (the pages were built in a visual editor). If you refactor to shared CSS, keep the tokens above and compare 1440px and 390px widths against `docs/`.
- Grids use `repeat(auto-fit, minmax(min(Npx, 100%), 1fr))` so they collapse to one column on phones.
- Keep the header and footer identical on both pages.
