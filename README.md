# Telegrafen design skills

Portable Agent Skills for creating and reviewing private-customer Telenor designs with the Telegrafen Design System. Each skill has a self-contained `SKILL.md` entry point for use in Figma Make and other systems that support the Agent Skills format.

## Structure

```text
skills/
├── telegrafen-visual-design/SKILL.md
├── telegrafen-design-mockups/SKILL.md
├── telegrafen-design-components/SKILL.md
└── telegrafen-ux-writing/SKILL.md
```

## Skills

- [Telegrafen visual design](skills/telegrafen-visual-design/SKILL.md) — Art-direct Telegrafen-governed designs so their hierarchy, composition, visual weight, typography, colour, imagery, motion, accessibility, and brand expression feel clear, premium, and distinctly Telenor.
- [Telegrafen design mockups](skills/telegrafen-design-mockups/SKILL.md) — Create, update, and QA Telegrafen-native mockups and prototypes. Covers tokens, components, responsive typography and heading hierarchy, approved imagery, accessibility, conversion and ethical-UX review, and a dated TV and broadband product reference.
- [Telegrafen component design](skills/telegrafen-design-components/SKILL.md) — Create, iterate, review, and finalize individual Telegrafen or Telenor components in Figma, including reusable typography contracts that respect their page context.
- [Telegrafen UX Writing](skills/telegrafen-ux-writing/SKILL.md) — Create, update, and QA Norwegian Bokmål UX microcopy for Telenor private-customer designs and interfaces.

## Use

Use the relevant skill’s `SKILL.md` file as the installable entry point:

- **Figma Make:** add the selected `SKILL.md` as the skill document.
- **Other Agent Skills-compatible systems:** install or copy the complete skill folder, keeping the file name `SKILL.md` and its frontmatter intact.

The skills use the published Telegrafen Figma libraries as their source of truth. They are intended for design work only and do not replace product, legal, accessibility, or implementation review.

## Which skill should I use?

Choose the primary skill according to the artifact or responsibility at the centre of the task:

| Need | Primary skill |
|---|---|
| Art-direct or review visual hierarchy, composition, visual weight, premium quality, or Telenor brand expression | [Telegrafen visual design](skills/telegrafen-visual-design/SKILL.md) |
| Create or update a screen, page, flow, product layout, mockup, or prototype | [Telegrafen design mockups](skills/telegrafen-design-mockups/SKILL.md) |
| Create, iterate, repair, or finalize a reusable component and its properties, variants, states, and behavior | [Telegrafen component design](skills/telegrafen-design-components/SKILL.md) |
| Create, rewrite, directly update, or QA Norwegian Bokmål interface copy | [Telegrafen UX Writing](skills/telegrafen-ux-writing/SKILL.md) |

Combine skills when the task crosses responsibilities. Keep one skill primary and use the others for their specialist decisions:

- **Premium page or flow:** use design mockups to construct it and visual design to art-direct it.
- **Reusable component in context:** use component design for the component contract and visual design for hierarchy and expression in its surrounding composition.
- **Screen with new or revised interface copy:** use design mockups for the screen and UX Writing for the customer-facing language.
- **Full design review:** use visual design for the art-direction review, then add component design, mockups, or UX Writing when their specialist QA is in scope.

Visual design does not replace component construction, mockup assembly, or UX writing. The construction and writing skills do not replace visual art direction.

## Commercial content

The mockup skill includes a dated TV and broadband product snapshot for realistic concept content. Refresh or provide verified material before presenting prices, offers, or other commercial facts as current or launch-ready.

## Versioning

Changes are tracked in Git. Update a skill’s version in its frontmatter when making a material change, then commit the change with a clear summary. When a versioned frontmatter name changes, update exact cross-skill references to that name. Use Git tags for released versions.
