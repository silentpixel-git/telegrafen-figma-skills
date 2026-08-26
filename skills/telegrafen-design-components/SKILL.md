---
name: telegrafen-design-components-v1-3
description: Use when creating, prototyping, iterating, reviewing, repairing, or finalizing Telegrafen or Telenor components in Figma.
---

# Telegrafen component design v1.3

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

Use published production components by default. Use a beta component only when no published equivalent meets the need, the user explicitly accepts its unstable status, and the dependency is recorded in the handoff.

Resolve decisions in this order:

1. User-approved brief or mockup defines the need
2. Existing live Telegrafen components and patterns determine reuse
3. Live Telegrafen variables, styles, and icon libraries
4. User interview for anything still unresolved

If an existing component serves the same task and interaction, use it through its supported API even when the approved mockup looks different. Never create a parallel component merely to match the mockup.

If sources conflict, explain the conflict and ask the user. Do not silently choose one.

## Choose a mode

| Mode | Use when | Depth |
|---|---|---|
| **Build & Iterate** | Build, create, prototype, try, adjust, or tweak | Fast draft loop with targeted questions and checks |
| **Review & QA** | Review, audit, validate, or QA | Read-only structural and visual assessment |
| **Repair & Finalize** | Fix, repair, update, or finalize and correct | Authorised edits followed by the complete finalisation audit |

Use Build & Iterate by default. Do not apply the release-level audit to an early draft.

Review and QA are read-only. Apply changes only when the user explicitly asks to fix, repair, update, or finalize and correct the component.

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
- Intended ownership: product component or Telegrafen component candidate
- Target platform, viewport context, and input methods
- Anatomy and content model
- Sizes and states
- Component properties and variant axes
- Selection or value model
- Icon behavior
- Resizing, wrapping, and count limits
- Text growth, wrapping, truncation, and clipping behaviour
- Interaction and keyboard behavior
- Intended accessible name, role, state or value, and announcement needs
- Motion and reduced-motion behaviour
- Editable destination
- Optional prototype wiring or new canvas examples
- Publication, compatibility, migration, or deprecation impact

Accessibility is mandatory, but component-specific accessibility behavior may still require an interview.

When the user asks for best practice, research current credible guidance and use it to support a recommendation. Research does not resolve a material product decision: translate the recommendation into Telegrafen and ask the user to confirm it.

## Build & Iterate

1. Confirm the editable destination and inspect the closest approved components, tokens, text styles, and icons.
2. Run the interview gate for every material ambiguity.
3. Build a coherent draft: foundation first, then meaningful variants and properties.
4. Add prototype wiring, documentation, or canvas examples only when requested.
5. Validate the changed structure and capture a fresh screenshot.
6. Return the draft link, confirmed contract, checks performed, and the next useful iteration question.

Call the result a **draft product component** or **Telegrafen component candidate**, according to its intended ownership, until it is approved for publication. Build mode does not require exhaustive variant combinations, every responsive example, or publication-style documentation. Report every contracted state or behaviour that remains missing.

## Review, repair, and finalize

1. Reinspect the destination and complete the interview contract. Every relevant topic must be resolved or marked not applicable. For review or QA, perform the remaining steps without editing.
2. Identify the directly affected component set, nested dependencies, variants, and existing examples. Keep unrelated library components out of scope.
3. Verify component and layer names, variants, properties, defaults, nested property exposure, and interaction invariants.
4. Verify token bindings, icon linkage, control sizes, Auto Layout, resizing, wrapping, focus treatment, and supported modes.
5. Verify every state declared in the contract; mark irrelevant states not applicable. Inspect fresh screenshots covering supported sizes, realistic short and long content, icon options, and light and dark contexts where applicable.
6. Before finalisation or publication, add a concise Figma description covering purpose, when to use or avoid the component, important properties, and accessibility or interaction expectations. New canvas examples remain optional.
7. Update and QA every existing example, specimen instance, and documentation frame directly affected by the component change.
8. Report `Complete` only when the resolved contract and all required checks pass. Otherwise report `Incomplete` and name what remains.

