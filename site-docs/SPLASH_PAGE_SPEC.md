# Nodes Nodes Nodes Splash Page Spec

## Goal
Ship a one-page splash site that explains the product clearly, establishes a light warm brand direction that still feels related to the app, and captures intent around two future actions:
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
4. waitlist is still a placeholder, and current alpha access can hand people to the GitHub repo

## Visual Direction
- light stone backgrounds with dark ink text
- citrus, aqua, coral, and amber accents used sparingly
- dark-canvas energy should live inside mock screens and media frames, not as a full-site theme
- strong typography and spacing over ornamental effects
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
- `Very early macOS alpha. Waitlist placeholder, GitHub repo for current access.`

### 2. Value Props
Purpose:
- explain why this is different from provider-specific tools

Layout:
- four equal-width cards on desktop
- stacked cards on mobile

Required cards:
1. `Infinite canvas workflows`
   - `Connect prompt notes, lists, templates, assets, and model nodes on one graph.`
2. `Text, data, images, video, files`
   - `Work across mixed inputs and outputs without flattening everything into one chat transcript.`
3. `Local tools + provider keys`
   - `Bring your own keys, wire in local tools, and keep provider execution inside the workflow.`
4. `Debug, inspect, iterate`
   - `Read queue state and provider request-response details, then compare outputs and loop back into the graph.`

### 3. How It Works
Purpose:
- make the workflow concrete in three steps

Required steps:
1. `Start a local project`
   - `Create or reopen a workspace so files, metadata, and outputs stay attached to one home.`
2. `Connect the graph`
   - `Add nodes, notes, templates, tools, and assets to the canvas, then wire the flow you need.`
3. `Run, inspect, and compare`
   - `Inspect queue state, request-response detail, and outputs before feeding results back into the workflow.`

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
- each tile may use a stylized screenshot placeholder block
- if no real screenshots exist, use labeled boxes only
- placeholder labels must read `APP HOME`, `CANVAS`, `QUEUE`, and `ASSETS`

### 5. Alpha Access Section
Section id:
- `alpha-access`

Purpose:
- explain the product status honestly
- hold both placeholder CTA outcomes in one location

Required copy:
- heading: `Very early alpha, living on GitHub for now.`
- body: `Nodes Nodes Nodes is currently a macOS alpha in active development. The waitlist flow is still a placeholder, and the GitHub repo is the current source of truth for early access.`

Required CTA cards:
1. `Join the waitlist`
   - status line: `Waitlist provider not selected yet.`
   - helper copy: `Reserve this slot for the future signup action or embed.`
2. `Download the alpha`
   - status line: `GitHub repo is the current early-alpha handoff.`
   - helper copy: `Explain that the build is very early, macOS first, unsigned, and may require using repo instructions.`

### 6. FAQ
Purpose:
- answer the obvious objections without overexplaining

Required questions and approved answers:

`What is Nodes Nodes Nodes?`
- `A local-first desktop app for building, running, debugging, and reviewing creative AI workflows.`

`Is it available right now?`
- `It is a very early macOS alpha, and the GitHub repo is the current source of truth for access.`

`Does it run in the browser?`
- `No. The current product is a desktop app.`

`Does it support collaboration or cloud sync?`
- `Not in the current version. The product is local-first and single-user today.`

`What providers does it support?`
- `The current product docs describe OpenAI, Google Gemini, and Topaz support in the active workflow.`

### 7. Footer
Required content:
- product name
- one-line descriptor: `Local-first desktop for creative AI workflows.`
- text nav to future routes: `/product/`, `/workflow/`, `/download/`, `/faq/`, `/privacy/`
- copyright placeholder

## Implementation Notes
- build the page as semantic sections with anchor-friendly ids
- do not include a real email form or embedded newsletter form in v1
- `/download/` may hand off to the GitHub repo instead of hosting artifacts directly
- keep copy close to the approved wording in this doc
- the first implementation should work cleanly with no JavaScript beyond optional menu toggles or smooth-scroll behavior
- mobile behavior matters: hero CTAs stack, value cards stack, and product-surface tiles collapse to one column
