# Basecamp at Allenberry: landing page v2

A single landing page for **Basecamp at Allenberry**, a community of homes on the grounds of the historic Allenberry Resort in Boiling Springs, PA. It's static HTML with no build step, deployed on Netlify (see `netlify.toml`).

v2 replaces the two-page v1 site (landing page plus `care.html`). All of the care content now lives on this one page.

## Audience and goal

The page is for **potential buyers**. It introduces the concept and measures interest through the "Register your interest" form. It is not a sales page: leave detailed pricing off.

## Positioning

- **Lead with the difference.** Concierge health and wellness is built into where you live, in a community where you own the home, with resort amenities on the property. Nothing else offers all three.
- **Fill the gap.** Basecamp sits between staying in a house that wasn't built for the years ahead and moving into a care community. Never use the words "CCRC" or "missing middle."
- **Intergenerational, not senior-only.** People of any age can live here, including those who want full healthcare but aren't of senior age. Use the word "intergenerational." Don't list types of people, and don't mention young families. The intro draws on how families used to live, with elders staying at home and part of the community.
- **"Aging in place" is back.** The client first replaced it with "lifelong living," then restored it in the hero subhead and the register-interest intro. Don't add it anywhere else without asking.
- **Ownership over entrance fees.** You invest in a home you keep, not an entrance fee and monthly fees you never get back. Don't do a dollar-for-dollar comparison.
- **Tone:** bold and optimistic. No anxious or "scary" framing.

## index.html: section order

1. **Header:** Basecamp logo. Nav: The Homes, Why Basecamp, Wellness & Care, Living Here, Plans. "Register interest" pill.
2. **Hero `#top`:** aerial rendering.
   - H1: "Basecamp *at Allenberry*"
   - Subhead: "Healthy living and aging in place, *reimagined.*"
   - Buttons: Register interest, Explore the homes
3. **Intro `#different`** (page background): "Concierge health and wellness, *built into where you live.*"
   - Two paragraphs: the gap between staying in your house and moving for care; Basecamp as your home base, an intergenerational neighborhood.
   - Wide street rendering below.
4. **Wellness & care `#care`** (cream): "Care that *comes to you.*"
   - Two intro paragraphs
   - Golden-hour stroll photo
5. **Partners `#care-partners`** (cream): "World-class partners. *Care close to home.*" Three partner cards (Burick Center, PAM Health, Choice Health At Home), each with the partner's logo (`assets/logo-burick.webp`, `logo-pam.webp`, `logo-choice.webp`) and copy kept roughly equal in length, then:
   - Green box: "Concierge medicine, *for every resident.*" "A Burick Center concierge health membership is included in the cost of every home."
   - "What concierge care *really means.*" Three cards covering only what the membership includes: direct physician access, the annual whole-health evaluation, and longevity programming.
6. **More support `#care-package`** (cream): "More support, *only if you need it.*\*" Six optional cards in two rows of three, kept roughly equal in length: check-ups and same-day care, the PAM Health nurse navigator, recovery at home, help at home, hyperbaric therapy, and housekeeping and laundry. Footnote under the cards: "\* These services come at an additional cost, and may be paid directly, or covered by Medicare, Medicaid or insurance, depending on the service." Keep anything beyond the three membership items here.
7. **Own the asset `#care-costs`** (paper, rule below): "Own the asset, *skip the entrance fee.*" Two cards with no dollar figures: a typical care community vs. Basecamp.
9. **The caregiver gap `#care-families`:** hidden for now (`hidden` attribute). The client may bring it back.
10. **Residences `#residences`** (navy): "A home you own, *built for every chapter.*"
    - Stats (`#plans`): $700s, 2027
    - Residence rendering
    - Three cards: Architecture, Integrated suites, Elevators
11. **Living Here `#amenities`:** six amenity photos. The Playhouse, Fly fishing, Fitness & classes, The Spa, Dining, Creekside gathering.
12. **Register interest `#waitlist`:** "Could you see yourself *here?*", the "Try it first" trial-stay block, and the form.
13. **Footer:** Allenberry logo and "Pricing and plans subject to change."

Spacing: each section has 96px of top and bottom padding. The exception is the cream care block (`#care`, `#care-partners`, `#care-package`), which uses 48px between its parts so it reads as one block.

## Copy rules from the client

