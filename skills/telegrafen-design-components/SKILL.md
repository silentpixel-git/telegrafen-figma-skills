---
name: telegrafen-design-components-v1
description: Use when creating, prototyping, iterating, reviewing, repairing, or finalizing Telegrafen or Telenor components in Figma.
---

# Telegrafen component design

## Core principle

Build useful drafts quickly, but never invent unresolved component decisions. Inspect the design system first; interview the user whenever anything material remains unclear.

Keep all work in Figma. Do not create or modify Vue, Storybook, Code Connect, or other implementation code unless the user explicitly requests a separate implementation task.

## Source of truth

Use the live, published Telegrafen sources:

- [Components](https://www.figma.com/design/80yLUPif6wgDwXLu5MbMFj/)
- [Beta Components](https://www.figma.com/design/DxIUwsPdqIhyCMOTC3v2iW/)
- [Design Tokens](https://www.figma.com/design/aW7bFTLqx5L0XTWMskOHSR/)
- [UI Icons](https://www.figma.com/design/tgJeQElYu5kOzdP3VxVsky/)
- [Product Icons](https://www.figma.com/design/iWy3sNQXCzr2XIBZUGJnAp/)
- [Illustrative Icons](https://www.figma.com/design/8pTia61uly3XAkmZfOSUYt/)

Components and Beta Components are protected, read-only references. Require a user-supplied editable page or frame before writing.

Resolve decisions in this order:

1. User-approved brief or mockup
2. Existing live Telegrafen components and patterns
3. Live Telegrafen variables, styles, and icon libraries
4. User interview for anything still unresolved

If sources conflict, explain the conflict and ask the user. Do not silently choose one.

## Choose a mode

| Mode | Use when | Depth |
|---|---|---|
| **Build & Iterate** | Build, create, prototype, try, adjust, or tweak | Fast draft loop with targeted questions and checks |
| **Review & Finalize** | Review, validate, finalize, publish, QA, or the design is ready | Complete contract and thorough structural and visual audit |

Use Build & Iterate by default. Do not apply the release-level audit to an early draft.

## Interview gate: no guesses

Anything that can change the component's purpose, anatomy, content, behavior, states, accessibility, consumer API, or deliverables is a product decision. Every unresolved product decision requires a user answer before the affected design is built.

Before the first affected write:

1. Inspect the editable target and the closest approved Telegrafen components.
2. Mark each relevant decision as resolved, unresolved, or not applicable.
3. Ask one focused question about the highest-impact unresolved decision.
4. Wait for the answer, update the contract, and ask the next question.
5. When all material decisions are resolved, summarize the agreed contract and ask the user to confirm the shared understanding. Continue the interview if anything remains unclear; proceed only after confirmation.

A decision is resolved only by:

- An explicit user answer
- An approved brief or mockup
- Clear evidence from an existing Telegrafen component or established pattern that directly applies

The following do **not** resolve a decision:

- A common industry pattern
- A pattern from another design system
- Visual intuition or a “reasonable default”
- Time pressure or an unavailable stakeholder
- A general request to “use your judgement”

When the user is unavailable, continue inspection and other non-committal work, but stop before designing anything affected by an unresolved decision. Never hide a guess by calling it a draft, assumption, recommendation, or best practice.

Interview only what is unclear. Do not repeat questions already resolved by the brief, inspection, or prior answers, and do not send a large questionnaire at once.

Check these topics when relevant:

- Purpose and usage
- Anatomy and content model
- Sizes and states
- Component properties and variant axes
- Selection or value model
- Icon behavior
- Resizing, wrapping, and count limits
- Interaction and keyboard behavior
- Editable destination
- Optional prototype wiring, documentation, or canvas examples

Accessibility is mandatory, but component-specific accessibility behavior may still require an interview.

## Build & Iterate

1. Confirm the editable destination and inspect the closest approved components, tokens, text styles, and icons.
2. Run the interview gate for every material ambiguity.
3. Build a coherent draft: foundation first, then meaningful variants and properties.
4. Add prototype wiring, documentation, or canvas examples only when requested.
5. Validate the changed structure and capture a fresh screenshot.
6. Return the draft link, confirmed contract, checks performed, and the next useful iteration question.

Call the result a **draft** until the user says it is ready. Build mode does not require exhaustive variant combinations, every responsive example, or publication-style documentation.

## Review & Finalize

1. Reinspect the destination and complete the interview contract. Every relevant topic must be resolved or marked not applicable.
2. Ask before adding unrequested extras: “Do you want prototype wiring, Figma documentation, or canvas validation examples included?”
3. Verify component and layer names, variants, properties, defaults, nested property exposure, and interaction invariants.
4. Verify token bindings, icon linkage, control sizes, Auto Layout, resizing, wrapping, focus treatment, and supported modes.
5. Inspect fresh screenshots covering supported sizes, representative states, long content, icon options, and light/dark modes where applicable.
6. Report `Complete` only when the resolved contract and all required checks pass. Otherwise report `Incomplete` and name what remains.

## Telegrafen construction rules

### Components and APIs

- Reuse live Telegrafen components when they satisfy the need. Do not detach, redraw, or recreate them.
- Do not add or override strokes, borders, drop shadows, blurs, glows, or other effects on any Telegrafen library asset or instance unless the component exposes them through a supported property or they are bound to a verified, named, live Telegrafen token or published style. A renamed local value does not qualify. If Telegrafen does not define the treatment, leave it off.
- Expose meaningful consumer choices through intentional text, boolean, instance-swap, and variant properties.
- Keep variant axes independent and avoid combinations that cannot occur.
- Do not expose internal styling choices as public properties.
- Do not enable the Button property `Neutral`. In dark mode, inspect every nested Button and verify `Neutral = Off`.
- Use clear, purpose-based names that match existing Telegrafen conventions.

### Naming and structure

- Inspect the closest current Telegrafen component before naming. Current live patterns override the historical “How to build components” guide.
- Name new components in singular, purpose-based form using the casing and syntax shown by the current library.
- Name every custom layer by its role. Frames are appropriate for Auto Layout and resizing, but `Frame`, `Group`, or `Rectangle` describes a node type, not its purpose; never leave names such as `Frame 12` or `Rectangle 3`.
- Use this vocabulary when it fits: `Container` for the outer structure; `Top`, `Content`, `Bottom`, or `Section` for major regions; `Wrapper` only for layout; `Slot` for swappable content; `Label`, `Title`, `Subtitle`, or `Text` for copy; and `Trigger`, `Input`, `Item`, or `Option` for interaction roles. Prefer a more specific name when it is clearer.
- Keep equivalent layers named consistently across variants so overrides survive. Do not rename internal layers of an untouched library instance.
- Match current live property names, order, and variant syntax; do not impose the older fixed `Size`, `Type`, `State` order.

### Tokens and typography

- Bind semantic Telegrafen variables and published styles wherever suitable tokens exist.
- Use published Telegrafen text styles; do not approximate them with local font settings.
- Reserve the `Display` typography style for major page-level headlines, such as an H1 in a Hero component. Never use `Display` for section headings, USP blocks, forms, labels, or other compact content; use the appropriate published heading or UI text style instead.
- Use live control-size tokens for interactive heights.
- Do not use primitive colors, copied values, guessed token names, or arbitrary substitutes.

### Icons

- Any brand-identity element must use the official Telenor symbol asset when it is available. Never typeset or style “Telenor” to imitate a logo or wordmark. If the symbol cannot be found, interview the user; do not substitute text. Ordinary content may still use the word Telenor.
- Use live instances from the appropriate UI Icons, Product Icons, or Illustrative Icons library.
- Choose icons by semantic meaning. **Never change an icon's aspect ratio:** scale width and height together and use a wrapper or container when a different footprint is needed.
- Use a supported icon size when available; do not preserve the ratio at an arbitrary size merely to make it fit.
- Never redraw, stretch, crop, generate, or substitute an icon.
- If no suitable icon can be verified, interview the user instead of approximating one.

### Layout, modes, and accessibility

- Define fixed, hug, and fill behavior, wrapping, minimum sizes, and nested-instance sizing where supported.
- Use semantic variables for light and dark modes rather than mode-specific visual overrides.
- In dark mode, verify that all text, icons, the Telenor symbol, dividers, borders, focus indicators, overlays, and hover, active, selected, and disabled states remain visible and distinguishable.
- Provide visible focus without layout movement, sufficient contrast and target size, semantic disabled behavior, and the agreed keyboard and selection behavior.

## WCAG delivery gate

Before every delivery, run a [WCAG 2.2](https://www.w3.org/TR/WCAG22/) Level AA design review on every visible mode and state in scope:

- Normal text has at least 4.5:1 contrast; WCAG large text has at least 3:1.
- UI components, meaningful graphics, and state indicators have at least 3:1 contrast against adjacent colors.
- Keyboard focus is visible and is not obscured.
- Pointer targets are at least 24 × 24 CSS px unless a documented WCAG exception applies.
- Labels, status, and meaning do not depend on color alone; the agreed keyboard and interaction behavior is represented where Figma can show it.

Run the review separately for light and dark modes. A Figma review validates design evidence only; it cannot prove implementation semantics or full product conformance.

Never omit the result from the handoff. State `WCAG 2.2 AA design review: PASS`, `NEEDS CHANGES`, or `BLOCKED`, followed by the modes and states checked, failures or exceptions, and implementation-only items that could not be verified.

Build & Iterate may hand over a transparent draft with `NEEDS CHANGES`, but never without the result. Review & Finalize may report `Complete` only when the WCAG design review passes.

## Never re-skin another library

External references may clarify a user need, but do not copy the anatomy, styling, API, or interaction model of Material, MUI, Ant, Bootstrap, Radix, shadcn, Chakra, or another design system.

## Common mistakes

| Mistake | Required response |
|---|---|
| Behavior is unclear, so a sensible default is chosen | Stop and interview the user |
| A draft is used to justify assumptions | A draft may be incomplete, never invented |
| An available component or icon is recreated | Replace it with the live library instance |
| A library instance is made “better” with a local border or shadow | Remove it unless it is a supported property or named Telegrafen token/style |
| A dark-mode Button uses `Neutral` | Turn `Neutral` off and recheck the state |
| WCAG is assumed from token use | Test the rendered design and record the result in the handoff |
| Component properties mirror internal layers | Expose only meaningful consumer choices |
| Full finalization audit slows the first draft | Return to Build & Iterate checks |
| The component looks correct but metadata disagrees | Treat validation as failed and diagnose the mismatch |

## Handoff

For Build & Iterate, report:

- Draft node link
- Confirmed component contract
- Components, variants, and properties created or changed
- Telegrafen libraries and token families used
- Targeted checks performed
- `WCAG 2.2 AA design review: PASS`, `NEEDS CHANGES`, or `BLOCKED`, including modes and states checked, exceptions or failures, and implementation-only items not verified
- Remaining questions, if any

For Review & Finalize, lead with `Complete` or `Incomplete`, then report the final node link, contract coverage, structural and visual verification, the required WCAG 2.2 AA design-review result, and any unresolved limitations.