## Telegrafen construction rules

### Components and APIs

- Reuse live Telegrafen components when they satisfy the need. Do not detach, redraw, or recreate them.
- Create a component only when it represents a repeatable structure, behaviour, or design contract. Keep one-off composition as semantically named frames unless the user explicitly intends a reusable product component.
- Do not add or override strokes, borders, drop shadows, blurs, glows, or other effects on any Telegrafen library asset or instance unless the component exposes them through a supported property or they are bound to a verified, named, live Telegrafen token or published style. A renamed local value does not qualify. If Telegrafen does not define the treatment, leave it off.
- Use variants for meaningful structural, behavioural, size, or state differences. Use text, boolean, and instance-swap properties for content and optional elements; do not create variants merely for copy, icon choice, or visibility when a property can express the difference.
- Keep variant axes independent and avoid combinations that cannot occur. Make the default instance the safest, most common usable state with representative content; do not default to destructive, disabled, error, loading, or selected states unless that state defines the component.
- Name public properties from the designer's perspective using current Telegrafen vocabulary. Prefer positive booleans such as `Show icon`, keep equivalent properties named consistently, and never expose layer or implementation terminology.
- Expose an instance-swap property only for genuinely swappable content. Restrict preferred values to semantically compatible live Telegrafen assets and name the slot by its role.
- Expose a nested property at the parent only when consumers need it and it behaves consistently across relevant variants. Keep implementation choices internal and avoid duplicate parent and child controls for the same decision.
- Do not expose internal styling choices as public properties.
- Never create or preserve a default, variant, or public property that encodes preselected consent, hidden costs, obstructed exits, false urgency, visually unequal choices, or another dark pattern. Flag the risk and propose a neutral Telegrafen alternative.
- Preserve built-in interactions on nested library instances. Add parent-level prototype behaviour only when requested and only where it does not conflict with the nested component's contract.
- Do not enable the Button property `Neutral`. In every dark-background region, inspect every nested Button and verify `Neutral = Off`.
- Use clear, purpose-based names that match existing Telegrafen conventions.

### Naming and structure

- Inspect the closest current Telegrafen component before naming. Current live patterns override the historical “How to build components” guide.
- Name new components in singular, purpose-based form using the casing and syntax shown by the current library.
- Name every custom layer by its role. Frames are appropriate for Auto Layout and resizing, but `Frame`, `Group`, or `Rectangle` describes a node type, not its purpose; never leave names such as `Frame 12` or `Rectangle 3`.
- Use this vocabulary when it fits: `Container` for the outer structure; `Top`, `Content`, `Bottom`, or `Section` for major regions; `Wrapper` only for layout; `Slot` for swappable content; `Label`, `Title`, `Subtitle`, or `Text` for copy; and `Trigger`, `Input`, `Item`, or `Option` for interaction roles. Prefer a more specific name when it is clearer.
- Keep equivalent layers named consistently across variants so overrides survive. Do not rename internal layers of an untouched library instance.
- Match current live property names, order, and variant syntax; do not impose the older fixed `Size`, `Type`, `State` order.
- Treat published property names, variants, defaults, and stable override layers as compatibility contracts. Preserve them whenever possible. A breaking change requires an impact assessment, migration plan, and explicit approval before implementation.

### Tokens and typography

- Bind semantic Telegrafen variables and published styles wherever suitable tokens exist.
- Use published Telegrafen text styles; do not approximate them with local font settings.
- A reusable component must not hard-code a page-level H1. Define its title role and typography in the component contract, and let the containing page determine its semantic heading level. If consumers genuinely need different approved title treatments, expose only contractually meaningful options through the component API; never rely on detached or local text overrides.
- Reserve `Display` for a concise, expressive page-level H1 in a Hero, banner, or similarly spacious context. Use `Title` for functional headings and section titles. Never use `Display` for H2 through H5, USP blocks, forms, labels, or compact component content, and never select it merely to make text larger.
- Do not map H1 through H5 to universal font sizes. Use only the published `Display`, `Title`, `Text`, or `Content` style that fits the contracted role and context. Preserve natural wrapping and growth; never shrink, tighten, truncate, or change semantic level merely to make text fit.
- Use live control-size tokens for interactive heights.
- Do not use primitive colors, copied values, guessed token names, or arbitrary substitutes.
- If a required semantic colour, spacing, radius, elevation, motion, or control-size token does not exist, pause and propose the missing foundation as a separate design-system decision. Never create or rename a local value to simulate a Telegrafen token.

