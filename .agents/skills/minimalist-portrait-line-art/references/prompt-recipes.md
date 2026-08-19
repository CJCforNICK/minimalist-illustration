# Prompt Recipes

Use these English prompt shapes as reusable starting points. Keep only the fields that improve clarity for the current request.

Across all recipes, default to these simplification priorities unless the user explicitly asks otherwise:

- Prefer omission over explanation
- Prefer outer contours over interior lines
- Prefer open, broken, incomplete contours over fully closed outlines
- Prefer one identity cue over many descriptive details
- Prefer expression and face direction over facial likeness
- Prefer abstract garment shapes over realistic garment information
- Prefer flat graphic shape readability over volume or depth
- Prefer unreadable abstract shirt graphics over literal lettering
- Prefer a single solid-black accent over multiple filled regions

Also include this drawing-logic block when pose, clothing layers, hands, or compact body structure matter:

Drawing logic:
- Reconstruct the person from an abstract drawing plan, not from photo edge tracing or a repaired realistic line drawing.
- Establish the pose skeleton first, then large body masses, then graphic fills, then primary contour fragments, then clothing-layer boundaries, then identity symbols.
- Use only structural lines, essential boundary lines, and identity lines.
- Treat the face as expression symbols: dots and short strokes for eyes, nose, and mouth, not realistic likeness.
- If the source face is mostly hidden, preserve the obscuration and do not invent a complete symbolic face.
- For curly or textured hair, use a few uneven silhouette decisions, not evenly repeated cloud scallops.
- Preserve boundary breaks that keep garments and limbs readable.
- Leave nonessential contours open; let the viewer complete obvious body, garment, and object shapes.
- Remove decorative, descriptive, texture, shading, volume, depth, and edge-detection lines.
- If an unclear hand, limb, or clothing layer cannot be verified from the source, simplify it into the silhouette instead of inventing a clearer detail.

Drawing Plan:
- Black fills: [zero to two flat filled shapes; explain why each is an anchor]
- Primary contours: [few broken outline fragments that carry the pose]
- Layer breaks: [minimum garment/object boundaries needed for readability]
- Face symbols: [dots and short strokes only]
- Intentional omissions: [specific contours, folds, shadows, textures, and anatomy not to draw]

Successful simplification pattern:
- Preserve source structure through pose, gaze, crop, hairstyle category, clothing silhouette, and object ownership.
- Rebuild the person as a cute, simple, symbol-like figure, not as a faithful face drawing.
- Make the face with the fewest readable marks: one dot or dash eye, one tiny dash/dot/hook nose, and one small mouth curve when needed.
- If the face is obscured, use the obscuring brim, hair, sunglasses, mask, object, angle, or crop as the face cue instead of adding eyes, nose, and mouth.
- Treat hands as gesture symbols: a few rounded marks that show holding, pointing, peace sign, or relaxed position, not anatomical fingers.
- Treat shoes and accessories as silhouette cues unless they are the main identity anchor.
- Use one or two black fills as graphic anchors, not as shadows or material rendering.
- Remove closure lines where the viewer can infer the form, but keep the minimum layer breaks that prevent garments, limbs, and objects from merging.

## 1. Single-person full-body photo

Use case: Single-person full-body photo
Asset type: Minimalist black-and-white line art illustration
Primary request: Transform the edit target into sparse hand-drawn line art while preserving the person's full-body pose and outfit silhouette.
Input images: Edit target = source photo
Subject invariants: One person, same stance, same body proportions, same head direction, same clothing silhouette, same accessories
Style/medium: Flat black ink line art only, white background, medium-weight lines, selective broken contours
Composition/framing: Preserve full-body framing and foot direction
Constraints: Preserve recognizability through hairstyle, posture, and clothing shape
Avoid: Grayscale shading, shadows, volume modeling, dense folds, extra props, text, toe detail, descriptive shoe detail, layered contour buildup, fully closed coloring-book outlines

## 2. Single-person half-body portrait

Use case: Single-person half-body portrait
Primary request: Reinterpret the portrait as minimal black line art while preserving face direction, expression, hairstyle, and crop.
Input images: Edit target = source portrait
Subject invariants: One person, same crop, same gaze, same hairstyle, same expression
Style/medium: Flat sparse black ink line drawing, white background, symbolic facial features
Constraints: Keep only the fewest facial marks needed for face direction and expression. Do not pursue eye, nose, mouth, or tooth likeness.
Avoid: Realistic skin detail, eye highlights, detailed irises, teeth detail, dense hair strands, lip modeling, nose modeling, beard texture, shadows, cheek volume, layered line buildup

## 3. Couple photo

