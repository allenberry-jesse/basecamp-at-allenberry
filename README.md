# Basecamp at Allenberry

Landing page for Basecamp at Allenberry — a resort community on the grounds of Allenberry Resort & Spa, Boiling Springs, PA.

Static site: one `index.html` plus `assets/`. No build step, no dependencies.

## Preview locally

Open `index.html` in a browser, or serve the folder:

```bash
python3 -m http.server 8000
# then visit http://localhost:8000
```

## Deploy (Netlify)

**GitHub:** push this folder to a repo, then in Netlify choose *Add new site → Import an existing project*. Leave the build command empty and set the publish directory to `.` (already set in `netlify.toml`).

**Drag and drop:** zip the folder and drop it on *Netlify → Sites → Deploy manually*.

## Before going live

See the TODO list in `CLAUDE.md`. The main items are the Klaviyo keys, the full-res logo, real renderings, floor plans and the site plan.

## Working with Claude Code

Open this folder in Claude Code. `CLAUDE.md` has the page structure, brand tokens, copy rules and open items, so you can ask for changes directly (for example, "add the floor plans for The Cottage" or "hook up Klaviyo with these keys").
