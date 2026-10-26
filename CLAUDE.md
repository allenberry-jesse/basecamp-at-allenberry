# Basecamp at Allenberry: website

A two-page marketing site for **Basecamp at Allenberry**, a multigenerational community of homes on the grounds of the historic Allenberry Resort in Boiling Springs, PA. It is static HTML with no build step and deploys on Netlify (see `netlify.toml`).

**Positioning, in priority order:**

1. **The homes come first.** The architecture, integrated suites, elevators and flexible living arrangements are the main selling points.
2. **The resort lifestyle is the setting.** Everything people come to Allenberry for is already here.
3. **Wellness is about living well every day,** not only when you're sick. Care is an optional benefit, so it sits lower on the landing page and has its own page.

Basecamp is a place people choose for how they want to live, not for how old they are. The community is an extension of your family, and a better answer to conventional senior living.

"Basecamp" means your home base, where every adventure begins and where you always feel at home. Keep the tone optimistic and never use anxious framing like "the scary ones."

## Files

```
index.html     landing page (inline styles + Klaviyo waitlist <script> at the bottom)
care.html      Wellness & Care page (linked from the Wellness & care band on index.html)
assets/
  basecamp-logo-white.webp     Basecamp at Allenberry logo, header of both pages
  allenberry-logo-white.webp   Allenberry resort logo, footer (240px; replace with full-res)
  orvis-endorsed.webp          Orvis Endorsed Fly-Fishing Lodge badge, under the "already here" heading
  favicon.png, apple-touch-icon.png
  render-aerial.jpg            landing hero: CONCEPTUAL RENDERING
  render-street.jpg            Why Basecamp image: CONCEPTUAL RENDERING
  render-residence.jpg         Residences image: CONCEPTUAL RENDERING
  render-lane.jpg, render-cottage.jpg   Plans section: CONCEPTUAL RENDERINGS
  amenity-*.jpg                six Allenberry amenity photos
  care-hero-walk.jpg           Care page hero
  creek-golden-hour.jpg        Care page, acute safety net section
docs/   screenshots of the approved design (landing + care, desktop + mobile)
```

## index.html: section order

1. **Header:** Basecamp logo. Nav: The Homes, Why Basecamp, Living Here, Plans. "Join the waitlist" pill.
2. **Hero `#top`:** aerial rendering with a bottom-up gradient.
   - Eyebrow: "Where wellness, nature and community meet"
   - H1: "The place you love, *now a place to live.*"
   - Buttons: Join the waitlist, Explore the homes
   - Keep only the headline and CTAs on the image; longer copy goes in the intro.
3. **Allenberry, reimagined:** "Everything you come here for is *already here.*" Four paragraphs:
   - the resort's history and Basecamp as its next chapter
   - see the place differently (trail, Playhouse, Barn)
   - neighbors as an extension of your family
   - a better answer to senior living, built around living well
4. **Why Basecamp `#why`** (cream):
   - "Your home base, *for every adventure.*" with a street rendering
   - "Less upkeep. More life."
   - "Is it for you? Basecamp is for every generation…" list, ordered by life stage
5. **Wellness & care band `#care`:** "Live well in *every season of life.*" plus a "Learn more about wellness & care →" link to `care.html`.
6. **The residences `#residences`** (navy): "A home designed to *evolve with you.*" Rendering, then six cards: Architecture, Integrated suites, Elevators, Flexible living, Ownership, Rental program.
7. **Living Here `#amenities`:** "Not an amenities package. *Your home.*" A 3×2 photo grid: Playhouse, Fly fishing, Fitness & classes / Spa, Dining, Creekside gathering.
8. **Plans `#plans`** (navy): "Homes big and small, *in the trees.*" $700s, 2027, and two renderings. **Floor plans and the site plan are on hold until the architect delivers them.**
9. **Waitlist `#waitlist`:** copy, a "Try it first" midweek-stay block, and the form (first name, last name, email).
10. **Footer:** Allenberry logo and "Pricing and plans subject to change."

## care.html: section order

1. **Header:** same as index; nav links point to `index.html#…`.
2. **Hero `#care-top`:**
   - Photo with a bottom-up gradient
   - "← Back to Basecamp" link
   - H1: "Live well in / *every season / of life.*" (forced line breaks keep it clear of the people in the photo)
   - Buttons: Join the waitlist, Explore the continuum of care
