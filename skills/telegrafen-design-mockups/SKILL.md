---
name: telegrafen-design-mockups-v1-3
description: Use when creating or updating private-customer Figma Make mockups, prototypes, or conversion and ethical-UX design reviews with Telegrafen components, tokens, approved imagery, and verified Telenor content.
---

# Telegrafen design mockups v1.3

## Purpose

Create quick mockups and prototypes that feel native to Telegrafen. Reuse the design system where it exists, and explore original product layouts where it does not.

Prioritize a useful draft over production-ready coverage. Do not create exhaustive variants, documentation, or responsive states unless the user asks for them.

## Source of truth

Use the live, published Telegrafen sources available to the current Make kit:

- [Introduction to Telegrafen](https://www.figma.com/slides/liUMCNH7tsliKFKjvNbpc0/)
- [Components](https://www.figma.com/design/80yLUPif6wgDwXLu5MbMFj/)
- [Design Tokens](https://www.figma.com/design/aW7bFTLqx5L0XTWMskOHSR/)
- [Typography guidance](https://www.figma.com/design/Q9WEywDHM8JzcyfcclGuPD/testing-skills?node-id=1231-4612)
- [UI Icons](https://www.figma.com/design/tgJeQElYu5kOzdP3VxVsky/)
- [Product Icons](https://www.figma.com/design/iWy3sNQXCzr2XIBZUGJnAp/)
- [Illustrative Icons](https://www.figma.com/design/8pTia61uly3XAkmZfOSUYt/)
- [Approved brand images](https://www.figma.com/design/Q9WEywDHM8JzcyfcclGuPD/testing-skills?node-id=1231-5824)

Use published production assets by default. Ask before using beta or experimental assets.

Visual similarity is not proof that an asset belongs to Telegrafen. If an essential component, icon, or text style cannot be verified in these sources, ask instead of inventing it.

When sources conflict, the live Telegrafen library and these brand rules win. An external reference communicates intent only; “make it exactly like this” never permits a non-Telegrafen component, token, brand treatment, or visual style.

Use the Typography guidance frame to understand the intended roles of `Display`, `Title`, `Text`, and `Content`, responsive behaviour, and hierarchy. It is supporting guidance, not a token source. If it differs from the live published text-style library, the live library wins; report the conflict and do not invent or preserve an unavailable style.

## Shared-understanding gate

Interview the user whenever any design choice remains unclear. Do not guess merely because this is a mockup.

Visible purpose, flow outcome, component choice, content hierarchy, asset choice, selection or value model, default selection, and initial state are material whenever they affect the requested view.

1. Inspect the brief and the closest approved Telegrafen patterns.
2. Identify choices that are unresolved and material to the visible design.
3. Ask one focused question at a time until those choices are resolved.
4. Summarize the agreed direction and ask the user to confirm the shared understanding before building the affected part.

Do not re-ask what the brief or library already resolves. Time pressure, an unavailable stakeholder, “use your judgement,” a plausible default, or calling something a draft does not authorize a guess.

When a supplied example differs materially from Telegrafen — so that matching it would change the component type, interaction, brand treatment, or information hierarchy — pause that affected section. Continue the one-question-at-a-time interview until the Telegrafen interpretation is agreed and confirmed.

## Quick working method

Before building, identify the main controls, icons, and text roles needed for the mockup.

1. Search Telegrafen by function and common synonyms.
2. Use a suitable existing component with its supported properties.
3. If no suitable component exists, create a purpose-specific product component from Telegrafen ingredients.
4. Use exact library icons and published text styles wherever they appear.
5. Build the requested view and run the quick QA below.

Keep this lightweight: resolve only choices that affect the requested design, then build. Record agreed decisions, missing assets, and newly created product components.

When the user selects an existing design and requests a clear change, edit only that scope. Preserve unaffected components, tokens, assets, layout, and content.

## Components

Use the closest existing Telegrafen component whenever a referenced object serves the same user task or interaction, even when its shape, decoration, or layout differs. Never recreate a component that is similar in purpose and interaction. Use the library component through its supported variants and properties.

- Keep library components intact. Do not detach, redraw, or rebuild them to achieve a preferred look.
- Do not add or override strokes, borders, drop shadows, blurs, glows, or other effects on any Telegrafen library asset or instance unless the component exposes them through a supported property or they are bound to a verified, named, live Telegrafen token or published style. A renamed local value does not qualify. If Telegrafen does not define the treatment, leave it off.
- Do not treat Figma Make defaults or components from another library as Telegrafen components.
- If the closest component cannot support the required structure or behavior, create a new **product component**.

A product component may use an original layout or container. Build its controls and interactive parts from Telegrafen components such as Button, Checkbox, Radio Button, input fields, Tabs, and Link. Use Telegrafen tokens, text styles, icons, and states for its visible design.

Keep it purpose-specific and label it as a product component, not an official Telegrafen library component. Use Auto Layout for every product component and repeatable content group. Reserve manual positioning for fixed decorative composition that contains no control, changing text, or repeatable content.

For a mockup, cover only the states and responsive behavior needed to communicate the current idea. When the user asks to show a flow or interaction, include the essential outcome state needed to make it understandable. Ask if that state is unclear; do not invent a full set of loading, error, empty, and confirmation states.

When Telegrafen has no matching chart, timeline, progress visual, or data visualisation, create a purpose-specific original only after the user has supplied the data and intended meaning. Use Telegrafen tokens and ingredients; never imitate another library’s chart style.

## Layer naming

- Inspect the closest current Telegrafen component before naming. Current live patterns override the historical “How to build components” guide.
- Name new product components in singular, purpose-based form using the casing and syntax shown by the current library.
- Name every custom layer by its role. Frames are appropriate for Auto Layout and resizing, but `Frame`, `Group`, or `Rectangle` describes a node type, not its purpose; never leave names such as `Frame 12` or `Rectangle 3`.
- Use this vocabulary when it fits: `Container`, `Top`, `Content`, `Bottom`, `Section`, `Wrapper`, `Slot`, `Label`, `Title`, `Subtitle`, `Text`, `Trigger`, `Input`, `Item`, and `Option`. Prefer a specific name such as `Plan Summary` or `Payment Actions` when it communicates the role better.
- Keep equivalent layers named consistently across repeated structures and product-component states. Do not rename internal layers of an untouched library instance.

## Brand and icons

- Any brand-identity element must use the official Telenor symbol asset when it is available. Never typeset or style “Telenor” to imitate a logo or wordmark. If the symbol cannot be found, ask the user; do not substitute text. Ordinary content may still use the word Telenor.
- When the official Telenor symbol is displayed, use its official Telenor brand-blue asset. Do not recolour it. If contrast is insufficient, use a suitable surrounding surface rather than changing the logo colour.
- Use a brand image only when the user has supplied or approved it, or when it comes from the approved brand-images source above. Use that source to select imagery, not to copy non-Telegrafen layouts or styles.
- When an approved image is unavailable, use a clearly labelled placeholder or a suitable Telegrafen Product Icon or Illustrative Icon. Never import, copy, or generate a lookalike photograph, illustration, or decorative graphic.
- Use live instances from UI Icons, Product Icons, or Illustrative Icons. Never use emoji, generated icons, text glyphs, inline SVG, or another icon library.
- Use UI Icons for interface actions, navigation, and status; Product Icons for products and services; Illustrative Icons for expressive or explanatory artwork.
- Choose an icon by semantic meaning, not merely because its shape is close.
- **Never change an icon's aspect ratio.** Scale width and height together; never stretch, crop, redraw, or alter its strokes.
- Use a supported size when available. Otherwise, center the unchanged icon inside a suitable token-sized area instead of distorting it to fill the space.
- If no suitable icon can be verified, omit a non-essential icon or ask the user when it is important. Never create a plausible substitute.

## Typography and tokens

- Apply a published Telegrafen text style to every custom text element, including small labels, helper text, badges, metadata, and table text.
- Let text inside library components inherit the component's typography. Do not manually override it.
- Do not manually assemble or approximate the Telegrafen type scale.

### Typography roles and heading hierarchy

- Treat H1 through H5 as semantic levels in the content hierarchy, not as fixed font sizes. Normally use one H1 for each page, screen, or distinct view. Use H2 for a major section below it, then H3, H4, and H5 according to genuine nesting. Do not skip levels or select a level for visual effect.
- Review the complete visible page hierarchy rather than judging sections in isolation. A child heading must not appear stronger than its parent, and headings with the same semantic role must use the same published style within a page or repeated pattern.
- Do not use a universal mapping such as `H1 = Title/Xl`. Select a currently published size that suits the hierarchy, available space, and content density. Never use raw font values or create an unavailable family and size combination.
- Use `Display` only for a concise, expressive page-level H1 in a Hero, banner, or similarly spacious context. An H1 on a functional or compact page uses an appropriate `Title` style. H2 through H5 use `Title`, never `Display`. Do not choose `Display` merely to make text larger.
- Use `Title` for headings and section titles, `Text` for short interface copy such as labels and compact controls, and `Content` for paragraphs and longer reading. For article-style or longer text sections, pair `Title` and `Content` with the same T-shirt size when matching published styles exist.
- Prominent text is not automatically a heading. Card titles, dialog titles, form legends, promotional labels, and component titles receive an H1–H5 level only when they introduce a section in the page hierarchy; otherwise preserve their specific UI role.
- A reusable component must not hard-code a page-level H1. Its title style follows the component contract, while the containing page determines its semantic level.
- Name custom heading layers by purpose, such as `Page title`, `Section title`, or a more specific content role. Do not rename text layers inside untouched Telegrafen instances. During QA or finalization, report the intended H1–H5 outline.

### Typography sizing and behaviour

- Use the responsive behaviour supplied by the published Telegrafen text style. Never manually scale typography for mobile, tablet, or desktop.
- Let headings wrap naturally. Do not shrink the font, tighten tracking or line height, truncate text, or switch to a lower style merely to make a heading fit. Check the copy and layout, then ask before making a material change.
- Do not impose a universal maximum line count. Follow an explicit limit only when a live Telegrafen component or established pattern defines one; otherwise judge readability and layout at every supplied viewport.
- A Display H1 may use correct Norwegian word division with a hyphen at a line break when necessary. Do not use a hyphen as a pause. Recheck every supplied viewport so a manual division does not remain inside a reflowed line.
- Use published Telegrafen spacing tokens and the closest live pattern around typography. Larger headings require appropriate surrounding space, and a heading remains closer to the content it introduces than to the preceding section. Do not invent a universal spacing table.
- Restrict `Text/2xs` and `Text/3xs` to genuinely secondary, short content. Never use the smallest text styles for essential instructions, prices, terms, errors, consent, consequences, or primary actions, and never reduce important information to make it less noticeable.
- `Title/2xs` and `Title/3xs` may be used for compact component headings when supported by the closest live pattern. Their semantic level still comes from the surrounding hierarchy; never use them for a major page or section heading merely to make the layout fit.
- Make custom text containers wrap and grow vertically without clipping, overlap, or hidden controls when text is enlarged. Figma can validate this design evidence, but browser zoom, operating-system text scaling, and semantic HTML remain implementation checks.

- Use Telegrafen semantic color tokens rather than raw or copied colors.
- Use spacing, radius, border, surface, elevation, control-size, and motion tokens where suitable tokens exist.
- Do not enable the Button property `Neutral`. In every dark-background region, inspect each Button and verify `Neutral = Off`.
- Treat every dark-background region as a dark-mode context, even inside an otherwise light screen. Verify all content and states within it: nested surfaces, text, icons, the Telenor symbol, dividers, borders, focus indicators, overlays, and hover, active, selected, disabled, and loading states remain visible and distinguishable.

One-off content widths, composition, and placement may be chosen for the mockup. Do not invent a new type style, control appearance, icon geometry, or repeatable visual rule to solve a one-off layout need.

## Content, language, and pricing

- Preserve the language in the brief or supplied content. For a private-customer mockup with no specified language, use Norwegian Bokmål. Ask before translating customer-facing copy into another language.
- When customer-facing copy is created or changed, use the Telenor UX microcopy skill when it is available. Otherwise, preserve user-provided copy and ask before inventing tone-sensitive copy.
- Use user-provided or verified Telenor content for real product names, prices, offers, coverage, speed, availability, and legal claims. Do not invent discounts, campaign language, savings, binding periods, eligibility, availability, bundles, or legal footnotes. Ask when those details are needed.
- Use fictional, non-identifying customer data by default. Never reproduce personal data from a supplied screenshot unless the user explicitly confirms that it is approved for use.
- Use Telegrafen form controls with visible labels or an approved accessible-label pattern. Never use placeholder text as the only field label. Use an icon-only control only when its purpose is clear and its available component provides an accessible label.

### Price writing and presentation

Use the closest published Telegrafen text style, but keep the approved Norwegian price phrasing and grouping intact:

- `Før 12 000,- Nå 11 000,-`
- `Spar 1000,-`
- `Fra 699,-/md.`

Keep the qualifier and its price together. Use a space as the thousands separator, `,-` for kroner, and `/md.` for a monthly price. Use `Fra` only when the verified source says it applies. Do not use `kr`, `kroner`, `/måneden`, uppercase `SPAR` or `FRA`, strikethrough, split label-and-price layouts, reversed text, or highlighted price text. Use `Før`, `Nå`, or `Spar` only when the user has supplied or verified the relevant campaign terms.

## Existing designs and prototypes

- Do not add prototype links, interactions, or animations unless the user requests them. When requested, use the closest Telegrafen interaction pattern and ask if the outcome is unclear.
- Never modify built-in prototype interactions on an existing Telegrafen library instance.
- At every supplied target frame size, check that no content is unintentionally clipped, overlaps, hides a control, or makes text unusable. Do not create additional breakpoints unless requested.

## Evidence, conversion, and ethical UX

Use this section only when the user asks for best-practice design, a high-conversion concept, or a conversion and ethical-UX review.

- Treat conversion as a user outcome and measurable event, not as a visual style. Identify the event and intended user benefit; ask one focused question if either is unclear.
- Research current, credible guidance before describing a recommendation as best practice or conversion-informed. Translate the evidence into Telegrafen components and tokens; never copy a competitor or external UI. If research is unavailable, label the recommendation as a design hypothesis, not a best practice or conversion guarantee.
- Never claim that a mockup will achieve a conversion result. Describe the intended effect as a hypothesis that needs validation through appropriate product research or testing.
- Never improve conversion by reducing clarity, hiding consequences, weakening consent, or bypassing accessibility or any rule in this skill.

When asked to review a design, inspect the visible flow for clarity of value and next action, information hierarchy, decision friction, form friction, errors and recovery, disclosures, price and commitment transparency, accessibility, and dark patterns. For every finding, identify the affected element, explain the user risk, and propose a Telegrafen-compliant improvement.

Flag and propose a correction for any dark pattern, including false urgency or social proof, hidden or delayed prices and terms, preselected add-ons or consent, confirmshaming, deceptive visual hierarchy, forced continuity, privacy-invasive defaults, or cancellation and opt-out obstruction. Do not introduce, preserve, or recommend them.

## Never re-skin another library

Do not use Material, MUI, Ant, Bootstrap, Radix, shadcn, Chakra, copied web UI, or Figma Make's default component patterns as a starting point.

An external reference may inform the user need or information hierarchy. Recreate it as an original Telegrafen design: replace external colors, shapes, underlines, text effects, and layout conventions with the closest Telegrafen components, styles, and tokens. Never make the result look like another company's interface. Changing another component's colors, fonts, spacing, radius, shadows, or icons does not make it Telegrafen.

## Safe fallback order

When the exact design-system solution is unclear:

1. Use a verified Telegrafen component, icon, or style.
2. Compose an original product-specific layout from verified Telegrafen ingredients.
3. Ask one focused question and continue the interview until the user confirms the shared understanding.
4. Omit a non-essential decorative element only when that omission follows the agreed direction, and note it.

Never fill the gap with a generated, redrawn, stretched, or external substitute.

## WCAG delivery gate

Before every delivery, inspect Figma component and variable bindings for every custom or changed element; visual resemblance alone is not proof of Telegrafen origin. If the origin cannot be verified, ask or report `BLOCKED`.

Run a [WCAG 2.2](https://www.w3.org/TR/WCAG22/) Level AA design review on every visible section of every supplied screen or frame in the submitted mockup, and on every visible mode and state in scope. Exclude unrelated pages and hidden prototype branches unless the user explicitly includes them.

- Normal text has at least 4.5:1 contrast; WCAG large text has at least 3:1.
- UI components, meaningful graphics, and state indicators have at least 3:1 contrast against adjacent colors.
- Keyboard focus is visible and is not obscured.
- Pointer targets are at least 24 × 24 CSS px unless a documented WCAG exception applies.
- Labels, status, and meaning do not depend on color alone; agreed keyboard and interaction behavior is represented where the mockup can show it.

Run the review separately for light and dark modes. A Figma review validates design evidence only; it cannot prove implementation semantics or full product conformance.

When a clear Telegrafen-compliant correction exists in the changed section or its directly connected states and surfaces, apply it automatically and rerun the review. Ask before a correction would change the agreed hierarchy, interaction, or design direction. For unrelated visible sections in a scoped update, report issues but do not modify them unless the user asks.

Never omit the result from the handoff. State `WCAG 2.2 AA design review: PASS`, `NEEDS CHANGES`, or `BLOCKED`, followed by the modes and states checked, failures or exceptions, and implementation-only items that could not be verified. Overall QA cannot be `PASS` when this review is missing or fails. For a scoped update, also state `Requested change QA: PASS`, `NEEDS CHANGES`, or `BLOCKED`; it may pass while the overall review needs changes because of an unrelated visible section.

## Quick QA

Review only the visible mockup and the states needed for the current concept:

- Existing Telegrafen components are used where they fit and remain intact.
- Every custom or changed element has verified Telegrafen component and token bindings; origin is not inferred from appearance.
- Library instances contain no unapproved strokes or effects.
- New product components use Telegrafen controls and are not presented as library components.
- Custom layers have semantic, consistent names; no generic Figma node names remain.
- Every visible icon comes from the correct Telegrafen icon library and keeps its original proportions.
- The official Telenor symbol is used in its Telenor brand-blue asset for brand identity; “Telenor” is not typeset as a substitute logo.
- Every custom text element uses a published Telegrafen text style.
- The complete visible H1–H5 outline is logical, uses one H1 per distinct view by default, and has no skipped levels or child headings that appear stronger than their parent.
- `Display`, `Title`, `Text`, and `Content` are used for their intended roles; heading levels, family and size bindings, wrapping, and responsive behaviour have been inspected. If the bindings cannot be inspected, typography structure QA is `BLOCKED` even when the screenshot looks correct.
- Semantic colors and standard control sizes come from Telegrafen tokens.
- Every dark-background region has been checked in full, including nested surfaces, text, icons, dividers, states, and every Button with `Neutral = Off`.
- Each supplied target frame has no unintended clipping, overlap, hidden control, or unusable text.
- The WCAG 2.2 AA design review is recorded and passes before overall QA is `PASS`.
- No external component has been copied or re-skinned.

Report `PASS` when the visible mockup contains no invented, distorted, or externally sourced design-system elements. Report `NEEDS CHANGES` when a visible issue can be corrected. Report `BLOCKED` only when an essential source or asset cannot be accessed or verified.

## Short handoff

Report:

- Main Telegrafen components used
- Product components created, if any
- Important icons and text styles used
- Intended H1–H5 outline and material typography decisions, when relevant
- Agreed decisions and missing assets
- `WCAG 2.2 AA design review: PASS`, `NEEDS CHANGES`, or `BLOCKED`, including modes and states checked, exceptions or failures, and implementation-only items not verified
- `Requested change QA: PASS`, `NEEDS CHANGES`, or `BLOCKED`, when updating an existing selected design
- `Conversion and ethical UX review`, when requested: conversion event, evidence-backed findings or stated hypotheses, dark patterns found, and Telegrafen-compliant recommendations
- QA result: `PASS`, `NEEDS CHANGES`, or `BLOCKED`

## Product reference — TV and broadband

Use this dated snapshot only for private-customer TV, broadband, WiFi, and T-We mockups. It is not a source for mobile, insurance, business, or other Telenor product areas.

- Use these names, speeds, inclusions, and prices as realistic mockup content. Prices are standard prices including mva unless stated otherwise.
- If the user asks for live, launch-ready, or current commercial information, require refreshed user-provided or verified content. Do not present this snapshot as current.
- Do not make T-We the default recommendation: it is scheduled for retirement in January 2027.
- For prices marked as changing, use a neutral placeholder or ask which effective date the mockup represents.

**Kilde:** Telenors [prisliste for TV og bredbånd](https://www.telenor.no/vilkar/prisliste-tv-og-bredband/)

**Sist kontrollert:** 30. juli 2026  
**Oppgitt virkningsdato for prisliste:** 1. februar 2026

### Fiberbredbånd

| Produkt | Månedspris |
| --- | --- |
| Bredbånd 150 | 1 048,-/md. |
| Bredbånd 500 | 1 148,-/md. |
| Bredbånd 1000 | 1 398,-/md. |

### Trådløst bredbånd

| Produkt | Månedspris |
| --- | --- |
| Trådløst Bredbånd 500 | 1 149,-/md. |
| Trådløst Bredbånd 250 | 999,-/md. |
| Trådløst Bredbånd 100 | 899,-/md. |
| Trådløst Bredbånd 50 | 849,-/md. |
| Trådløst Bredbånd 30 | 849,-/md. |
| Trådløst Bredbånd 10 | 799,-/md. |

### Trådløst bredbånd hytte

| Produkt | Månedspris |
| --- | --- |
| Trådløst Bredbånd Hytte 100 | 699,-/md. |
| Trådløst Bredbånd Hytte 60 | 699,-/md. |
| Trådløst Bredbånd Hytte 30 | 669,-/md. |
| Trådløst Bredbånd Hytte 10 | 599,-/md. |

### TV-tjenester

| Produkt | Månedspris | Merknad |
| --- | --- | --- |
| T-We | 690,-/md. | Planlagt avviklet i januar 2027 |
| T-We & Streaming | 849,-/md. | |
| T-We Classic | 699,-/md. | |
| Ekstra programkort | Avklar før bruk | Kilden oppga prisendring til 99,-/md. fra 1. juli 2026 |
| Poengpakke, 20 poeng | 29,-/md. | Kilden oppga prisendring til 35,-/md. fra 1. september 2026 |
| Opptak | 99,-/md. | |

### TV-tillegg

| Produkt | Pris |
| --- | --- |
| V premium | 699,-/md. |
| Select | Fra 149,-/md. |
| Filmleie | 39–59,- per film |

### Utstyr

| Produkt | Månedspris |
| --- | --- |
| WiFi Ruter | 49,-/md. |
| WiFi Ruter II | 49,-/md. |
| WiFi Forsterker | 29,-/md. |
| WiFi Forsterker II | 39,-/md. |
| T-We Boks II with recorder | 129,-/md. |
| T-We Boks II without recorder | 99,-/md. |
| T-We Boks III | 129,-/md. |

### Etableringskostnader

| Tjeneste | Engangspris |
| --- | --- |
| Hybridfiber, new cable to home | 1 990,- |
| Fiber, new cable to home | 4 990,- |
| TV or broadband setup for existing customer, without technician | 399,- |
| TV or broadband setup for existing customer, with technician | 695,- |