### Icons

- Any brand-identity element must use the official Telenor brand-blue symbol asset when it is available. Never recolour it or typeset or style “Telenor” to imitate a logo or wordmark. If contrast is insufficient, change the surrounding surface or placement. If the symbol cannot be found, interview the user; do not substitute text. Ordinary content may still use the word Telenor.
- Reserve the main Telenor brand colour for the official logo or symbol. Do not use it on non-logo elements unless a current, explicit, approved Telegrafen or Telenor brand rule requires it for that exact element. Use the appropriate semantic Telegrafen colour token for every other role.
- Use live instances from the appropriate UI Icons, Product Icons, or Illustrative Icons library.
- Commit each repeated peer-artwork role to one non-UI icon family before selecting individual icons. Equivalent peers and their examples must never mix Product Icons and Illustrative Icons, even when every asset is individually relevant, visually related, or present in a reference.
- A public instance-swap slot for peer artwork must use preferred values from one non-UI family and a structure sized for that family. Do not use one slot or variant set to normalize Product and Illustrative Icons into interchangeable peer artwork. Different families belong in separate roles or component contracts only when their semantic purposes genuinely differ.
- Within a peer set, use the same supported instance size, container footprint, alignment, and colour rule. Preserve natural differences in approved artwork; never modify an icon to force identical visual weight.
- If one family does not cover the complete peer set, choose another family that does, separate the content only when it has genuinely different roles or contracts, remove the icon property from the entire peer set when icons are non-essential, or ask and report `BLOCKED` when icons are essential. Never fill a coverage gap with the other non-UI family.
- A UI Icon may coexist with Product or Illustrative artwork only through a clearly separate action, navigation, or status role supplied by a supported slot or nested component. It does not permit Product and Illustrative Icons to mix as peer artwork.
- At 32 px or smaller, use UI Icons only. Above 32 px, continue to choose the family by semantic meaning; size alone never turns a UI Icon into a Product or Illustrative Icon.
- Never display an Illustrative Icon below a 120 × 120 px instance frame.
- Choose icons by semantic meaning. **Never change an icon's aspect ratio:** scale width and height together and use a wrapper or container when a different footprint is needed.
- Use a supported icon size when available; do not preserve the ratio at an arbitrary size merely to make it fit.
- Keep every icon's `Default` library colour by default. A designer may explicitly define another colour for a complete section before application, but it must use a verified semantic Telegrafen token or supported component property, apply consistently to equivalent icons, pass contrast in its light or dark context, and never use the logo-reserved main brand colour. One-off recolouring remains prohibited unless a verified semantic state requires it.
- Never redraw, stretch, crop, generate, or substitute an icon.
- If no suitable icon can be verified, interview the user instead of approximating one.

### Content and media

- Use representative Norwegian Bokmål content and the Telegrafen UX Writing skill when available. Do not use lorem ipsum or invent commercial facts. Test realistic short and long content while keeping copy secondary to the component contract.
- Keep editorial imagery swappable and outside the component's structural identity unless an approved asset is intrinsic to the component. Use only user-provided or approved Telenor imagery in examples; never package generated or third-party lookalikes as defaults.
- Keep every approved image source intact. Do not apply local strokes, borders, shadows, blurs, glows, recolouring, distortion, or other effects to the image itself. An approved presentation frame may crop the visible view without altering the source asset; any wrapper treatment must use a verified Telegrafen token, published style, or supported component property.

### Lists, cards, and repeated content

