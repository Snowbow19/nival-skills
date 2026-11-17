# Style and Color Calibration

Use this method when words such as colorful, soft, vivid, or paper-like leave materially different visual interpretations. For a precise color replacement, make the requested change and check its effects without starting a new exploration.

## 1. Read the Context

Inspect the actual page, relevant styles, and the component at its intended size. Identify the background, adjacent text, accents, semantic colors, and material treatment. Prefer computed styles and source tokens for color values; use screenshots for visual relationships. If only an image is available, describe sampled colors as estimates.

Record observed values separately from inferred mood. Summarize background lightness and temperature, accent chroma, text contrast, and visual emphasis. Do not infer a fixed palette from a page label such as playful or minimal. Identify the color's role: text, surface, border, focus indicator, semantic state, or decoration.

## 2. Translate the Feeling

Map the request to controllable properties:

- Hue family, span, direction, and number of colors.
- Lightness and chroma bands relative to the page.
- Gradient interpolation space, stop positions, and transition character.
- Opacity, blending, texture, and movement only where relevant.
- Intended emphasis compared with neighboring components.

Treat the mapping as a proposal. Colorful does not necessarily mean a full-spectrum gradient. Bright can mean lighter, more chromatic, or more prominent. Ask a focused question or show alternatives when the distinction matters. Do not ask the user to supply technical color coordinates.

## 3. Build Controlled Candidates

Use OKLCH to separate lightness (L), chroma (C), and hue (H). Derive initial L and C bands from the page and the component's role. Vary hue while initially holding L and C stable to isolate that variable. This is an exploration technique, not a universal constraint.

Adjust L or C when contrast, output gamut, or the intended appearance requires it. Equal OKLCH lightness does not guarantee equal contrast against a background. Treat supported color gamut and browser rendering as constraints; do not rely on unexamined channel clipping.

Specify the gradient interpolation space and hue path deliberately. A hue sweep and a direct perceptual blend can produce different intermediate colors. When intermediate hues fight the brief, prefer a narrower path or another interpolation choice because endpoint colors alone do not define the gradient.

Do not add blending or transparency merely to imitate a material word. Prefer them only when their rendered effect helps the requested appearance and remains readable. Keep semantic state colors distinct where the product relies on them.

## 4. Compare in Context

Provide a small set of genuinely different candidates at actual size, on the same background and with the same neighboring content. Keep geometry, text, and behavior fixed. Vary one property group at a time and explain the difference in chat. The number of options depends on the unresolved decision, not a fixed quota.

Use the shared component implementation for true-size and enlarged views. Ask which direction is closest and what still feels wrong. If the user provides a clear choice, apply it without another selection round. Preserve accepted properties in later revisions.

## 5. Check and Report

Measure text and required indicator contrast on their actual backgrounds in applicable states. Check gradient interiors, not just stops. Include opacity, blending, and overlapping decorations in the final composition. Sample densely enough to detect a failing region; report the sampling method and its limits rather than implying mathematical proof.

Evaluate harmony at actual size: does the component have the intended emphasis, remain readable beside nearby text, and fit the page's existing palette and material treatment? A contrast pass is not proof of aesthetic fit. Separate measured results, the agent's visual judgment, and the user's acceptance.

After changes, repeat the affected checks. If a check is skipped or unavailable, record that limit. User acceptance does not establish accessibility compliance.

## Style Vocabulary

These relative bands are candidate directions, not fixed presets. Calibrate them to the page and component role. Put task-specific numeric ranges in the design notes, not in this general vocabulary.

| Word | Candidate property bands | Question to resolve if needed |
| --- | --- | --- |
| Pastel | Higher L; low-to-moderate C; hue range open | Soft surfaces, or readable colored text? |
| Muted | Lower C than the relevant accents; L set by background and role | Less saturated, less prominent, or both? |
| Aurora | Related hues over a broader span; smooth transitions; C and L set by context | A static gradient, or a moving light effect? |
| Iridescent | Hue changes across position or state; bounded L variation | Color shift alone, or a reflective material effect? |
| Ink on paper | Background-informed hue and moderate or reduced C; L chosen for legibility | Flat ink color, or visible texture and translucency? |
| Vivid | Higher C than the current candidate, within gamut; avoid uncontrolled L changes | Stronger color, or greater overall emphasis? |

Aurora does not require glow. Iridescent does not require animation. Paper does not require a warm background. No term overrides the user's references or the component's accessibility needs.

## Sources

- [CSS Color 4: Oklab and OKLCH](https://www.w3.org/TR/css-color-4/#ok-lab)
- [WCAG: Contrast Minimum](https://www.w3.org/WAI/WCAG22/Understanding/contrast-minimum.html)
