---
name: ai-site-reconstruction
description: Reconstruct websites from supplied reference screenshots with staged analysis, implementation, and browser comparison.
metadata:
  short-description: Rebuild websites from reference images
---

# AI Site Reconstruction

Use this skill when implementing a website from visual references. Treat screenshots as evidence to reproduce faithfully, not inspiration for a redesign. Follow the user's project structure and conventions.

## Workflow and approval gate

Respect the requested stopping point. When the user asks to analyze first, complete Phase 1 only, present the report, then wait for explicit confirmation before coding. Do not scaffold or edit files during analysis. After approval, establish the design system and implement one module at a time. If the user authorizes multiple phases without pauses, follow that authorization.

### Phase 1 — Analyze the reference

Inspect each image at native resolution. Record viewport dimensions. Separate observable facts from estimates; note cropped, obscured, or uncertain content. Identify different breakpoints or scroll positions when multiple screenshots are supplied.

Report:

1. Page structure: header/navigation, hero, visible content sections, footer, and order.
2. Layout: viewport and content widths, column ratios, positions, alignments, and major dimensions.
3. Typography: likely family/category, sizes, weights, line heights, letter spacing, casing, and wrapping.
4. Color: backgrounds, text, brand/accent, borders, muted colors; estimate hex only when supported.
5. Spacing: section gaps, padding, margins, and whitespace proportions.
6. Images: ratios, crop/focal point, subject placement, overlays, and treatment.
7. Components: buttons, cards, navigation, icons, borders, radii.
8. Visual character: contrast, light/shadow, texture, depth, density, and focal hierarchy.

Estimate pixel sizes, mark uncertain values as ranges, and avoid false precision. Finish with key unknowns or assumptions, then wait.

### Phase 2 — Establish the design system

After approval, define max-width, grid/breakpoints, color tokens, typography roles and scale, spacing scale, radii, shadows, image ratios/crop rules, and button/card patterns. Derive them from the screenshot. Reconcile with an existing project system and explain unavoidable conflicts. Preserve the decisions in project-appropriate durable form when useful.

### Phase 3 — Implement modules

Inspect local instructions, project structure, entry points, and available assets first. Split the page into modules evidenced by the reference and preserve their order. Use reusable components and real HTML/CSS layout. Implement one module at a time, prioritizing composition, position, dimensions, and imagery. Use supplied assets; disclose material substitutions. Do not add unsupported sections or decoration.

### Phase 4 — Match visual details

Refine in priority order: P0 overall composition and geometry; P1 image source, ratio, crop, focal point; P2 font, size, line height, weight, wrapping; P3 color, spacing, radii, borders; P4 shadows, gradients, motion only when visible. Do not use effects to hide layout errors.

### Phase 5 — Browser comparison

Run the site using its normal workflow and capture a screenshot at the reference viewport size. Compare page dimensions, module placement/size, alignment, image crop, text wrapping, colors, hierarchy, and whitespace. Correct mismatches and recapture after meaningful changes. Check a mobile viewport and preserve the same visual rules while keeping the layout usable. Never claim pixel-level verification without a browser screenshot; state concrete blockers and remaining unverified items.

### Phase 6 — Deliver

Summarize files/modules changed, visual comparison performed, and remaining mismatches or asset limits.

## Fidelity constraints

- Never flatten the screenshot into a page background or pretend it is HTML content.
- Do not omit visible modules, silently replace distinctive assets, or redesign for personal taste.
- Do not add unsupported ornaments, gradients, shadows, or animation.
- Use responsive HTML/CSS and the project's component framework where appropriate.
- Where the reference cannot establish a property, state the uncertainty and choose the least speculative implementation.
