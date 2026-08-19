# Quality Checklist

Use this checklist before accepting the output.

## Drawing logic checks

Confirm:

- The image reads as a symbolic reconstruction, not a traced or edge-detected photo
- The image looks planned as a minimal illustration, not repaired from a realistic line drawing
- Pose structure is clear before decorative detail appears
- Large body masses are readable
- One or two graphic fills replace detail instead of adding decoration
- Clothing-layer hierarchy is readable
- Forms read as flat graphic shapes, not shaded three-dimensional volumes
- Obvious forms can be incomplete without losing readability
- Necessary hems, openings, cuffs, straps, and overlap breaks are present when they prevent visual merging
- Gaps and broken contours clarify overlap rather than creating accidental missing anatomy
- Solid-black fills act as identity anchors, not shading
- Ambiguous hands, limbs, or garment edges are simplified instead of invented

## Composition checks

Confirm:

- Correct number of people
- Correct relative placement
- Correct crop
- Correct pose
- Correct head direction
- Correct gaze
- Correct face visibility, including hidden or barely visible faces
- Correct hand gestures
- Correct hand ownership for each gesture
- Correct held-object ownership and hand placement
- Correct arm positions, including arms behind the body, relaxed arms, crossed arms, and out-of-frame arms
- Correct contact relationships between people
- No invented touch, linked arms, hugs, shoulder holds, or extra peace signs
- Correct leg position
- Correct compact-pose structure for crouching, kneeling, sitting, or compressed poses
- Correct visible versus hidden limb segments
- No invented limbs used to clarify ambiguous anatomy
- Correct subject proportions
- Correct overlap between people and objects

## Recognizability checks

Confirm:

- Hairstyle is preserved
- Face direction is preserved
- Expression is preserved
- Clothing silhouette is preserved
- Garment category and layer order are preserved
- Important accessories are preserved
- Held objects are preserved
- People remain visually distinguishable in couple and group images

Do not require photorealistic identity reproduction. Evaluate recognizability through a limited set of meaningful cues.

## Minimalism checks

Confirm:

- Most photographic texture has been removed
- Most clothing folds have been removed
- Light, shadow, and volume cues have been removed
- Interior line density is low
- Negative space is generous
- Nonessential contours are left open or omitted
- The result could be redrawn from memory as a small set of strokes and fills
- Facial features are symbolic
- The face reads as a simple expression symbol, not a portrait study
- Cuteness or friendliness comes from fewer marks and softer placement, not from realistic eyes, lips, cheeks, or smile anatomy
- Hair is represented as shapes rather than individual strands
- Facial recognition is not based on realistic eyes, teeth, lips, nose, or beard texture
- Face direction and expression remain readable through a few marks
- Hidden faces remain hidden; the drawing does not invent a full expression when the source face is obscured
- Nose and facial hair are symbolic cues, not modeled portrait features
- Curly or textured hair is not simplified into evenly repeated cloud scallops
- The output remains readable at thumbnail size
- The image does not trace every visible boundary
- The image does not look like fully outlined coloring-book art

## Style checks

Confirm:

- Pure black lines
- Pure white or genuinely transparent background
- Mostly consistent medium line weight
- Slight hand-drawn character
- Intentional contour breaks
- No more than two solid-black accent regions
- Calm and uncluttered appearance

## Prohibited-element checks

Check for:

- Grayscale shading
- Gradients
- Cross-hatching
- Dense texture
- Extra people
- Extra limbs
- Extra objects
- Changed clothing
- Changed pose
- Text
- Captions
- Arrows
- Borders
- Watermarks
- Signatures
- Book-page remnants
- Paper texture
- Fake transparency

## Correction decision table

