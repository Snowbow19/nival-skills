---
name: design-ui-components
description: Use when a user wants to design or refine a UI component, its visual states, or its interactions through a working preview and feedback. Applies to controls, cards, inputs, menus, and other components in any visual style.
---

# Design UI Components

Develop the component with the user. Preserve accepted choices while refining the parts they change. No particular color, icon, layout, or motion style is required.

## Inputs

Read the current request, relevant feedback, reference images, and existing product files first. Determine:

- Purpose: component type, user action, and expected result.
- Context: placement, neighboring elements, target devices, and edit boundaries.
- Appearance: style, brand rules, copy, icons if needed, and visual hierarchy.
- Geometry: container constraints, relative sizes, spacing, and alignment.
- Behavior: applicable states, input methods, transitions, and recovery.
- Delivery: exploration, preview, existing-component edit, or product integration.

Ask only for missing information that would materially change the design. Treat an inferred choice as a proposal, not as a confirmed preference. When feedback changes a choice, use the latest explicit direction.

## Resolve Ambiguous Visual Direction

When a style feeling has several plausible meanings, use [Style and color calibration](references/style-color.md). Ground proposals in the actual page and compare them in context. Do not turn style words or example palettes into fixed defaults.

## Flow

1. **Understand the component.** Identify what it does and what must remain unchanged. Distinguish visual exploration from a functional change.
2. **Define applicable states.** Map each relevant trigger to its visible result and recovery. A link needs a destination; a toggle needs a value; an input needs editing behavior; a menu needs opening, selection, and dismissal. A static card may need no interaction.
3. **Build an HTML preview.** By default, include a true-size view and an enlarged detail view. Include nearby product context when available. Use one component implementation and the same state logic in both views; enlarge its presentation instead of maintaining a separate design. Keep independent instances accessible, with unique IDs.
4. **Review in context.** Check readability, proportions, meaning, layout, and applicable interactions at actual size. Use the enlarged view to inspect details, not to judge touch-target size or overall balance.
5. **Iterate from feedback.** Change the requested property or related group. Preserve other accepted choices. Explain the change briefly in chat and keep the preview current. Continue routine edits without a formal approval gate after each action. Ask when feedback has materially different interpretations.
6. **Verify and deliver.** Run the applicable checks below. Integrate only within the authorized scope, using the accepted design. Existing authorization remains valid. Check the component again in its real product environment; preview success alone does not prove integration success.

Keep visible UI copy suitable for a finished product. Put design reasoning, review instructions, simulated behavior, and verification limits in chat, not in the component.

## Decision Rules

- When editing an existing product, prefer its established conventions because the component must work with its surroundings. When the user requests a new style, use that direction instead.
- When behavior affects the judgment, prefer an interactive preview because an image cannot show triggers, transitions, or recovery.
- When an icon is misread, prefer correcting its silhouette and structure because decoration cannot repair the wrong meaning. Icons are optional.
- When size or spacing feels wrong, prefer comparing related elements at actual size because nominal CSS dimensions may not match visible bounds.
- When feedback is local, prefer a bounded change because it makes comparison clear and protects accepted work.
- When an adjustment amount is vague, prefer a small reversible change and state its magnitude because a large guess may miss the intended balance.
- When several elements change state, prefer a coherent trigger and recovery because their feedback should read as one interaction. Do not animate unrelated elements.
- When motion adds no useful feedback or conflicts with the requested style, prefer a static response because motion is a choice, not a requirement.
- When an action is essential, prefer controls usable by the applicable keyboard, pointer, and touch inputs because hover cannot be the only way to perform it.

## Quality Checklist

Check each relevant item. Mark a state not applicable when the behavior does not require it.

- Meaning: labels, icons, semantics, and action results agree.
- Geometry: readable at actual size; intended hierarchy and alignment; no unintended overlap, clipping, or layout shift, including with long content and narrow containers.
- States: default, hover, focus, pressed, selected, expanded, disabled, loading, error, and success as applicable. Check entry, exit, repeated use, and recovery.
- Accessibility: suitable native semantics, accessible names and state values, logical focus order, visible focus, applicable keyboard behavior, and usable target sizes. Do not rely on color alone.
- Contrast: measure text and required visual indicators against their actual backgrounds in each relevant state; meet the applicable accessibility target. Do not judge contrast from appearance alone.
- Motion: does not obstruct input; remains coherent during rapid changes; respects reduced-motion preferences.
- Consistency: true-size and detail views reflect the same design; integration preserves accepted choices and surrounding product behavior.
- Evidence: distinguish implementation from observed verification. Report untested interactions and limits. A successful build is not a visual or accessibility pass.

- After a color change, repeat affected contrast and harmony checks. For gradients, check intermediate colors and final compositing, not only endpoints or isolated swatches.

## Output

Provide:

1. A working HTML preview with true-size and enlarged views, plus an editable source file.
2. A short chat summary of the current choices and the latest change.
3. Checks performed, observed results, and material limits.
4. Any unresolved design decision, or the verified integration location when integration was authorized.

For unresolved color direction, include a small set of comparable options, their changed properties, and the user's selected direction.

## Optional Example

Read [EXAMPLE: animated navigation link](references/example-bookshelf.md) only when a worked example is useful. Its imagery, values, and technology are not defaults for new work.

Read [EXAMPLE: portfolio color refinement](references/example-portfolio-colors.md) only when the color workflow needs a worked example. Its palette is not a default.