Use case: Couple photo
Primary request: Convert the couple photo into minimalist line art while preserving both people, their relative placement, height difference, and interaction.
Input images: Edit target = couple photo
Subject invariants: Two people, same spacing, same overlap, same pose relationship, same clothing silhouettes
Composition/framing: Preserve crop and the balance between both figures
Constraints: Keep each person visually distinguishable
Avoid: Merging the two people into one silhouette, changing height difference, extra people, extra contour fragments used only for decoration

## 4. Group photo

Use case: Group photo
Primary request: Convert the group into sparse black-and-white line art while preserving the correct subject count and arrangement.
Input images: Edit target = group photo
Subject invariants: Same number of people, same placement, same overlap, same crop
Per-person pose map: Name each person from left to right and specify each visible hand, arm position, held object, and real contact point.
Constraints: Preserve the key visual cue for each person so the group remains readable. Preserve hand ownership exactly: do not swap gestures or held objects between hands or people.
Avoid: Missing people, duplicated limbs, crowd-detail clutter, over-describing each person with separate texture lines, invented hugs, linked arms, shoulder touches, extra peace signs, or moved bags

For group photos, include language like:

Person 1: [left/right hand status], [arm position], [held object and hand], [contact or no contact].
Person 2: [left/right hand status], [arm position], [held object and hand], [contact or no contact].
Person 3: [left/right hand status], [arm position], [held object and hand], [contact or no contact].
Person 4: [left/right hand status], [arm position], [held object and hand], [contact or no contact].

Do not invent warmer social interaction. If two people are only standing near each other, keep them only standing near each other.

## 5. Fashion or outfit photo

Use case: Fashion or outfit photo
Primary request: Preserve the overall garment silhouette and styling cues while simplifying the person and removing most fabric detail.
Subject invariants: Same pose, same garment category, same major silhouette, same key seams, straps, cuffs, and waistlines
Style/medium: Editorial-feeling minimalist line art
Constraints: Preserve silhouette and only one or two structural garment cues
Avoid: Fabric texture, photorealistic folds, changing the clothing type, readable logos, descriptive seam overload

## 6. Person holding an important object

Use case: Person holding an important object
Primary request: Preserve both the person and the held object in sparse line art.
Subject invariants: Same pose, same hand gesture, same object identity, same object placement
Constraints: Simplify fingers but keep the gesture readable
Avoid: Dropping the object, replacing the object, inventing extra props, rendering finger joints or object texture in detail

## 6a. Single-person crouching or compact pose

Use case: Single-person crouching or compact pose
Asset type: Minimalist black-and-white line-art reinterpretation
Primary request: Convert the source photo into ultra-minimal line art while preserving the compact pose structure.
Input images: Edit target = source photo
Pose Map: Describe torso angle, head direction, weight-bearing foot, bent knees, visible and hidden leg segments, each arm, each hand, held objects, and occlusions before writing the final request.
Layer Map: Describe outer garment hem, shorts/skirt/trouser opening, sleeve cuff, visible leg edge, hidden leg area, bag or strap overlap, and the minimum boundary breaks required for readability.
Subject invariants: One person, same crouching or kneeling structure, same head direction, same gaze, same clothing silhouette, same key accessory or held object
Style/medium: Pure black line art, pure white background, very low line density, long outer contours, symbolic facial marks
Constraints: Preserve body compression and limb ownership exactly. Keep the garment-layer hierarchy readable with the fewest possible lines. If a hand, foot, leg segment, or clothing edge is ambiguous, simplify it or hide it in the silhouette instead of inventing a clearer limb.
Avoid: Standing the subject up, changing the crouch, adding missing feet, inventing fingers, merging jacket with shorts or shorts with legs, over-rendering shoes, realistic facial modeling, dense clothing folds

## 7. Person against a complex background

Use case: Person against a complex background
Primary request: Remove the photographic background and isolate the person on white while preserving pose and identity cues.
Constraints: Background should be removed completely unless the user explicitly requests one element to remain
Avoid: Background residue, decorative scenery, texture clutter, replacing removed background with filler lines

## 8. Transparent-background output

Use case: Transparent-background output
Asset type: Minimalist portrait line art with true alpha transparency
Primary request: Create clean black line art and keep the background genuinely transparent.
Constraints: Preserve alpha channel and subject silhouette
Avoid: White fill background, checkerboard fake transparency, background residue

## 9. Preserving one requested environmental object

Use case: Preserve one environmental object
Primary request: Keep the requested object and simplify it with the same sparse line vocabulary while removing the rest of the background.
Subject invariants: Same person or people, same object identity, same relative position between subject and object
Change only: Preserve the requested object; remove unrelated background
Avoid: Adding scenery, over-rendering the object, adding explanatory background contours

## 10. Reducing excessive line detail

