---
name: minimalist-portrait-line-art
description: Transform uploaded portrait, full-body, fashion, couple, and group photos into recognizable minimalist black-and-white line-art likenesses when a user wants a sparse hand-drawn reinterpretation that preserves people, pose, composition, and key identity cues.
---

# Minimalist Portrait Line Art

Use this Skill to turn a supplied photo into clean black-and-white minimalist portrait line art with native ChatGPT or Codex image editing or image generation capabilities. Keep the workflow host-independent, do not add API code or infrastructure, and do not claim success when the active environment cannot edit images.

This Skill should prefer omission over explanation. If a detail is not required for recognizability, pose clarity, or a requested object, leave it out.

## Generation mindset

Do not simplify the photo by tracing edges and deleting details. Do not start from a realistic line-art version and repair it. Reconstruct a finished minimalist illustration from an abstract drawing plan.

The target style is intentionally incomplete and flat. Do not close every contour just because the photo has a visible boundary. Let viewers complete obvious forms through gaps, broken lines, and implied continuation. Remove light, shadow, volume, depth modeling, and realistic three-dimensional form.

Use this order of thinking before any generation:

- Pose skeleton: head, torso, arms, hands, legs, feet, weight, gaze, and contact points
- Body masses: large readable head, torso, hip, limb, and compressed-pose shapes
- Graphic block plan: one or two high-contrast fills only where they organize the image, such as hair, hat, jacket, or bag
- Primary contour plan: the few outer contour fragments that describe posture and silhouette
- Layer break plan: only the hems, openings, cuffs, collars, straps, and overlap breaks that prevent garments or limbs from merging
- Symbol plan: only the facial, hand, hair, and garment marks needed for expression, direction, posture, and life

The final image should feel drawable from memory as a sparse icon-like figure. If the prompt would require many connected contours, realistic face construction, fabric lines, or cleanup passes, the drawing plan is still too photographic.

Design the character from the pose and identity anchors, not from facial likeness. A successful result may look cuter, simpler, and more innocent than the source photo as long as the pose, gaze, clothing silhouette, hairstyle category, and held-object relationships remain correct. Do not make the face accurate by adding more face information; make it readable by reducing it to a few well-placed symbols.

Treat structural readability as more important than photographic outline fidelity. When a faithful photo contour would merge jacket with shorts, sleeve with arm, hand with object, or one person's arm with another person's body, add or preserve a minimal boundary break rather than tracing the continuous photo edge.

Do not solve recognizability by drawing realistic facial likeness. Preserve face direction, expression category, hairstyle, facial-hair category, glasses, and posture instead. Eyes, nose, and mouth should usually be dot-and-line symbols, not modeled features. A nose should normally be one dot, dash, or short angle; facial hair should be one abstract cue, not a shaped mustache or beard drawing.

For curly or textured hair, preserve the silhouette rhythm without turning the outline into evenly spaced cloud scallops. Use a few uneven, larger contour decisions rather than many identical bumps.

Solid fills are identity anchors, not shading. Default to pure black fills only; use a single pure-color accent only when the user explicitly asks for color. Use fills only for one or two important shapes such as hair, a cap, or a bag.

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

When a style reference is supplied, match its simplification level and line economy more strongly than the model's default idea of polished line art. Do not preserve photographic realism just because it is present in the edit target.

## Visual invariants

Before generation, identify and preserve:

- Number of people
- Relative placement of people
- Crop and framing
- Body pose
- Hand gestures
- Which hand performs each gesture or holds each object
- Which hands are relaxed, hidden, behind the body, or out of frame
- Whether people are touching, not touching, overlapping, or only standing near each other
- Exact arm relationships between neighboring people
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

Do not promote ordinary photographic texture into an invariant. Texture, tiny folds, toe detail, finger detail, hair strands, lip modeling, nose modeling, and most interior garment lines are removable unless they are the only way to preserve identity or gesture.

For group photos, hand and arm relationships are high-priority invariants. Do not make people hold hands, link arms, hug, touch shoulders, or make peace signs unless that exact interaction or gesture appears in the edit target. Do not move a bag, strap, phone, flower, hat, or other object to the wrong hand.

## Pose Map

Before writing the final image prompt, create a concise `Pose Map` from the edit target. Treat it as the source of truth for body structure.

The `Pose Map` should include:

- Subject count and left-to-right order when relevant
- View angle, crop, and body orientation
- Head direction and gaze direction
- Torso angle and weight-bearing stance
- Each visible arm and hand, including uncertain or hidden hands
- Each visible leg and foot, including crouching, kneeling, walking, crossed, hidden, or cropped positions
- Which hand holds each object
- Actual contact or non-contact between people
- Important occlusion relationships

For compact poses, group photos, and layered clothing, extend the `Pose Map` with a short `Layer Map` that names which garment or limb is in front, which is hidden, and which boundary line is required to keep the pose readable.

Copy the `Pose Map` into the image-editing prompt. Do not let the final prompt replace the pose map with a prettier or more generic pose description.

When hand, arm, leg, or contact ownership is ambiguous, simplify that area or hide it inside the body silhouette. Do not invent a clearer gesture, limb, held object, or social interaction to resolve ambiguity.

## Drawing Plan

After the `Pose Map`, create a concise `Drawing Plan` and copy it into the image prompt. This plan is the visual recipe for the final illustration.