- **Membership price:** the concierge medicine membership costs $3,000 a year and is built into the home's purchase price. There is no monthly fee and nothing paid through HOA dues. Say it's "included in the cost of every home" (or "comes with every home"); never imply it's free, and never mention a monthly or HOA fee for it. Keep the dollar figure off the page unless asked.
- **No "24/7":** the client removed it from the PAM Health nurse navigator copy. Don't promise round-the-clock access.
- **Partners:** naming PAM Health, the Burick Center and Choice Health At Home is approved for v2. Choice is Basecamp's designated home care partner. This reverses the v1 rule. Keep confidential partnership terms (pricing, revenue share, contract details) off the site.
- **Removed copy, don't bring back:**
  - "Other communities make you choose"
  - "Less upkeep, more life"
  - "Is it for you?"
  - "Allenberry, reimagined"
  - the resident journey
  - the care ladder
  - the acute safety net section (its points now live in the "Recover in your own living room" card)
  - the "Flexible living," "Ownership" and "Rental program" cards
  - "One care plan per household"
  - all eyebrow labels
- **Names:** always write "The Playhouse" and "The Spa" with a capital T. Don't say "Allenberry Hotel."
- **Don't repeat "Imagine"** as a card lead-in.
- **"Where you live"** should appear only once, in the intro headline.
- **Dining:** the restaurants are the Barn, Breeches Café and the Terrace.
- **Investor-only content:** keep investor language off the site.

## Brand

| Token | Value | Use |
|---|---|---|
| Logo green (accent) | `#595C3B` | buttons, italic accents on light backgrounds, membership box |
| Sage | `#C5C9A4` | italic accents on navy or photos |
| Navy | `#1A2530` | text, header, dark sections, Basecamp cost card |
| Paper | `#F4F1EA` / `#FBF8F2` | page / raised surfaces |
| Cream | `#E8E2D2` | care block |
| Ink soft | `#32414E` | body copy |
| Muted | `#5A6572` | small labels |
| Rule | `#D2D4CF` | dividers |

**Type** (Google Fonts):

- **Fraunces 400** for display. Each heading has one italic `<em>` accent phrase.
- **Inter** for body copy.
- **JetBrains Mono** for small uppercase labels only.
- **Poppins 500** for uppercase pill buttons: 13px, 1.8px letter spacing.

## Register-interest form → Klaviyo

The form (`#waitlist-form`) collects:

- **Required:** first name, last name, email.
- **Optional:** "How would you use a home here?" (`home_use`), "When might you consider a move?" (`timeline`), "What interests you most?" checkboxes (`interests`), and "I want to schedule a trial stay" (`trial_stay`). The "Plan a trial stay" button scrolls to the form and ticks that box; it does not go to the booking engine.

The script at the bottom of `index.html` sends a Klaviyo subscription. The optional answers go on the profile as `basecamp_home_use`, `basecamp_timeline` and `basecamp_interests`, `basecamp_trial_stay`, along with any UTM parameters, using source "Basecamp Website v2".

The keys are set, so live submissions go to the Klaviyo list.

## TODO before launch

- [x] **Klaviyo:** public key `TjnXN7` and list `RnJtAH` are set. A test submission returned 202. Confirm the API `revision` date is still supported.
- [ ] **Orvis logo:** add it to the Fly fishing card and confirm the approved wording for the relationship. The Orvis Endorsed badge used in v1 is still in `assets/orvis-endorsed.webp`; confirm with the client whether it's the official file.
- [ ] **Disclaimer:** consider a footer note. Care services are in development, pricing is subject to change, and covered services are billed to the resident's insurance.
- [ ] **Verify claims:**
  - $700s pricing and 2027 timing
  - membership inclusion
  - partner services
  - the suite and elevator in every home
- [ ] **Assets:**
  - footer logo: swap in a full-resolution Allenberry logo
  - renderings: confirm they're final, and keep the "Conceptual rendering" captions
- [x] **Mobile nav:** below 1080px the nav collapses into a hamburger menu (`.nav-toggle`); the Register interest pill sits at the bottom of the open menu.

## Working notes

- **Inline styles:** the page was built in a visual editor, so styles are inline. If you refactor to shared CSS, keep the tokens above and compare 1440px and 390px widths against `docs/`.
- **Responsive grids** use `repeat(auto-fit, minmax(min(Npx, 100%), 1fr))` so they collapse on phones.
- **Old care page:** `netlify.toml` redirects `/care.html` and `/care` to `/#care`.
- **Unused v1 assets:** `render-lane.jpg`, `render-cottage.jpg`, `care-hero-walk.jpg` and `creek-golden-hour.jpg` were intentionally dropped from v2.
