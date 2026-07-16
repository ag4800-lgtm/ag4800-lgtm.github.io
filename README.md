# The Language Blueprint LLC — Website & Business Docs

This folder contains your full website and core business documents.

```
index.html              Homepage
services.html            Services & pricing (with payment buttons)
contact.html             Contact form + consultation booking
intake.html              Client intake form
privacy-policy.html      Privacy policy
terms-of-service.html    Terms of service
css/style.css            Site styling
js/main.js               Mobile nav toggle, footer year
assets/logo-icon.svg      Icon-only logo (used in the nav + favicon)
assets/logo-full.svg      Icon + wordmark lockup (for letterhead, social profiles, etc.)
assets/favicon.svg        Browser tab icon
docs/                     Operating Agreement, Consulting Agreement, DPA,
                          proposal template, invoice template, checklists,
                          LinkedIn copy — see docs/00-READ-ME-FIRST.md
```

## 1. Preview the site locally

No build step needed. Easiest option — just double-click `index.html` to open it in a browser. If you want it served properly (recommended so forms/links behave like production):

```
cd "The Language Blueprint LLC"
python -m http.server 8000
```

Then visit `http://localhost:8000`.

## 2. Wire up payments (Stripe Payment Links — no code required)

Every "Pay" / "Enroll" button on `services.html` currently points to a placeholder URL like `https://buy.stripe.com/REPLACE_WITH_...`. To make them real:

1. Create a free account at [stripe.com](https://stripe.com) and complete business verification.
2. In the Stripe Dashboard, go to **Payment Links** → **New**.
3. Create one payment link per package (District Consulting, AI Tool Pilot, Student Standard, Student Intensive, Writing Mentorship, Teacher Mentorship) with the matching price.
4. Copy each generated link and paste it over the matching placeholder `href` in `services.html` (search the file for `REPLACE_WITH`).

Stripe handles all card data and PCI compliance — you never touch raw card numbers, and money lands directly in your Stripe/bank account.

## 3. Wire up the forms (Formspree — no backend required)

`contact.html` and `intake.html` submit via [Formspree](https://formspree.io):

1. Create a free Formspree account.
2. Create **two** forms — one for general contact, one for client intake (keeping them separate makes it easy to filter submissions later).
3. Copy each form's endpoint URL and paste it over `YOUR_FORM_ID` in `contact.html` and `YOUR_INTAKE_FORM_ID` in `intake.html`.
4. Formspree will email you each submission and let you export them to CSV.

## 4. Add consultation booking

`contact.html` has a placeholder where a Calendly (or Google Calendar appointment) embed goes:

1. Create a free [Calendly](https://calendly.com) account and set up an event type (e.g. "Free 20-Minute Consultation").
2. Use Calendly's "Add to Website" → "Inline Embed" option to get a code snippet.
3. Paste that snippet into `contact.html` where the comment says so.

## 5. Fill in remaining placeholders

Search the project for these and replace them:

- Phone number (`contact.html`, `index.html`, `docs/invoice-template.md`)
- Any `[bracketed]` placeholder in the `docs/` files

## 6. Deploy the site

Since this is a plain static site, any of these work (all have free tiers):

- **Netlify** — drag-and-drop the whole folder at [app.netlify.com/drop](https://app.netlify.com/drop)
- **GitHub Pages** — push this folder to a GitHub repo and enable Pages in repo settings
- **Vercel** — `vercel` CLI or drag-and-drop deploy

Once deployed, point your domain (`thelanguageblueprint.org`) at it via your domain registrar's DNS settings — Netlify/Vercel both walk you through this.

## 7. Before you take your first paying client

Read `docs/00-READ-ME-FIRST.md`. Short version: get the Operating Agreement, Consulting Agreement, and DPA reviewed by a licensed NY attorney, and get your General Liability + Professional Liability insurance quotes locked in — several of the contract clauses assume that coverage exists.
