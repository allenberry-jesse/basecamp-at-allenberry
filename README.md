# Basecamp at Allenberry

Website for Basecamp at Allenberry, a multigenerational community of homes on the grounds of the historic Allenberry Resort in Boiling Springs, PA.

It's a static site with no build step and two pages:

- `index.html`: the landing page
- `care.html`: the Wellness & Care page

## Preview locally

```bash
python3 -m http.server 8000
# then visit http://localhost:8000
```

## Deploy (Netlify)

There are two ways to deploy:

- **From GitHub:** push this folder to a repo. In Netlify, choose *Add new site → Import an existing project*. Leave the build command empty. The publish directory is `.`, which is already set in `netlify.toml`.
- **Drag and drop:** zip the folder, then drop it on *Netlify → Sites → Deploy manually*.

## Before going live

See the TODO list in `CLAUDE.md`. The main items are:

- Klaviyo keys
- the architect's site plan and floor plans
- a full-resolution footer logo
- confirming pricing, timing and service claims

## Working with Claude Code

Open this folder in Claude Code. `CLAUDE.md` covers the page structure, positioning, brand tokens, client copy rules and open items, so you can ask for changes directly. For example:

- "add the site plan to the Plans section"
- "hook up Klaviyo with these keys"
- "build a compact mobile menu"
