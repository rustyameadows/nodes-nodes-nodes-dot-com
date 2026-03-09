# Nodes Nodes Nodes Marketing Site Map

## Purpose
This document defines the full marketing-site information architecture after the splash page. It keeps the public site small, honest, and implementable as a static site.

## Global Rules
- every page uses `Nodes Nodes Nodes` branding only
- the primary site audience is creative AI power users
- the site must not claim collaboration, cloud sync, Windows support, or a broad public release
- the primary global CTA label remains `Join the waitlist`
- the secondary global CTA label remains `Download the alpha`
- until the real integrations exist, the waitlist remains a placeholder destination and `/download/` should honestly hand people to the GitHub repo

## Global Navigation
Required nav items:
- `Product`
- `Workflow`
- `Download`
- `FAQ`

Home behavior:
- clicking the wordmark returns to `/`

Footer links:
- `/product/`
- `/workflow/`
- `/download/`
- `/faq/`
- `/privacy/`

## Route Plan

### `/`
Goal:
- explain the product fast and convert interest into future alpha intent

Required sections:
- hero
- value props
- how it works
- product surfaces
- alpha access
- FAQ preview

Primary CTA:
- `Join the waitlist`

Secondary CTA:
- `Download the alpha`

Allowed placeholders:
- screenshot boxes
- placeholder CTA destinations

### `/product/`
Goal:
- explain what the app is and why it exists

Required sections:
- product overview
- core differentiators
- local-first desktop explanation
- current supported workflow surfaces
- alpha status note

Copy emphasis:
- project-based workflow
- infinite canvas
- integrated queue
- comparison-oriented asset review

Allowed placeholders:
- stylized UI mock blocks

### `/workflow/`
Goal:
- show how a real workflow moves through the app

Required sections:
- step-by-step workflow narrative
- canvas explanation
- run and queue explanation
- review and iteration explanation
- short “who this is for” section

Copy emphasis:
- start a project
- build and connect nodes
- run supported providers
- compare outputs and iterate

Allowed placeholders:
- numbered diagrams rendered as static blocks or simple SVG

### `/download/`
Goal:
- become the eventual distribution page for the macOS alpha

Required sections for v1:
- current status message
- macOS alpha label
- GitHub repo handoff
- system expectations note
- source-run fallback note

Required status copy:
- `The current early alpha lives on GitHub.`
- `Expect a very early macOS-first, unsigned Apple Silicon build with repo-driven install notes.`

Allowed placeholders:
- GitHub handoff card
- expectations card

### `/faq/`
Goal:
- answer common availability, platform, and product-scope questions

Required sections:
- general FAQ
- platform and availability FAQ
- workflow and provider FAQ
- privacy and local-first FAQ

Required topics:
- what the app is
- who it is for
- current platform support
- whether it runs in the browser
- collaboration and sync status
- provider support at a high level

### `/privacy/`
Goal:
- provide a minimal, honest placeholder privacy page until legal copy is formalized

Required sections:
- page scope notice
- local-first product statement
- analytics statement placeholder
- contact and policy-owner placeholder
- future update notice

Required constraints:
- do not invent legal guarantees not backed by an adopted policy
- clearly mark the page as a draft placeholder pending formal review

## Content Relationships
- `/` is short and conversion-oriented
- `/product/` expands the product story
- `/workflow/` expands the user journey
- `/download/` holds distribution status and later release links
- `/faq/` handles objections and scope boundaries
- `/privacy/` exists early so the public site has a stable policy route

## Copy Inventory To Reuse
Use these exact phrases repeatedly where appropriate:
- `local-first desktop`
- `creative AI workflows`
- `macOS alpha`
- `Join the waitlist`
- `Download the alpha`

## Implementation Defaults
- one shared stylesheet across all routes
- one shared header and footer pattern
- no client-side router required
- each route is a real static HTML file under its own folder