- Every rendered list item must contain meaningful primary content. Never add blank, invisible, placeholder, or whitespace-only items to create spacing, fill a grid, balance columns, or equalize container heights.
- Omit unavailable items. Use the approved Telegrafen Skeleton pattern for loading and an appropriate empty state for a genuinely empty result; never represent either with an empty List instance.
- Optional fields inside a valid item may be absent only when the component supports that state.
- Default a repeated static icon–title–description benefit contract to an open item or list pattern, not a Card. Create or preserve a Card contract only when the boundary communicates independent content, interaction, selection, state, comparison, or another distinct containment purpose.
- Treat a containing section surface as existing group containment. Nested child cards require a second, distinct purpose. Before adding a second consecutive card-led specimen or example section, review the page for cardification and flatten at least one set unless the task genuinely requires repeated independent or comparable modules; do not impose a universal numeric cap.
- Cards with the same purpose must use the same verified Telegrafen component and variant. Use different variants only when function, hierarchy, interaction, or state differs, and use supported light- or dark-mode treatments rather than style overrides.
- An interactive Card contract must define the supported action and visible states. A static Card contract must not imitate interaction through unsupported hover treatments, action chevrons, cursor cues, or elevation. Do not expose nested competing actions unless the verified component contract supports them.
- Peer card instances in the same row, comparison set, or specimen should use consistent widths and visually aligned heights when they represent equivalent choices. Align equivalent internal regions when this improves scanning.
- Achieve alignment with Auto Layout, shared structure, consistent padding, and supported fill or hug behaviour. Never use empty items, invisible filler, fake copy, clipping, or truncation to equalize cards.
- Cards with different purposes or hierarchy do not need matching dimensions. When realistic content varies too much for sound equal-height treatment, revise the layout or allow natural height.

### Layout, modes, and accessibility

- Define fixed, hug, and fill behavior, wrapping, minimum sizes, and nested-instance sizing where supported.
- Define growth, wrapping, truncation, and clipping behaviour for every variable-content region. Prefer growth or wrapping. Use truncation only when an established Telegrafen pattern supports it and the full content remains available through an agreed accessible method. Never allow accidental clipping.
- Use semantic variables for light and dark modes rather than mode-specific visual overrides.
- Treat every dark-background region as a dark-mode context, even inside a light component or screen. Verify all nested surfaces, text, icons, the Telenor symbol, dividers, borders, focus indicators, overlays, and hover, active, selected, disabled, loading, and error states.
- Provide visible focus without layout movement, sufficient contrast and target size, semantic disabled behavior, and the agreed keyboard and selection behavior.
- For interactive components, record the intended accessible name, role, state or value, focus order, keyboard behaviour, and announcement needs in the contract and handoff. Treat these as implementation requirements; Figma cannot prove implementation semantics.
- Treat target platform, viewport context, and input methods as material decisions. Do not infer desktop, touch, mouse, or keyboard behaviour from appearance alone.
- Add motion only when requested or established by a live Telegrafen pattern. Use verified motion tokens, define the transition and interruption behaviour, and document a reduced-motion alternative when the motion is not essential.

## Editing and lifecycle safety

- Work only in the user-supplied branch, staging page, or explicitly designated editable area. Never modify a published master component in place unless the user identifies it as the target and confirms the change scope.
- Label new work as a draft product component or Telegrafen component candidate according to its intended ownership. Never present it as an official Telegrafen component until it has passed final review and been approved for publication.
- Deprecate rather than delete by default. Identify the replacement, preserve the old component during migration, and remove it only with explicit approval after usage and migration impact are understood.
- Never publish, replace, deprecate, delete, or perform another library-wide lifecycle action without explicit confirmation immediately before the action. First report the exact components, changed properties or variants, migration impact, and unresolved risks.

## WCAG delivery gate

Before every handoff, inspect fresh screenshots of every changed component, affected example, and visible state at the supported sizes in scope. Check clipping, overlap, gaps, off-canvas elements, peer icon-family commitment and slot consistency, component and token provenance, unapproved effects, empty list items, dark-mode treatment, card-contract purpose, redundant containment, consecutive cardification, static or interactive affordance, repeated-card alignment, typography, and contrast. Fix clear in-scope defects and reinspect; a draft may report unfinished defects, but it must name them.