The `Drawing Plan` should include:

- `Black fills`: zero to two filled shapes, chosen for composition and identity, not shading
- `Primary contours`: the few broken outline fragments that carry the pose
- `Layer breaks`: the minimum garment or object boundaries required for readability
- `Face symbols`: dots and short lines that communicate direction and expression, not likeness; define the expression with the minimum marks before any generation
- `Intentional omissions`: contours, folds, shadows, textures, and anatomy that should not be drawn

Prefer restarting from the drawing plan over revising a realistic line-art result. If a result looks like a repaired trace, treat it as a wrong approach even when some details are accurate.

## References

Read these files before building or accepting the output:

- [references/style-guide.md](references/style-guide.md)
- [references/prompt-recipes.md](references/prompt-recipes.md)
- [references/quality-checklist.md](references/quality-checklist.md)

Keep detailed style rules, prompt patterns, and acceptance criteria in those references rather than duplicating them here.

If the style reference demonstrates a more reduced visual language than the current text prompt, follow the more reduced visual language.

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
- Pose Map
- Drawing Plan

For edits, repeat the invariants explicitly. Keep structured prompt text in English even when the user speaks another language.

Every prompt should include an explicit simplification stance. State that the result must:

- rebuild the person as a cute, simple, symbol-like figure rather than a realistic portrait
- prefer long outer contours over many short interior lines
- leave intentional gaps in obvious contours
- avoid fully closed outline tracing
- use one or two graphic fills as composition anchors only
- remove nonessential interior detail
- remove light, shadow, volume, and 3D modeling
- avoid layered line buildup
- avoid realistic feature modeling
- preserve expression with dot-and-line facial symbols, not facial likeness
- reduce hands, shoes, and accessories to posture cues unless detail is needed for object ownership
- prefer omission over explanation

When the user provides style references, explicitly say:

- `match the line economy and simplification level of the style references`
- `do not copy page text, arrows, annotations, or layout from the style references`

For group photos, include a per-person pose map before requesting the final drawing. Name each person by position, then state:

- visible hand gesture for each hand
- held object and which hand holds it
- arm position, including relaxed, behind body, crossed, touching another person, or out of frame
- real contact points between people
- relationships that must not be invented

For crouching, kneeling, sitting, or other compact poses, include a body-structure map before requesting the final drawing. State:

- weight-bearing foot or contact point
- bent knee locations
- visible versus hidden leg segments
- arm and hand placement
- held object placement
- body compression caused by the pose

## Generation

Generate one result by default.

- Use image editing rather than unconstrained generation when the supplied people, pose, or composition must be preserved closely.
- Generate multiple variants only when the user explicitly asks for variants.
- Never add visible text unless the user explicitly asks for it.
- If the first result is clean but too descriptive, treat that as a simplification failure rather than a success.
- If the first result looks like realistic line art that has been repaired with fewer details, restart from the `Drawing Plan` rather than polishing the same image.

## Evaluation

Before accepting the result, check:

- Subject count
- Relative placement
- Pose
- Per-person hand and arm position
- Which hand holds each object
- Actual contact or non-contact between neighboring people
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

Treat these as common failure signals even when likeness is good:

- too many facial lines
- eyes, teeth, lips, nose, or beard rendered as likeness detail instead of symbols
- curly hair simplified into an evenly scalloped cloud outline instead of a selective hairstyle silhouette
- too many hair strands
- too many shirt, pants, or shoe detail lines
- readable shirt lettering that should have been abstracted or removed
- contour tracing that follows every photographic edge
- fully connected outlines around heads, arms, torsos, clothes, or bags when broken contours would remain readable
- any shading, shadow, gradient, or volume line used to make the person feel three-dimensional
- iterative repair artifacts: lines that exist because a realistic drawing was cleaned up rather than redesigned
- invented group interactions, such as linked arms, shoulder holds, hugs, or extra peace signs

## Correction policy

Perform at most one targeted correction when there is one clear failure.

- Too detailed: reduce interior lines only.
- Too complete: break nonessential continuous contours and remove closure lines only.
- Too realistic: simplify facial, hand, or material detail only; facial correction should preserve expression and direction, not exact facial likeness.
- Wrong approach: restart from a sparse drawing plan; do not keep repairing the same realistic line-art base.
- Too generic: restore only the missing identity cue.
- Pose drift: restore pose and framing only.
- Hand or contact drift: restore the exact hand, arm, held-object, and contact relationships only.
- Background residue: remove background only.
- Extra object: remove the extra object only.
- Excessive black areas: reduce solid fills only.

For extreme-minimal style references, the default correction should usually be:

- reduce facial marks to the minimum readable cues
- collapse hair into a few large contour decisions
- remove garment graphics unless they are essential identity cues
- remove toe and finger detail unless needed for gesture clarity
- replace descriptive interior lines with one outer contour when possible

If several major constraints fail at once, explain the limitation honestly and ask whether the user wants another iteration instead of restarting with unrelated creative changes.

## Response style

Accept requests in any language and reply in the user's language unless they ask otherwise.

Briefly report:

- Which identity and composition cues were preserved
- Which details were intentionally simplified
- Whether a targeted correction was performed
- Any remaining limitation

Do not expose unnecessary internal implementation details.