Use case: Correction for excessive line detail
Primary request: Reduce interior line density and remove nonessential contour fragments.
Change only: Interior detail level
Keep unchanged: Subject count, pose, crop, hairstyle, clothing silhouette, accessories, held objects
Avoid: Changing composition, identity cues, or object placement

Use these extra instructions when the first result still feels too polished or descriptive:

- remove most face detail and keep only minimal symbolic marks
- replace realistic eyes, teeth, lips, nose, nostrils, and beard texture with dots and short strokes
- reduce nose to one dot, dash, hook, or short angle
- reduce mustache or beard to one abstract cue only
- remove most hair strands and keep only major silhouette decisions
- break up evenly scalloped cloud hair into fewer, uneven contour choices
- remove shirt graphics unless they are required as abstract shape cues
- remove toe and finger detail unless needed for gesture clarity
- collapse multiple descriptive lines into one longer contour when possible

If the first result invents unclear anatomy, do not add detail to explain it. Instead, collapse the uncertain area into a simpler silhouette while preserving the visible pose.

## 10a. Rebuilding from symbolic drawing logic

Use case: Correction when the result looks like traced photo line art, repaired line art, or a minimalized realistic drawing
Primary request: Restart the illustration from the Pose Map and Drawing Plan using sparse symbolic construction.
Change only: Drawing approach, line economy, contour completeness, and simplification level
Keep unchanged: Subject count, pose, crop, hand ownership, contact relationships, hairstyle silhouette, clothing categories, accessories, and held objects
Required structure: Pose skeleton first, large body masses second, graphic fills third, primary contour fragments fourth, clothing-layer boundaries fifth, tiny identity symbols last
Avoid: Preserving the old realistic line-art base, edge-detection contours, realistic face modeling, fabric folds, descriptive interior lines, or adding extra detail to explain ambiguous areas

Use this when the drawing is accurate in content but visually behaves like a cleaned or repaired tracing instead of a designed minimalist figure.

## 10d. Correcting over-complete contours

Use case: Correction when the drawing is too complete, connected, three-dimensional, or coloring-book-like
Primary request: Remove nonessential closure lines, volume lines, and introduce intentional contour gaps while preserving readability.
Change only: Contour completeness, volume cues, and unnecessary connection lines
Keep unchanged: Subject count, pose, crop, hand ownership, clothing-layer boundaries, hairstyle category, accessories, and held objects
Required approach: Keep structural anchor lines, contact points, key garment boundaries, and object ownership; break or omit obvious contour segments that the viewer can infer
Avoid: Breaking lines that would confuse pose, limb ownership, hand gestures, garment layer separation, or held objects

Use this when the output has acceptable pose and simplification but still feels too polished, finished, dimensional, or fully outlined.

## 10b. Correcting facial over-likeness

Use case: Correction when the face is recognizable through realistic features instead of symbol-like expression marks
Primary request: Replace facial likeness detail with a few symbolic marks while preserving face direction and expression category.
Change only: Facial detail level
Keep unchanged: Pose, crop, head direction, hairstyle silhouette, glasses or facial-hair category if present, clothing silhouette, accessories, held objects, and line economy
Allowed marks: Dot eyes, tiny brow strokes, one dot/dash/hook nose mark, one simple mouth curve, and one minimal abstract beard or mustache cue only if important
Avoid: Detailed irises, eyelids, eyelashes, teeth, lip shape, nose bridge, nostril structure, cheek modeling, beard texture, shaped mustache drawing, skin detail, realistic smile rendering, or caricature

Use this when the body and objects are acceptable but the face still looks like a portrait likeness.

When the requested direction is cuter or simpler, use this phrasing:

Revise the face as symbolic marks only. Keep the same head angle and expression category, but do not draw a realistic face. Use one tiny dot or short dash for the eye, one tiny dash/dot/hook for the nose, and one small soft mouth curve if needed. Remove realistic lips, nostrils, eyelids, cheek modeling, facial planes, smile anatomy, and portrait likeness construction. The expression should read as simple, friendly, and innocent through mark placement, not through detailed features.

## 10e. Correcting invented visible face

Use case: Correction when the source face is hidden or barely visible but the result invents a complete face
Primary request: Preserve the original face obscuration instead of adding a full symbolic expression.
Change only: Face visibility, headwear/occluder relationship, and unnecessary facial marks
Keep unchanged: Pose, crop, head angle, clothing silhouette, hands, held objects, accessories, and line economy
Allowed marks: Cap brim, hair edge, mask edge, sunglasses shape, jaw edge, chin curve, ear, one partial lower-face mark, or no facial marks
Avoid: Full dot-eye pairs, complete eyes-nose-mouth expression, realistic face, cute cheeks, visible smile anatomy, or changing the head angle to reveal the face

Use this when a good minimalist result incorrectly makes the person look at the viewer or shows a full face that the source did not reveal.

