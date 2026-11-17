# EXAMPLE: Portfolio Navigation Color Refinement

This example records one user's accepted direction on one page. Its colors, material, and component are not defaults for other work.

## Context and Outcome

The page used warm off-white backgrounds, dark text, a brown neighboring link, and a blue brand link. The component was a portfolio navigation link with a stack of illustrated cards that opened on hover or keyboard focus.

The user initially asked for rainbow-like color. Successive feedback rejected the first palette as too subdued, then rejected a brighter palette as too bright. The user clarified a colored-pen-on-warm-paper feeling, then requested fewer colors, reference to adjacent text, and finally a slightly stronger red-to-blue gradient. This shows that rainbow-like did not mean all spectral colors.

The accepted text gradient used warm red `#c45748` and blue `#397fae`, with stops at 8% and 92% and an angle of 105 degrees. A light underline used `#e8beb5` and `#b5d2e5`. These are historical example values, not a recommended general palette.

The user also found that the underline obscured the letter strokes. Moving the underline to a lower sibling layer corrected that composition issue. Palette selection alone could not solve it.

## Apply the Updated Method

For a new attempt, first inspect the actual background and adjacent text. Translate the ambiguous request into candidate hue spans, chroma bands, lightness bands, and gradient transition choices. Compare a restrained two-hue direction with a broader multicolor direction in the same navigation context. Let the user choose the nearest direction before fine tuning.

For controlled exploration, express candidate colors in OKLCH rather than repeatedly guessing unrelated hexadecimal palettes. Do not claim the historical process used OKLCH: it did not. Do not force hue-only rotation if the path introduces unwanted intermediate colors or fails contrast.

After selection, check the rendered gradient, underline, and relevant states together. Preserve accepted geometry and animation while adjusting color.

## Evidence Limits

The recorded session demonstrated rendered previews, user preference, focus-triggered animation, navigation, and deployment. A contrast calculation was made for an earlier purple design; it does not validate the later red-blue palette. No final contrast audit was recorded.

The proposed calibration method has not been regression-tested against this example or stress-tested on other components in this update. The user explicitly requested skipping local tests. This file is an illustrative application of the method, not a report of a successful test.
