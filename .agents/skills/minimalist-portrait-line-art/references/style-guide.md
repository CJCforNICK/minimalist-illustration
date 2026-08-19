# Style Guide

## Visual identity

Define the output as black-and-white minimalist portrait line art with a modern lifestyle or editorial fashion illustration feel. The result should feel calm, approachable, friendly, understated, hand-drawn, flat, low-density, and recognizable without becoming photorealistic. Simplify rather than exaggerate.

## Drawing logic

The correct output is a symbolic reconstruction, not edge detection, cleaned tracing, a contour-filtered photo, or a repaired realistic line drawing.

The drawing may be intentionally incomplete and graphically flat. Missing contour segments are acceptable when the body, clothing, and gesture remain readable. The viewer should be allowed to complete obvious forms. Do not translate lighting, shadow, volume, or 3D form into lines.

Build the drawing in this order:

- Pose structure: establish head angle, torso direction, limb ownership, weight, gesture, gaze, and contact points
- Body masses: reduce the figure into large readable head, torso, hip, limb, and compressed-pose shapes
- Graphic blocks: choose zero to two flat filled shapes that define the composition, such as hair, a hat, draped jacket, or bag
- Primary contours: choose the few broken outline fragments that describe posture and silhouette
- Layer breaks: add only the hems, openings, cuffs, collars, straps, and overlap breaks needed to separate garments from limbs
- Identity anchors: preserve the few hairstyle, object, expression, posture, or silhouette cues that make the subject recognizable
- Minimal symbols: use tiny facial, hair, hand, and garment marks only after the silhouette reads clearly

When photographic fidelity conflicts with simplified readability, favor simplified readability while preserving the source pose. A continuous outline may be broken when the break clarifies overlap, garment layering, or limb separation.

When completeness conflicts with minimalism, favor minimalism. Keep a contour closed only when closure is needed to identify a limb, garment layer, held object, or important silhouette.

## Line taxonomy

Use lines according to their job:

- Structural lines define pose, weight, direction, and silhouette
- Boundary lines separate important layers such as jacket hem, shorts opening, sleeve cuff, wrist, hand-object contact, or leg edge
- Identity lines preserve hairstyle, expression category, accessory, or a distinctive garment cue
- Decorative or descriptive lines are removed unless they solve one of the jobs above

Composition anchors are not lines: they are rare flat fills that give the image graphic focus. Filled areas should replace many small lines, not add decoration.

## Line behavior

Require:

- Pure black ink lines
- Mostly consistent medium line weight
- Slight organic variation
- Smooth, confident contours
- Selective and intentional breaks in contours
- Open contours and implied continuation
- Fewer closure lines than a conventional clean line-art illustration
- A small set of decisive strokes rather than many corrected strokes
- Lines chosen for structural and identity value
- Removal of redundant photographic edges
- No attempt to trace every visible edge

Avoid:

- Fully closed outline tracing around every body part
- Continuous contour loops used only to make the drawing feel finished
- Polished commercial coloring-book line art
- Lines used as shading, volume, or three-dimensional modeling
- Lines that look like leftover cleanup from a more realistic drawing

## Facial treatment

Require:

- A few symbolic facial marks
- Preservation of face direction and expression
- Eyes, nose, and mouth reduced to dots, short curves, or tiny strokes
- Expression shown through placement and angle of marks, not likeness rendering
- A cute, simple, innocent expression when the source allows it, built from fewer marks rather than softer realism
- Nose reduced to one dot, dash, hook, or short angle; never a modeled bridge or nostril structure
- Facial hair reduced to one abstract cue, tiny fill, or a few short marks only when important
- A jaw or chin contour when useful
- Essential hairline information only

If the source face is obscured by a cap brim, hair, sunglasses, mask, object, motion, low head angle, or crop, preserve the obscuration. Do not add a complete cute face just because the style uses facial symbols. The visible hat brim, shadow edge, head tilt, jaw, chin, ear, or hair mass may be the correct facial information.

Avoid:

- Facial likeness as the main recognition strategy
- Correcting a face by adding more realistic facial information
- Inventing visible eyes, nose, or mouth when the source face is mostly hidden
- Photorealistic skin
- Pores
- Detailed eyelashes
- Eye highlights
- Detailed irises
- Realistic facial shading
- Teeth detail
- Lip modeling
- Nose bridge modeling
- Nostrils as realistic paired details
- Beard or mustache texture
- Shaped mustache or beard drawn as a portrait feature
- Excessive wrinkles
- Exaggerated caricature

## Hair treatment

Require:

- Preservation of the main hairstyle silhouette
- Preservation of bangs, ponytail, bun, tied hair, curls, or headwear when distinctive
- Simplified hair masses
- A few uneven contour choices for curly or textured hair
- No strand-by-strand rendering
- At most one restrained solid-black hair shape when useful

Avoid:

- Evenly repeated cloud scallops around curly hair
- Decorative curl bumps with uniform spacing or size
- Interior curl loops unless one or two are essential identity cues

## Clothing treatment

Require:

- Large, clean clothing shapes
- Preservation of the main garment silhouette
- Preservation of only identity-relevant collars, cuffs, waistlines, pockets, straps, and seams
- Preservation of garment boundaries that prevent layer ambiguity, such as an outer jacket hem, shorts opening, sleeve cuff, or trouser break
- Small contour gaps or short boundary marks where clothing overlaps a limb
- Removal of most folds
- Removal of fabric texture
- Removal of realistic material shading
- No change to the original garment category

For crouching, kneeling, sitting, or compressed poses, make clothing-layer hierarchy readable before adding style. If a jacket covers shorts or a sleeve covers a wrist, use the fewest boundary marks needed so the hidden and visible parts do not merge.

## Hands, feet, and accessories

Require:

- Simplified fingers while preserving the gesture
- Simplified shoes while preserving shoe shape and foot direction
- Preservation of important hats, bags, flowers, glasses, or held objects
- Removal of tiny accessories only when they do not affect recognizability or composition

Hands and shoes should support pose readability, not become small realistic drawings. Use a few rounded finger marks only where hand ownership or a held object would otherwise become unclear.

## Color and fill

Default to:

- Pure black
- Pure white background
- No grayscale modeling
- No gradients
- No cross-hatching
- No colored accents
- No more than one or two restrained solid-black regions

Allow solid-black regions only for visually important areas such as hair, a hat, a bag, or a major clothing shape. Use a single pure-color accent only when the user explicitly requests color; never use color for shading or gradients.

## Background

Default behavior:

- Remove the photographic background
- Place the subject on pure white
- Preserve a background object only when the user explicitly requests it
- Simplify preserved background objects with the same sparse line vocabulary
- Never add decorative scenery

For transparent-background requests:

- Request genuine transparency
- Preserve the alpha channel
- Do not imitate transparency with a checkerboard pattern

## Prohibited output characteristics

Explicitly prohibit:

- Photorealism
- Fully connected coloring-book style outlines
- Grayscale shading
- Gradients
- Cross-hatching
- Dense fabric folds
- Dense hair strands
- Mechanical edge detection
- Tracing every photographic boundary
- Extra people
- Extra limbs
- Extra accessories
- Changed clothing
- Changed pose
- Changed subject count
- Captions
- Labels
- Arrows
- Borders
- Signatures
- Watermarks
- Book pages
- Paper texture
- Checkerboard transparency backgrounds
