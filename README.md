# Basecamp at Allenberry: landing page v2

This is a single landing page for Basecamp at Allenberry: homes you own on the grounds of the historic Allenberry Resort in Boiling Springs, PA, with concierge health and wellness built in. Its purpose is to introduce the concept to potential buyers and see how much interest there is.

It's a static site with no build step. Everything is in `index.html` and `assets/`.

## Preview locally

```bash
python3 -m http.server 8000
# then visit http://localhost:8000
```

## Deploy (Netlify)

There are two ways to deploy:

- **From GitHub:** push this folder to a repo. In Netlify, choose *Add new site → Import an existing project*. Leave the build command empty. The publish directory is `.`.
- **Drag and drop:** drop the folder on *Netlify → Sites → Deploy manually*.

## Before going live

The full TODO list is in `CLAUDE.md`. The main items are:

- Klaviyo keys
- the Orvis logo
- a footer disclaimer
- confirming pricing, timing and service claims

## Working with Claude Code

Open this folder in Claude Code. `CLAUDE.md` covers the section order, positioning, copy rules, brand tokens and the form fields, so you can ask for changes directly. For example:

- "hook up Klaviyo with these keys"
- "add the Orvis logo to the fly fishing card"
- "build a compact mobile menu"