## 10c. Correcting cloud-like curly hair

Use case: Correction when curly or textured hair becomes an evenly scalloped cartoon cloud
Primary request: Preserve the hairstyle silhouette with fewer, larger, uneven contour decisions.
Change only: Hair outline simplification
Keep unchanged: Head size, face direction, expression marks, pose, crop, clothing silhouette, accessories, and held objects
Allowed marks: A simple hair mass outline with a few irregular bumps, one or two directional breaks, or one restrained fill if needed
Avoid: Uniform cloud scallops, repeated curl bumps, many interior curl loops, hair strands, or changing the hairstyle category

Use this when the output is minimal but the hair silhouette feels too decorative or generic.

## 11. Restoring missing identity cues

Use case: Correction for missing identity cues
Primary request: Restore the single missing identity cue that improves recognizability.
Change only: The missing cue, such as hairstyle shape, glasses, or a key collar
Keep unchanged: Existing pose, crop, line economy, and all other accepted elements
Avoid: Adding new creative details or increasing overall complexity

## 12. Correcting pose or composition drift

Use case: Correction for pose or composition drift
Primary request: Restore the original pose, framing, and relative placement from the source image.
Change only: Pose, crop, or placement drift
Keep unchanged: Style, simplification level, preserved accessories, and approved background treatment
Avoid: Re-styling the image or altering identity details unnecessarily

For compact poses, correct the body structure first: torso angle, bent knees, weight-bearing foot, hidden limbs, and hand positions. Do not convert a crouch into a standing or seated pose.

## 12a. Correcting group hand or contact drift

Use case: Correction for group hand, arm, or contact drift
Primary request: Restore the exact original hand positions, arm positions, held-object ownership, and contact relationships from the source image.
Change only: Hand gestures, arm placement, held-object ownership, and person-to-person contact drift
Keep unchanged: Subject count, left-to-right order, crop, style, line economy, hairstyle silhouettes, clothing silhouettes, and background treatment
Avoid: Inventing friendliness, linked arms, hugs, shoulder holds, extra peace signs, swapped bags, swapped held objects, or new gestures

Use this when the drawing is stylistically acceptable but the group interaction is wrong.

## 12b. Correcting garment-layer ambiguity

Use case: Correction when clothing layers, hidden limbs, or exposed limbs merge together
Primary request: Restore only the missing garment and limb boundary needed for readability.
Change only: The minimal jacket hem, shorts opening, skirt edge, trouser break, sleeve cuff, wrist gap, visible leg edge, or overlap break
Keep unchanged: Subject count, pose, crop, face direction, expression, hairstyle silhouette, accessory placement, held objects, and overall line economy
Avoid: Adding fabric texture, folds, shading, new seams, new clothing, extra limbs, or unrelated contour detail

Use this when the pose is correct but a jacket merges into shorts, shorts disappear into legs, a sleeve merges into a hand, or an object merges into the body.

## 13. Removing unwanted background residue

Use case: Correction for background residue
Primary request: Remove leftover background marks and keep only the subject on white or transparent background as requested.
Change only: Background residue
Keep unchanged: Subject lines, pose, crop, and preserved object if requested
Avoid: Editing the subject silhouette beyond what is required for cleanup

## 14. Removing an extra generated object

Use case: Correction for extra object
Primary request: Remove the extra object that was not present in the source.
Change only: The extra object
Keep unchanged: People, pose, crop, clothing silhouette, legitimate accessories, and held objects
Avoid: Removing real accessories or changing composition

## 15. Reducing excessive solid-black fill

Use case: Correction for excessive solid-black fill
Primary request: Reduce solid-black regions so the result returns to sparse line art with at most one or two restrained accent fills.
Change only: Solid-black fill amount
Keep unchanged: Subject count, pose, hairstyle silhouette, and garment silhouette
Avoid: Reintroducing texture or adding shading

## 16. Ultra-minimal style-reference conversion

Use case: Edit target plus explicit ultra-minimal style references
Asset type: Minimalist black-and-white line-art reinterpretation
Primary request: Convert the edit target into a drawing that matches the line economy and simplification level of the supplied style references.
Input images: Edit target = source photo; Style reference = provided minimal line drawings
Subject invariants: Preserve people, pose, crop, hairstyle silhouette, major clothing silhouette, key accessories, and held objects
Style/medium: Pure black lines, pure white background, very low line density, long outer contours, tiny symbolic facial marks, one optional solid-black accent
Constraints: Match the reduction level of the style references more strongly than the photographic detail of the source image
Keep unchanged: Subject count, pose, framing, and key identity cues
Avoid: Copying text, arrows, annotations, page borders, layout, book graphics, realistic feature modeling, dense interior detail, decorative filler lines