3. **Wellness & care `#care-continuum`:**
   - Heading: "A better way to live: *mind, body and community.*" with two intro paragraphs
   - Then the "The Basecamp continuum of care" label
   - Then the "Most days, residents only use Level 1…" quote
   - Then five stepped levels: Everyday wellness, Proactive health, Support at home, Recovery & respite, Acute care. Each lists Who / How / Where.
4. **The acute safety net `#care-partners`:** "Priority care when it matters, *and a clear path home.*" Steps 01–03 (Expedited placement, Specialized care, Recovery at home) beside the creek photo.
5. **The caregiver gap `#care-families`** (navy): "Built for *the family caregiver.*" Three cards: Multigenerational homes, Respite capacity, Care on demand.
6. **CTA band** (logo green): Join the waitlist (`index.html#waitlist`) and Plan a trial stay.
7. **Footer:** "Care services are in development. Details subject to change."

## Brand

| Token | Value | Use |
|---|---|---|
| Logo green (accent) | `#595C3B` | buttons, eyebrows and italic accents on light backgrounds; care CTA band |
| Sage | `#C5C9A4` | italic accents and eyebrows on navy or photos |
| Navy | `#1A2530` | text, header, dark sections |
| Navy card | `#24323F` | cards on navy |
| Paper | `#F4F1EA` / `#FBF8F2` | page / raised surfaces |
| Cream | `#E8E2D2` | Why Basecamp, continuum level 1 |
| Ink soft | `#32414E` | body copy |
| Muted | `#5A6572` | small labels |
| Rule | `#D2D4CF` | dividers |

**Type** (all from Google Fonts):

- **Fraunces** for display, weight 400. Each heading has one italic `<em>` accent phrase.
- **Inter** for body copy.
- **JetBrains Mono** for uppercase eyebrows, with 0.22em letter spacing.
- **Poppins 500** for uppercase pill buttons: 13px, 1.8px letter spacing, radius 9999px.

## Copy rules from the client

- **Partners:** never name PAM Health, York College or Burick on the site. Describe the acute partner generically ("a major healthcare provider — a leading operator of long-term acute care and inpatient rehabilitation hospitals"). The partner section was intentionally removed.
- **Students:** don't say students live on site.
  - The continuum says "Health-care students."
  - The safety net says "nursing students."
  - The client hasn't confirmed which term to use.
- **Wellness language:** frame wellness as daily life, never as being sick. Aging-in-place language stays limited to the care content.
- **Dining:** don't say "the table." The restaurants are the Barn, Breeches Café and the Terrace.
- **The Playhouse:** call it a "historic theater."
- **Homes:** say "homes," never "many homes." Every home is described as having an integrated suite and an elevator. Confirm this against the architect's plans.
- **Removed copy:** "this place has so much potential" and "Basecamp at Allenberry · Boiling Springs, PA" in the footer were both removed. Don't bring them back.
- **Investor-only content:** keep investor language (revenue lines, rental revenue, "what sets Basecamp apart") off the site.

## TODO before launch

- [ ] **Klaviyo:** set `KLAVIYO_PUBLIC_KEY` and `KLAVIYO_LIST_ID` in the `<script>` at the bottom of `index.html`, and confirm the API `revision`. Until then the form shows the success state but sends nothing.
- [ ] **Footer logo:** replace with a full-resolution Allenberry logo.
- [ ] **Site plan and floor plans:** add the architect's site plan and floor plans to `#plans` once delivered.
- [ ] **Renderings:** confirm they're final, or swap in updated ones. Keep the "Conceptual rendering" captions.
- [ ] **Verify claims:**
  - $700s pricing and 2027 timing
  - exterior maintenance
  - amenity access
  - the rental program
  - a suite and elevator in every home
  - care services and partner terms
- [ ] **Trial stay link:** currently `https://allenberry.com/stay`. Swap it for a dedicated midweek booking link if one exists.
- [ ] **Mobile nav:** links wrap under ~420px. Consider a compact menu.

## Working notes

- **Styles are inline,** because the pages were built in a visual editor. If you refactor to shared CSS, keep the tokens above and compare 1440px and 390px widths against `docs/`.
- **Responsive grids** use `repeat(auto-fit, minmax(min(Npx, 100%), 1fr))` so they collapse to one column on phones.
- **Hero darkening on phones:** both heroes use a `.care-hero-shade` overlay, which a `max-width: 760px` media query strengthens.
- **Shared header and footer:** keep them identical on both pages.
