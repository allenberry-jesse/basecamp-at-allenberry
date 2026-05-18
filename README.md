# Basecamp at Allenberry

Single-page teaser site for the Basecamp at Allenberry residential community.
Static HTML — no build step, no dependencies.

## Stack

- One HTML file (`index.html`) with inline CSS and a tiny JS for scroll reveals + nav state
- Local images in `assets/`
- Google Fonts (Fraunces, Inter, JetBrains Mono) loaded from CDN
- Two Unsplash photos referenced by direct CDN URL (in the Programming section)
- Favicon: `assets/favicon.svg`

## Deploying to Netlify

### Option A — Push to GitHub, link the repo

1. Create a new GitHub repo (private or public).
2. From this folder:
   ```bash
   git init
   git add .
   git commit -m "Initial commit"
   git branch -M main
   git remote add origin git@github.com:<you>/<repo>.git
   git push -u origin main
   ```
3. In Netlify, **Add new site → Import an existing project → GitHub** → pick the repo.
4. Build settings:
   - **Build command:** *(leave empty)*
   - **Publish directory:** `.` (the repo root)
5. Deploy.

Once linked, every push to `main` re-deploys; every PR generates a deploy preview.

### Option B — Drag-and-drop

Zip this folder and drag onto **Netlify → Sites → Add new site → Deploy manually**.
Works for a one-off preview, but you lose the GitHub workflow.

## new.allenberry.com

You mentioned `new.allenberry.com` is already wired up for deploy previews.
Netlify's deploy-preview URLs look like:

```
deploy-preview-<PR#>--<site-name>.netlify.app
```

If you've configured branch subdomains (Netlify → Domain management → Branch
subdomain), pushes to a branch named e.g. `preview` will publish at
`preview.new.allenberry.com` (or whatever pattern you set up).

For a one-off review URL: push to a branch, open a PR, and Netlify will post
the deploy-preview link in the PR.

## File map

```
index.html                  the whole site
assets/
  basecamp-phase1.webp      hero image (charred residences at dusk)
  allenberry-aerial.png     The Place — aerial of Allenberry
  bend-dusk-house-2.webp    Life gallery
  bend-exterior-2.webp        ”
  bend-exterior-3.webp        ”
  bend-exterior-4.webp        ”
  interior-2.webp             ”
  interior-3.webp             ”
  interior-4.webp             ”
  favicon.svg
netlify.toml                deploy config
.gitignore
README.md
```

## Editing

`index.html` is the only file you need to touch for content. It's organized
top-to-bottom in sections; comments mark each one:

```
01 — HERO
02 — MANIFESTO
03 — THE IDEA
04 — WHO LIVES HERE
05 — THE PLACE
06 — MISSING MIDDLE
07 — THE HOMES        (CSS only — section removed from markup)
08 — THE SITE         (CSS only — section removed from markup)
09 — THE LIFE
10 — THE PROGRAMMING
11 — DEDICATION
```

The Homes and Site CSS is retained in case those sections come back; they cost
nothing while unused.

## Swapping images

- **Local images** — replace files in `assets/`, keep the filename, or update the
  `src=` in `index.html`.
- **Unsplash** (two tiles in the Programming section) — open any Unsplash photo
  page, copy the `og:image` URL (or the `images.unsplash.com/photo-...` src),
  and paste it into the corresponding `<img src=…>`.

## License & credits

- Bend reference photos: from Basecamp Tetherow, Bend OR (used as visual
  reference; swap before public publication).
- Allenberry aerial: courtesy of the Allenberry Resort archive.
- Unsplash images in the Programming section: free under the Unsplash License.
- Fonts: Fraunces (SIL OFL), Inter (SIL OFL), JetBrains Mono (SIL OFL).
