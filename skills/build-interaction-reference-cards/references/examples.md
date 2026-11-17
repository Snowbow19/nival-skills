# Examples — Illustrations, Not Templates

## A. Observed Card: Hand Pointer

The user supplied a sketch with a working example on the left, terminology and pointer visuals at the upper right, and an AI instruction plus use cases below.

The main example became a travel-project card. Its action uses `cursor: pointer` and opens a local detail dialog. The user removed a redundant surrounding blue panel, leaving the example card itself.

The first decorative hand icon was replaced with platform references. The Mac illustration was updated to the local macOS 27 resource. The Windows raster was visibly off-center because of transparent padding, then proved too small for clear enlargement. Its visible bounds were centered; the final display became a reference-based SVG redraw. That redraw is not an extracted Windows system asset.

The user replaced overly casual copy with: “当光标在这个元素上时，使用**手形指针 / Pointer**。” The paired keyword is bold; the sentence remains short and technically precise.

Use-case categories first appeared as chips, then as interactive mini examples. The user removed their redundant surrounding boxes, reduced the set to three, and requested one horizontal row with consistent dimensions and alignment. The retained examples were a text link, a clickable card, and a save button.

Observed verification included opening dialogs, changing a save state, reading the computed cursor value, and measuring equal sample bounds. These observations do not establish a complete accessibility or cross-platform audit.

Transfer: verify visual meaning, demonstrate actual behavior, use concise terminology, remove redundant hierarchy, and align comparable examples. Do not transfer the travel scene, three-item count, fixed row height, or operating-system pair as defaults.

## B. Conceptual Card: Reorder a List

This is a design walkthrough, not a built or tested widget.

- Topic: reorder a short reading list.
- Main example: move a reading item to another position, with a visible drop target and the resulting order. Provide keyboard move controls so dragging is not the only method.
- Terms: “拖拽排序 / Drag and drop.”
- Reference visual: before, dragging, and dropped states; no Mac/Windows comparison unless requested.
- AI instruction: “让用户通过**拖拽排序 / Drag and drop**调整列表顺序，并提供键盘移动方式。”
- Use cases: a reading queue and a task-priority list, each with working reordering. Two distinct examples suffice here.
- Layout consequence: a taller main example accommodates list movement; sample widths follow the available space rather than the pointer card's fixed row.
- Checks: order changes, canceled drags, focus after movement, keyboard operation, and readable feedback.

## C. Conceptual Card: Inline Form Validation

This is a design walkthrough, not a built or tested widget.

- Topic: help users correct an invalid field.
- Main example: an email field, a submit action, a specific inline error, and a successful correction. No data is sent externally.
- Terms: “行内校验 / Inline validation.”
- Reference visual: invalid and corrected field states, not a cursor drawing.
- AI instruction: “提交时检查邮箱格式；有问题就在输入框旁显示**行内校验 / Inline validation**信息，修改正确后清除错误。”
- Use cases: an email format check and a required-field check. Each must demonstrate a different useful error, not two copies of the same form.
- Layout consequence: reserve space for errors and allow long messages; the instructional groups remain, while the interactive area is a form rather than a project card.
- Checks: error timing, association with the field, keyboard submission, correction, announcement, and avoiding color-only feedback.

## Overfit Check

The shared outer teaching sequence is intentional because this skill targets interaction reference cards. The inner widget, relevant states, reference visuals, sample count, and verification differ substantially.

The method would be overfit if it always produced travel cards, pointer images, platform badges, three equal-height samples, or hover effects. Equal spacing does not require identical control shapes. Layout must adapt when the instructional interaction needs more room.
