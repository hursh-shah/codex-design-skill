---
name: ui-design
description: Create distinctive, production-grade frontend interfaces directly in code with a strong visual point of view. Use when Codex is asked to design or redesign a page, screen, flow, or component; improve UI quality; or ship polished frontend experiences that must feel intentional and non-generic. Default to Next.js unless the user specifies another framework, and use targeted 21st.dev inspiration with screenshot capture only for specific components that need references.
---

# UI Design

## Overview

Build frontend code directly in the user's project with a clear design direction and production quality.

Prefer implementation over mockups unless the user explicitly asks for design-only output.

Default to Next.js unless the user requests another framework.

## Workflow

Follow these steps in order.

### Step 0: Security gate for Next.js (CVE-2025-55182)

If the project uses Next.js, verify the installed `next` version before doing implementation work.

Treat these versions as vulnerable and require upgrade first:

- `>=14.3.0-canary.77` and `<15.0.5`
- `>=15.1.0-canary.0` and `<15.1.9`
- `>=15.2.0-canary.0` and `<15.2.6`
- `>=15.3.0-canary.0` and `<15.3.6`
- `>=15.4.0-canary.0` and `<15.4.8`
- `>=15.5.0-canary.0` and `<15.5.7`
- `>=16.0.0-canary.0` and `<16.0.7`

Accept only patched versions for this CVE:

- `15.0.5`, `15.1.9`, `15.2.6`, `15.3.6`, `15.4.8`, `15.5.7` or newer patch in those lines
- `16.0.7` or newer
- `15.6.0-canary.58+` and `16.1.0-canary.12+`

`13.x` and `14.x` stable releases are not affected by this CVE.

When version status is unclear, upgrade to the latest stable Next.js release before continuing.

### Step 1: Confirm implementation brief

Collect only the critical inputs:

- Deliverable type (page, section, flow, component)
- Target devices (desktop, mobile, responsive)
- Framework and constraints (default Next.js)
- Required states and interactions
- Brand constraints (color, typography, voice)

Ask concise follow-up questions only when blocked by missing requirements.

### Step 2: Define design direction before coding

Commit to a concrete direction before writing code:

- Purpose and audience
- Tone and aesthetic
- Layout and hierarchy strategy
- Typography and color system
- Motion strategy
- Signature differentiator (one memorable element)

Load `references/design-direction.md` when creating or pressure-testing the direction.

### Step 3: Use targeted inspiration only when needed

Use 21st.dev only for specific components that benefit from references.

Do not run broad inspiration passes.

When targeted inspiration is needed:

1. Verify screenshot capture capability is available.
2. Verify web/browser search capability is available.
3. Capture only the minimum references needed.
4. Synthesize patterns instead of cloning.

If screenshot capture is unavailable, stop and tell the user:
"This workflow requires screenshot capture for targeted component inspiration. Install the screenshot skill and retry."

If web search is unavailable, stop and tell the user to restart with search enabled.

Load `references/component-inspiration.md` when this step is needed.

### Step 4: Implement in project code

Implement directly in the user's codebase:

- Reuse existing components and conventions first.
- Maintain responsive behavior and accessible states.
- Avoid generic AI-looking structure, spacing, and styling defaults.
- Keep visuals cohesive with the selected direction.

### Step 5: Validate and deliver

Before finishing:

- Run relevant lint/test/build checks for changed files.
- Verify responsive behavior and critical interaction states.
- Confirm the implementation matches the declared direction.

Load `references/validation-checklist.md` to run a final quality pass.

## Output requirements

In the final response, include:

- Chosen design direction and signature differentiator
- Which components used targeted inspiration (if any)
- Framework used (default Next.js or user override)
- Concrete files changed
- Validation status (what was run and what was not)
