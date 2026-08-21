# Telegrafen design skills

Portable Agent Skills for creating and reviewing private-customer Telenor designs with the Telegrafen Design System. Each skill has a self-contained `SKILL.md` entry point for use in Figma Make and other systems that support the Agent Skills format.

## Structure

```text
skills/
├── telegrafen-design-mockups/SKILL.md
├── telegrafen-design-components/SKILL.md
└── telegrafen-ux-writing/SKILL.md
```

## Skills

- [Telegrafen design mockups](skills/telegrafen-design-mockups/SKILL.md) — Create, update, and QA Telegrafen-native mockups and prototypes. Covers tokens, components, approved imagery, accessibility, conversion and ethical-UX review, and a dated TV and broadband product reference.
- [Telegrafen component design](skills/telegrafen-design-components/SKILL.md) — Create, iterate, review, and finalize individual Telegrafen or Telenor components in Figma.
- [Telegrafen UX Writing](skills/telegrafen-ux-writing/SKILL.md) — Create, update, and QA Norwegian Bokmål UX microcopy for Telenor private-customer designs and interfaces.

## Use

Use the relevant skill’s `SKILL.md` file as the installable entry point:

- **Figma Make:** add the selected `SKILL.md` as the skill document.
- **Other Agent Skills-compatible systems:** install or copy the complete skill folder, keeping the file name `SKILL.md` and its frontmatter intact.

Use the mockup skill for screens and flows, the component skill for reusable components, and the UX Writing skill for customer-facing interface copy.

The skills use the published Telegrafen Figma libraries as their source of truth. They are intended for design work only and do not replace product, legal, accessibility, or implementation review.

## Commercial content

The mockup skill includes a dated TV and broadband product snapshot for realistic concept content. Refresh or provide verified material before presenting prices, offers, or other commercial facts as current or launch-ready.

## Versioning

Changes are tracked in Git. Update a skill’s version in its frontmatter when making a material change, then commit the change with a clear summary. Use Git tags for released versions.
