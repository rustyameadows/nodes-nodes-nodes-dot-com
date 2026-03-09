# Nodes Nodes Nodes Visual Asset System

## Purpose
This document defines how screenshots and illustrations should be used across the marketing site so future updates feel deliberate instead of improvised.

## Asset Roles
- Real product screenshots are proof assets. Use them whenever the goal is trust, capability proof, or product authority.
- Illustrations are supporting/editorial assets. Use them to explain flow, add atmosphere, or fill places where a real screenshot would be less clear.
- If a real screenshot exists for a slot, it should win over an illustration.

## Current Rule
- The only approved product screenshot currently in the site repo is `assets/hero-beauty.png`.
- Do not pull additional repo screenshots into the site without explicitly replacing them with a fresh requested pack.

## Screenshot Contract
Request and store future screenshots under these filenames:
- `assets/hero-beauty.png`
  - full app window
  - landscape
  - pink or warm backdrop acceptable
  - minimum `2200px` wide
- `assets/screen-canvas.png`
  - in-app canvas workflow
  - minimum `1440x960`
  - no browser chrome
- `assets/screen-queue.png`
  - queue plus request-response or debug visibility
  - minimum `1440x960`
  - no clipped inspector panels
- `assets/screen-assets.png`
  - asset review / compare view
  - minimum `1440x960`
  - no unreadable thumbnail labels
- `assets/screen-app-home.png`
  - project picker or home/project-management view
  - minimum `1440x960`
  - clearly legible project controls

## Screenshot Capture Guidance
- Include the app window, not browser chrome.
- Export retina-quality PNGs when possible.
- Prefer real product state over staged decorative mockups.
- Avoid clipped labels, cropped panels, tiny unreadable text, or transient debugging junk unless the screenshot is specifically for a debugging feature.
- Keep the capture calm: one clear story per image.

## Illustration System
Use illustrations only as supporting media and keep them inside this family:
- palette:
  - stone outer fields
  - ink interiors
  - citrus, aqua, coral, and amber accents
- role:
  - editorial support
  - explanatory diagrams
  - OG or decorative context when a screenshot is already carrying proof
- never:
  - use illustration as the primary hero proof when a real screenshot exists
  - fake dense UI with tiny unreadable labels
  - let decorative shapes overlap important text or crop awkwardly

## Composition Rules
- No chopped text.
- No floating random ornaments without a compositional role.
- No accidental overlaps between frames, labels, and connector lines.
- Text inside illustrations must be large, sparse, and UI-like.
- Keep all critical content inside a consistent inset so the asset survives card crops and social crops.

## Review Checklist
Before approving any illustration or SVG-derived asset:
- render the SVG to PNG
- inspect it at full size
- inspect it at thumbnail size
- inspect the mobile crop
- verify that no text is clipped
- verify that no linework or framing feels accidental

## Template
- Start future editorial illustrations from `assets/illustration-template.svg`.
- Reuse the same safe areas, frame language, and palette relationships instead of drawing each asset from scratch.
