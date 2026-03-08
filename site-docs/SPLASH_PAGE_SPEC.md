# Nodes Nodes Nodes Splash Page Spec

## Goal
Ship a one-page splash site that explains the product clearly, establishes the black-and-white brand direction, and captures intent around two future actions:
- primary CTA: `Join the waitlist`
- secondary CTA: `Download the alpha`

This first pass is plain static HTML/CSS/JS hosted on GitHub Pages with no backend form handling.

## Audience
Primary audience:
- creative AI power users

Secondary audience:
- designers, artists, and creative technologists who want a more structured workflow than separate provider tabs

## Page Objective
After one scroll, a visitor should understand:
1. this is a local-first macOS desktop app
2. it is for building and reviewing creative AI workflows
3. it is early, not a broad public release
4. waitlist and alpha access are planned, but not wired yet

## Visual Direction
- black background, white foreground, grayscale accents only
- strong typography and spacing over decorative effects
- no gradients, color pops, or glassmorphism in the first pass
- use one accent treatment only: thin borders and subtle section dividers
- screenshots are optional placeholders until real captures exist

## Page Structure

### 1. Hero
Purpose:
- identify the product
- establish the category
- present the two CTA labels immediately

Required content:
- small eyebrow: `LOCAL-FIRST DESKTOP FOR CREATIVE AI WORKFLOWS`
- product name: `Nodes Nodes Nodes`
- one hero headline
- one supporting paragraph
- primary and secondary CTA buttons
- a short alpha-status line directly below the CTAs

Approved headline options:
1. `Build creative AI workflows, not prompt clutter.`
2. `A local-first desktop app for serious creative AI workflows.`
3. `From prompt to review, keep the whole workflow in one place.`

Approved supporting copy options:
1. `Nodes Nodes Nodes gives you a project-based canvas for running models, connecting assets and notes, and reviewing outputs without losing the thread.`
2. `Build generation flows on an infinite canvas, run supported providers from one interface, and compare outputs in a review-first desktop app.`

CTA behavior for v1:
- `Join the waitlist` links to `#alpha-access`
- `Download the alpha` links to `/download/`
- both buttons are active anchor links, not form submits

Alpha-status line:
- `macOS alpha. Waitlist and public download flow coming soon.`

### 2. Value Props
Purpose:
- explain why this is different from provider-specific tools

Layout:
- three equal-width cards on desktop
- stacked cards on mobile

Required cards:
1. `Build on a canvas`
   - `Connect prompts, notes, templates, and assets in one visual workflow.`
2. `Run in one interface`
   - `Use supported providers without breaking the flow across tabs and tools.`
3. `Review like it matters`
   - `Compare outputs, tag them, rate them, and filter what survives.`

### 3. How It Works
Purpose:
- make the workflow concrete in three steps

Required steps:
1. `Start a project`
   - `Create or reopen a project and land in a dedicated workspace.`
2. `Build and run`
   - `Add nodes, connect the graph, and run supported model steps from the canvas.`
3. `Review and iterate`
   - `Inspect outputs in the asset viewer, compare versions, and feed results back into the workflow.`

### 4. Product Surfaces
Purpose:
- show the app has distinct product surfaces, not just one screen

Required tiles:
1. `App Home`
   - `Create, reopen, and switch isolated projects.`
2. `Canvas`
   - `Build the workflow with notes, templates, model nodes, and asset pointers.`
3. `Queue`
   - `See job state and inspect what is running.`
4. `Assets`
   - `Review outputs in grid, 2-up, and 4-up comparison views.`

Screenshot placeholder rules:
- each tile may use a grayscale screenshot placeholder block
- if no real screenshots exist, use labeled boxes only
- placeholder labels must read `APP HOME`, `CANVAS`, `QUEUE`, and `ASSETS`

### 5. Alpha Access Section
Section id:
- `alpha-access`

Purpose:
- explain the product status honestly
- hold both placeholder CTA outcomes in one location

Required copy:
- heading: `Early access, not a broad public release.`
- body: `Nodes Nodes Nodes is currently a macOS alpha in active development. The waitlist flow and public alpha distribution are still being finalized.`

Required CTA cards:
1. `Join the waitlist`
   - status line: `Waitlist provider not selected yet.`
   - helper copy: `Reserve this slot for the future signup action or embed.`
2. `Download the alpha`
   - status line: `Public download link not posted yet.`
   - helper copy: `Future target should be a GitHub Releases artifact or release page.`

### 6. FAQ
Purpose:
- answer the obvious objections without overexplaining

Required questions and approved answers:

`What is Nodes Nodes Nodes?`
- `A local-first desktop app for building, running, and reviewing creative AI workflows.`

`Is it available right now?`
- `It is in macOS alpha and still being prepared for broader access.`

`Does it run in the browser?`
- `No. The current product is a desktop app.`

`Does it support collaboration or cloud sync?`
- `Not in the current version. The product is local-first and single-user today.`

`What providers does it support?`
- `The current product docs describe OpenAI and Topaz support in the active workflow.`

### 7. Footer
Required content:
- product name
- one-line descriptor: `Local-first desktop for creative AI workflows.`
- text nav to future routes: `/product/`, `/workflow/`, `/download/`, `/faq/`, `/privacy/`
- copyright placeholder

## Implementation Notes
- build the page as semantic sections with anchor-friendly ids
- do not include a real email form, embedded newsletter form, or download artifact in v1
- keep copy close to the approved wording in this doc
- the first implementation should work cleanly with no JavaScript beyond optional menu toggles or smooth-scroll behavior
- mobile behavior matters: hero CTAs stack, value cards stack, and product-surface tiles collapse to one column
