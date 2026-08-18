---
name: minimalist-portrait-line-art
description: Transform uploaded portrait, full-body, fashion, couple, and group photos into recognizable minimalist black-and-white line-art likenesses when a user wants a sparse hand-drawn reinterpretation that preserves people, pose, composition, and key identity cues.
---

# Minimalist Portrait Line Art

Use this Skill to turn a supplied photo into clean black-and-white minimalist portrait line art with native ChatGPT or Codex image editing or image generation capabilities. Keep the workflow host-independent, do not add API code or infrastructure, and do not claim success when the active environment cannot edit images.

## Input gate

Check whether a usable source photo is available before doing anything else.

- If no usable source photo is present, ask the user to attach one.
- If a source photo is already available, do not ask unnecessary questions.
- If the current host does not expose image editing or image generation for this task, explain that the Skill requires a ChatGPT or Codex environment with image editing and stop there.

## Image roles

When one or more images are supplied, label them explicitly inside the working prompt:

- `Edit target`: the person or people that must be preserved.
- `Style reference`: an optional example of the desired visual language.
- `Supporting reference`: optional extra context for clothing, accessories, or an environmental object the user wants preserved.

Never treat a style reference as the person to reproduce.

## Visual invariants

Before generation, identify and preserve:

- Number of people
- Relative placement of people
- Crop and framing
- Body pose
- Hand gestures
- Leg position or walking stance
- Head direction
- Gaze direction
- Body proportions
- Hairstyle
- Expression
- Clothing silhouette
- Important collars, cuffs, waistlines, pockets, seams, and straps
- Hats, bags, flowers, glasses, and other important accessories
- Held objects
- Important overlap or occlusion relationships
- Any background element the user explicitly wants preserved

## References

Read these files before building or accepting the output:

- [references/style-guide.md](references/style-guide.md)
- [references/prompt-recipes.md](references/prompt-recipes.md)
- [references/quality-checklist.md](references/quality-checklist.md)

Keep detailed style rules, prompt patterns, and acceptance criteria in those references rather than duplicating them here.

## Prompt construction

Build a structured English image-editing prompt that clearly specifies:

- Use case
- Asset type
- Primary request
- Input image roles
- Subject invariants
- Style and medium
- Composition and framing
- Color palette
- Required constraints
- Prohibited elements

For edits, repeat the invariants explicitly. Keep structured prompt text in English even when the user speaks another language.

## Generation

Generate one result by default.

- Use image editing rather than unconstrained generation when the supplied people, pose, or composition must be preserved closely.
- Generate multiple variants only when the user explicitly asks for variants.
- Never add visible text unless the user explicitly asks for it.

## Evaluation

Before accepting the result, check:

- Subject count
- Relative placement
- Pose
- Gaze
- Crop
- Recognizability
- Hairstyle
- Expression
- Clothing silhouette
- Accessories
- Held objects
- Line economy
- White space
- Background handling
- Prohibited elements

## Correction policy

Perform at most one targeted correction when there is one clear failure.

- Too detailed: reduce interior lines only.
- Too realistic: simplify facial, hand, or material detail only.
- Too generic: restore only the missing identity cue.
- Pose drift: restore pose and framing only.
- Background residue: remove background only.
- Extra object: remove the extra object only.
- Excessive black areas: reduce solid fills only.

If several major constraints fail at once, explain the limitation honestly and ask whether the user wants another iteration instead of restarting with unrelated creative changes.

## Response style

Accept requests in any language and reply in the user's language unless they ask otherwise.

Briefly report:

- Which identity and composition cues were preserved
- Which details were intentionally simplified
- Whether a targeted correction was performed
- Any remaining limitation

Do not expose unnecessary internal implementation details.
