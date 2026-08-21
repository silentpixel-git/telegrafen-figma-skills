---
name: telenor-ux-writing-v1
description: Use when creating, rewriting, directly updating, or QAing Norwegian Bokmål UX Writing for Telenor private-customer designs in Figma. Do not use it for campaigns, articles, product pages, emails, push notifications, or other long-form copy.
---

# Telenor UX Writing

Use this guide when creating, rewriting, or reviewing Norwegian UX copy for Telenor private customers in Figma. Write in Norwegian Bokmål.

This guide covers in-product microcopy only: labels, buttons, helper text, validation and errors, confirmations, empty and loading states, dialogs, onboarding, payments, security, and service interruptions. Do not use it for campaigns, articles, product pages, emails, push notifications, or other long-form copy.

## The voice

Write as Telenor: clear, calm, helpful, and competent.

- Use `du` for the customer and `vi` for Telenor.
- State what the customer can do or gets before explaining technical detail.
- Use short, natural sentences and familiar Norwegian words.
- Do not use em dashes or hyphens as pauses. Use full stops or rewrite the sentence instead.
- Be warm without becoming casual. Be confident without hype.
- Give a clear next step whenever one is useful.
- Use one exclamation mark at most; usually use none.

Avoid jargon, English phrasing translated word-for-word, fear, blame, slang, empty superlatives, pressure, and vague CTAs such as `Klikk her`.

Good: `Vi kunne ikke lagre endringen. Prøv igjen.`

Avoid: `Oops! Noe gikk galt med systemet vårt.`

## Required context

Before writing or changing copy, establish:

1. What the customer is trying to do.
2. Where the text appears: component or screen.
3. The current state: default, loading, selected, success, error, empty, disabled, or interrupted.
4. What happens after the customer acts.
5. The approved product facts, if the copy includes price, eligibility, timing, data allowance, coverage, policy, or a promise.

Ask for the missing context when it could change the meaning. Do not invent product facts. Use `[avklar med produktteamet]` for a missing fact if a draft must be shown.

## Create and rewrite copy

Return one recommended version by default. Provide alternatives only when asked.

Match the copy to its UI role:

| UI role | Write this |
|---|---|
| Button | A precise verb and outcome: `Lagre endringer`, `Se faktura`, `Prøv igjen` |
| Field label | What the customer must provide: `Mobilnummer` |
| Helper text | The minimum useful clarification: `Vi bruker nummeret for å sende deg en kode.` |
| Error | What happened, how to fix it, and the next step: `Skriv inn et gyldig mobilnummer.` |
| Confirmation | What is complete and what happens next: `Endringene er lagret.` |
| Empty state | What is absent and the useful next action: `Du har ingen åpne fakturaer.` |
| Loading | What is happening: `Henter forbruket ditt …` |
| Security or payment | Be factual, calm, and specific. Explain the action without alarming the customer. |

Do not use a button label that hides an irreversible consequence. Name the consequence clearly, for example `Slett eSIM` rather than `Fortsett`.

## Update selected Figma content

When a designer selects text, a component, or a frame and asks to update the mockup with UX copy:

1. Inspect the selected scope and its surrounding UI context.
2. Apply the one recommended version directly when the context and facts are clear.
3. Preserve the selected component, layout, and visual design. Change copy only unless asked otherwise.
4. Update related text in the same local flow when it would otherwise become inconsistent, such as a dialog title, body, and CTA.
5. Report briefly what changed.

Ask before editing if the selection is unclear, the task outcome is unknown, the copy contains an unverified product fact, or changing it may alter legal meaning.

## Protected copy

Do not invent, remove, or change the meaning of legal, price, consent, policy, eligibility, or security commitments.

When approved wording is supplied, keep its meaning intact. You may add a clearer explanation around it, or flag it for product/legal review. Do not turn uncertainty into certainty.

## QA UX copy in a design

Review selected content, a screen, or a flow for:

- clarity on first reading;
- correct use of `du` and `vi`;
- a specific next step where needed;
- useful help text rather than repeated labels;
- errors that explain both problem and recovery;
- clear consequences for destructive, payment, security, and consent actions;
- consistent terminology across the local flow;
- natural Norwegian, without jargon, hype, fear, blame, or translated English idioms;
- text that still works with long names, amounts, dates, and real product data.

For every issue, provide a ready-to-paste replacement:

`[Location] — [Issue] → [Recommended copy]`

Finish with one result: `PASS`, `NEEDS CHANGES`, or `BLOCKED`.

- `PASS`: copy is clear, factual, and consistent with this guide.
- `NEEDS CHANGES`: copy can be improved without missing information.
- `BLOCKED`: a required fact, outcome, or approved wording is missing.

## Final check

Before completing work, ask: does this help the customer understand what is happening and take the next step with confidence?
