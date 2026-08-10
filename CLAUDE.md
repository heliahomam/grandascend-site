# GrandAscend Website

Luxury social media and brand strategy agency based in Montreal.
Founder and Creative Director: Helia Homam.
Live at grandascend.co, hosted on Netlify.

## Who you are working with

Helia is a founder and creative director, not a developer. She has a
strong visual eye and works in Figma, Canva, Shopify, and Notion.
She does not use a terminal.

Explain what you did in plain language. Skip the jargon, or define it
in one short clause if you must use it. Say what changed and what it
means for the live site, not which git commands you ran.

## Stack

Plain HTML and CSS. No framework, no build step, no package manager.
Netlify deploys automatically from the `main` branch.

- `index.html` — homepage, all styles inline in a `<style>` block
- `careers.html` — careers page with a Netlify Forms application form
- `images/` — all site imagery (SVG and JPEG)

## Critical constraints

**Do not break the careers form.** `careers.html` contains Netlify
Forms markup: `data-netlify="true"`, a hidden `form-name` input set to
`grandascend-application`, and a `netlify-honeypot="bot-field"` field.
If any of that is removed or renamed, job applications stop arriving.

**Never inline images as base64.** The site previously had every image
embedded as a base64 data URI, which made index.html 37MB and destroyed
load performance. Images must stay as separate files in `images/`.

## Brand system

Colours:
- Charcoal `#2A2A2A` — primary text
- Cream `#F5F0E8` — page background
- Gold `#B5A898` — accents
- Taupe `#8C7E72` — secondary text

Typography:
- Cormorant Garamond — headings and display
- Montserrat — body, labels, buttons (light and regular weights)

Aesthetic: editorial, restrained, cinematic. Generous whitespace.
Confidence comes from restraint, not decoration.

## Copy rules

**Never use an em dash.** Use a comma, a period, or rewrite the
sentence. This applies to all site copy without exception.

The LVMH Inside Certificate in Creation & Branding and Retail &
Customer Experience is the single strongest differentiator. No other
Montreal boutique agency leads with it. Keep it prominent and above
the fold.

## Working style

- Always work on a branch and open a pull request. Never push to `main`.
- Netlify builds a deploy preview on every PR. That preview is how
  Helia reviews work, so mention it when a PR is ready.
- One task per session where possible. Small, reversible changes.
- Flag anything that would affect the live site before doing it.

## Known outstanding work

- Several images are oversized and should be compressed: one SVG at
  ~6.4MB and three JPEGs between 3.5MB and 4.8MB. Target under 400KB
  each. Consider WebP with JPEG fallbacks.
- Homepage stat counters have been reported as displaying incorrectly.
- A case study page for Roza Grip Socks is planned but not built.
