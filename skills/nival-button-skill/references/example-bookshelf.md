# EXAMPLE: Animated Bookshelf Navigation Link

This is one worked example, not a template or a style requirement. It covers only the bookshelf-button design session, beginning with the request to add the navigation item.

## Brief

Add “书架” between the home and personal-introduction navigation items. On hover, change “书” into stacked books and “架” into a standing shelf. The user allowed an image or HTML preview before integration.

## Initial Preview

Build a standalone HTML page with the navigation at actual size and an enlarged instance below it. Reuse the same markup and styles for both instances. HTML was chosen because the main design question involved an interactive transition.

The initial mechanism fades and moves the letters out while revealing SVG illustrations. The interaction returns to text when the trigger ends. This is a visual replacement, not a geometric morph of the letter outlines.

## Feedback and Revisions

| User feedback | Revision | Reason retained for other work |
| --- | --- | --- |
| Give the letters book-like colors and add a left icon. | Try brown and muted green text with a shelf icon. | Evaluate the default state separately from the animated state. |
| Make both letters brown; use a smaller quill. | Unify text color and reduce the replacement icon. | Follow the latest explicit choice and adjust visual hierarchy. |
| The quill looks like a leaf; use a ladder. | Replace it with a small wooden ladder. | Recognizability matters more than the intended name of an icon. |
| The shelf looks like a cabinet; it should stand upright. | Use two vertical supports and three open shelves, without a cabinet body or drawer. | Correct structural meaning before decorative detail. |
| Move the ladder about five pixels closer to the text. | Reduce the icon-to-text spacing by that amount. | Make a local change without changing accepted geometry elsewhere. |
| The ladder must not be taller than the letter. | Reduce its height and keep center alignment. | Use neighboring content as a relative size constraint. |
| Enlarge it a little. | Increase its size by about eight percent. | Use a small reversible adjustment for vague magnitude feedback. |
| Enlarge the ladder together with the hover effect. | Add coordinated scaling and preserve recovery to the default state. | Review the whole component when changing its interaction. |
| Approved; deploy it. | Integrate the accepted component into the existing header. | Preview work and production integration have different scopes. |

## Example-Specific Values

The final example uses brown text, a wooden ladder, colored book stacks, and an open standing shelf. The ladder is sized at 0.86em by 1.08em, with a -1px trailing margin within a layout that also has a gap. It scales to 1.25 on hover or visible keyboard focus. These are implementation values from this example, not general sizing rules. The visible outline occupies less than the full SVG box.

The navigation destination was inferred as the existing content library, `/library`. That destination was not specified in the initial design request and must not be generalized.

## Implementation and Evidence

The preview used HTML, CSS, and SVG. The production version used a React link and scoped CSS, with an accessible name, decorative SVGs hidden from assistive technology, visible keyboard focus, and reduced-motion handling.

The recorded checks covered rendering, the main animation triggered by keyboard focus, successful navigation, a production build, and the deployed header. They did not establish a complete accessibility audit, measured contrast compliance, touch behavior, or a separately recorded pointer enter/leave test. Those gaps remain verification limits, not successful checks.

## Transferable Result

The useful method is to clarify meaning, provide a working preview at two scales, make bounded revisions, preserve accepted choices, and verify authorized integration. A different button may need different states, no icon, no animation, and an entirely different visual style.