Before every delivery, run a [WCAG 2.2](https://www.w3.org/TR/WCAG22/) Level AA design review on every visible mode and state in scope:

- Normal text has at least 4.5:1 contrast; WCAG large text has at least 3:1.
- UI components, meaningful graphics, and state indicators have at least 3:1 contrast against adjacent colors.
- Keyboard focus is visible and is not obscured.
- Pointer targets are at least 24 × 24 CSS px unless a documented WCAG exception applies.
- Labels, status, and meaning do not depend on color alone; the agreed keyboard and interaction behavior is represented where Figma can show it.

Run the review separately for every supported light and dark context. A Figma review validates design evidence only; it cannot prove implementation semantics or full product conformance.

Never omit the results from the handoff. State `Visual QA: PASS`, `NEEDS CHANGES`, or `BLOCKED`, followed by `WCAG 2.2 AA design review: PASS`, `NEEDS CHANGES`, or `BLOCKED`, the modes and states checked, failures or exceptions, and implementation-only items that could not be verified.

Never pass structural QA from screenshots alone. If component properties, variants, layer structure, metadata, or variable bindings cannot be inspected, report `Structure and API: BLOCKED` and state what access or evidence is missing.

Build & Iterate may hand over a transparent draft with `NEEDS CHANGES`, but never without the result. Repair & Finalize may report `Complete` only when the WCAG design review passes.

## Never re-skin another library

External references may clarify a user need, but do not copy the anatomy, styling, API, or interaction model of Material, MUI, Ant, Bootstrap, Radix, shadcn, Chakra, or another design system.

Research and external references may inform a recommendation, but they never override the live Telegrafen library or resolve a material component decision without user confirmation.

## Common mistakes

| Mistake | Required response |
|---|---|
| Behavior is unclear, so a sensible default is chosen | Stop and interview the user |
| A draft is used to justify assumptions | A draft may be incomplete, never invented |
| Review or QA is treated as permission to edit | Report findings only until fixes are explicitly requested |
| An available component or icon is recreated | Replace it with the live library instance |
| A beta component is used as a convenient shortcut | Return to production assets or obtain explicit beta approval |
| A library instance is made “better” with a local border or shadow | Remove it unless it is a supported property or named Telegrafen token/style |
| A dark-mode Button uses `Neutral` | Turn `Neutral` off and recheck the state |
| WCAG is assumed from token use | Test the rendered design and record the result in the handoff |
| Variants or properties mirror internal layers | Expose only meaningful consumer choices through the correct property type |
| A published API is renamed for neatness | Preserve it or obtain approval for a migration plan |
| A final component omits a contracted state | Mark it incomplete and name the missing state |
| Screenshots look correct but metadata cannot be inspected | Report `Structure and API: BLOCKED` |
| A component is published as the final workflow step | Stop and obtain explicit publication confirmation |
| Full finalization audit slows the first draft | Return to Build & Iterate checks |
| The component looks correct but metadata disagrees | Treat validation as failed and diagnose the mismatch |

## Handoff

For Build & Iterate, report:

- Draft node link
- Confirmed component contract
- Components, variants, and properties created or changed
- Telegrafen libraries and token families used
- Targeted checks performed
- `Visual QA: PASS`, `NEEDS CHANGES`, or `BLOCKED`
- `WCAG 2.2 AA design review: PASS`, `NEEDS CHANGES`, or `BLOCKED`, including modes and states checked, exceptions or failures, and implementation-only items not verified
- Remaining questions, if any

For Review & QA or Repair & Finalize, report separately:

- `Structure and API: PASS`, `NEEDS CHANGES`, or `BLOCKED`
- `Visual QA: PASS`, `NEEDS CHANGES`, or `BLOCKED`
- `WCAG 2.2 AA design review: PASS`, `NEEDS CHANGES`, or `BLOCKED`
- `Overall: Complete`, `Incomplete`, or `BLOCKED`

Overall is `Complete` only when all required reviews pass. Include the final node link, contract coverage, affected dependencies and examples, compatibility or migration impact, implementation-only accessibility requirements, and unresolved limitations.
