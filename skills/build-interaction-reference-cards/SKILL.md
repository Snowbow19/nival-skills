---
name: build-interaction-reference-cards
description: Use when the user wants an instructional card that combines a working interaction example, terminology, a reusable AI instruction, and appropriate use cases. Applies to interaction reference cards, not standalone button design.
---

# Build Interaction Reference Cards

## When to Use

Create or revise a card that helps a reader recognize an interaction, try it, describe it to AI, and know when to use it. Use the current brief and relevant reference material. This format teaches an interaction concept; it is not a template for every kind of knowledge or UI widget.

## Inputs

Infer available information before asking. Ask when a missing detail would change the behavior, layout, or technical accuracy.

| Variable | Default | Decision rule |
| --- | --- | --- |
| Topic | One interaction concept | Split concepts when their purpose or behavior differs. |
| Audience and language | Current conversation language; beginner-friendly wording | Match the audience's terminology and prior knowledge. |
| Names and technical terms | Human-readable name plus canonical technical term | Add bilingual keywords when they help map natural language to implementation. |
| Layout | Working example on the left; reference content on the right | Follow the supplied sketch; stack sections on narrow screens while preserving reading order. |
| Visual style | Existing page style, when available | Use the user's reference and the card's background; do not impose a fixed palette. |
| Main example | One familiar scenario with working behavior | Choose the smallest scenario that clearly demonstrates the concept and its result. |
| Reference visual | Include when appearance is part of the lesson | Use relevant symbols, states, or diagrams; omit redundant visuals. |
| Platform variants | None unless the appearance or behavior differs | Include only the platforms and versions relevant to the reader. |
| AI instruction | One concise, precise sentence | Describe the trigger, target, and intended behavior; bold paired native-language and English keywords when requested. |
| Use-case samples | A small representative set | Keep cases that teach distinct uses; remove redundant cases before shrinking content. |
| Sample sizing | Equal columns, aligned content, comparable visual weight | Match bounding boxes for comparable peers without making links look like buttons or distorting illustrations. |
| Delivery | Editable local HTML preview | Publish or integrate only within the requested scope. |

## Process

1. **Read the sketch and brief.** Identify required content, grouping, and behavior. Ask about genuinely unreadable details. Why: layout guesses can override the user's intended teaching sequence.
2. **Verify the concept and visual references.** Check technical terms and any platform-specific assets. Record source, version, and whether an asset is native or redrawn. Why: a plausible-looking symbol can still teach the wrong appearance or behavior.
3. **Build the main interaction.** Use an actual control with an observable result and a recovery path. Keep demonstrations local unless external effects are requested. Why: a static picture or cursor change alone does not demonstrate the action.
4. **Write the teaching content.** Connect the human-readable name, technical term, AI instruction, and use cases. Use plain, precise wording without excessive casual phrasing or unnecessary implementation detail. Why: readers need language they can reuse without changing the intended behavior.
5. **Make use cases representative and operable.** Let each label or example perform the action it represents. Avoid a caption plus a redundant demonstration of the same thing. Use a scene that matches each label, with distinct content and behavior rather than reskinning one repeated widget. Why: examples should teach through recognizable behavior, not merely enumerate categories.
6. **Refine the hierarchy.** Keep the main example and content groups distinct. Remove wrappers that add no useful grouping. Align peer samples and normalize reference visuals by visible bounds rather than transparent image dimensions. Why: visual noise and uneven weight obscure the comparison.
7. **Check and iterate.** Verify the applicable items below, then change only the requested aspects. Preserve accepted structure, copy, and behavior. Report observed results and material limits. Why: a bounded revision is easier to assess and less likely to undo accepted work.

## Quality Checklist

- The main example, terminology, and AI instruction describe the same behavior. Match the operation to its object: panning moves the scene; moving changes an object position; cropping changes the visible bounds without stretching the image; resizing changes the specified dimensions.
- When spatial order changes, provide a visible transition or placement cue so readers can track the result. Support cancellation, recovery, and reduced motion where relevant.
- Visible text contains the requested teaching content, not collaboration notes or unrequested caveats.
- Demonstrations have real local outcomes, usable focus states, suitable semantics, and applicable keyboard or touch behavior. Do not depend on hover for an essential action.
- Reference assets are sharp at the intended display size and pixel density. Platform labels do not imply that a redraw is an exact native asset. Keep provenance in handoff notes.
- Reference images are optically centered; transparent margins do not shift their visible shapes.
- Peer examples have consistent spacing, text scale, and alignment. Preserve meaningful differences between a link, a card, and a button.
- No unnecessary nested container duplicates a content group. No clipping or unreadable shrinking occurs on narrow screens.
- Contrast is checked against actual backgrounds; focus remains visible and motion respects reduced-motion settings.
- Copy actions copy the intended instruction, including the terminology, with success or fallback feedback.
- Check only relevant states and flows. State what was not verified; do not equate source inspection with a passing interaction test.

## Decision Rules

- When examples have different labels, prefer different recognizable scenes because labels alone do not demonstrate different uses.
- When a source supplies appearance but not behavior, verify the concept before implementing because a convincing drawing can still teach the wrong operation.
- When a platform label is long, expand the reference area before shrinking the text because the label must remain readable.
- When multiple cards are requested, verify one representative card first, then reuse its teaching structure while adapting each interaction and scene. Preserve accepted quality at the actual collection width.

## Examples — Illustrations, Not Templates

Read [worked examples](references/examples.md) when useful. The original pointer card and two contrasting card concepts illustrate the method. Their colors, platforms, scenarios, sample counts, and dimensions are not universal rules.

Deliver the editable HTML, a preview link or image, a brief change summary, and verification limits. Keep explanations about design decisions outside the card unless the user requests them as teaching content.

For the distinction between reusable rules, variables, and example-only choices, see [process analysis](references/process-analysis.md).