| Failure | Failure signal | Allowed correction | Must remain unchanged | Action |
| --- | --- | --- | --- | --- |
| Wrong drawing logic | Output looks like cleaned tracing, edge detection, repaired line art, or descriptive line art instead of symbolic reconstruction | Restart from Pose Map and Drawing Plan: pose skeleton, body masses, graphic fills, primary contour fragments, layer breaks, and minimal symbols | Subject count, pose, crop, hand ownership, contact relationships, clothing categories, accessories | Revise once |
| No drawing plan | Output contains many locally correct details but lacks a simple graphic composition | Rebuild around one or two fills, a few primary contour fragments, and intentional omissions | Subject count, pose, crop, key accessories, held objects | Revise once |
| Too detailed | Interior lines or clothing folds are too dense | Reduce interior lines only | People, pose, crop, accessories, held objects | Revise once |
| Over-complete contours | Outlines around head, torso, arms, clothes, bags, or objects are too continuously connected and coloring-book-like | Remove closure lines and add intentional gaps only where forms remain obvious | Subject count, pose, hand ownership, garment-layer clarity, accessories, held objects | Revise once |
| Too dimensional | Shadows, volume lines, wrinkles, or contour modeling make the figure feel three-dimensional | Remove depth, shading, and modeling cues only | Subject count, pose, silhouette, clothing layers, accessories, held objects | Revise once |
| Too realistic | Face, hands, or materials look overly rendered | Simplify facial, hand, or material detail only | Composition, hairstyle, clothing silhouette | Revise once |
| Facial over-likeness | Eyes, teeth, lips, nose, beard, or skin are modeled like a portrait likeness | Replace facial detail with dot-and-line expression symbols only | Pose, crop, head direction, expression category, hairstyle silhouette, accessories | Revise once |
| Cute style drift | The result becomes cute by adding chibi proportions, decorative eyes, cheeks, or extra expression detail | Reduce cuteness to simple mark placement and preserve original proportions | Pose, crop, body proportions, clothing silhouette, accessories | Revise once |
| Invented visible face | Source face is hidden by brim, hair, sunglasses, mask, object, angle, motion, or crop, but output adds a complete visible face | Restore the obscuring element and remove unnecessary facial symbols | Pose, crop, head angle, clothing silhouette, hands, accessories, held objects | Revise once |
| Nose or beard modeling | Nose has bridge/nostril structure, or mustache/beard is drawn as a shaped portrait feature | Reduce nose to one dot, dash, hook, or short angle; reduce facial hair to one abstract cue | Pose, crop, expression category, hairstyle silhouette, clothing, accessories | Revise once |
| Cloud-like curly hair | Curly hair becomes an evenly scalloped cartoon cloud or repeated decorative bumps | Replace with fewer, larger, uneven silhouette decisions | Head size, face direction, expression marks, hairstyle category, pose, crop | Revise once |
| Too generic | A key identity cue is missing | Restore one missing cue only | Existing simplification, pose, crop | Revise once |
| Pose drift | Body stance, gesture, or head direction changed | Restore pose and framing only | Style and approved simplification | Revise once |
| Hand or contact drift | A gesture moves to the wrong hand, an object moves to the wrong hand, or people touch when they should not | Restore exact hand, arm, object, and contact relationships only | Subject count, order, crop, style, line economy, clothing silhouettes | Revise once |
| Compact-pose drift | A crouch, kneel, sit, or compressed pose becomes standing, generic seated, or anatomically clarified with invented limbs | Restore compact pose structure only | Subject count, crop, style, line economy, clothing silhouette, key accessories | Revise once |
| Garment-layer ambiguity | Jacket merges with shorts, shorts disappear into legs, sleeve merges with hand, or object merges into body | Add or restore only the minimum hem, opening, cuff, wrist gap, visible limb edge, or overlap break | Pose, crop, identity anchors, garment categories, overall line economy | Revise once |
| Crop drift | Framing moved too far in or out | Restore source crop only | Subject styling and pose | Revise once |
| Missing accessory | Important glasses, hat, bag, flowers, or object missing | Restore the missing item only | Pose, crop, other accepted details | Revise once |
| Background residue | Leftover lines from removed background remain | Remove background residue only | Subject lines and preserved object | Revise once |
| Extra object | New object appears that is not in the source | Remove the extra object only | Real accessories, people, composition | Revise once |
| Excessive black fill | Too many large solid-black areas | Reduce solid-black fill only | Subject silhouette and identity cues | Revise once |
| Incorrect transparency | Transparency request returned a white or fake transparent background | Restore true transparency only | Subject drawing and composition | Revise once |
| Incorrect number of people | A person is missing or added | No narrow fix is reliable | None | Ask the user before another iteration |
