# Quality Checklist

Use this checklist before accepting the output.

## Composition checks

Confirm:

- Correct number of people
- Correct relative placement
- Correct crop
- Correct pose
- Correct head direction
- Correct gaze
- Correct hand gestures
- Correct leg position
- Correct subject proportions
- Correct overlap between people and objects

## Recognizability checks

Confirm:

- Hairstyle is preserved
- Face direction is preserved
- Expression is preserved
- Clothing silhouette is preserved
- Important accessories are preserved
- Held objects are preserved
- People remain visually distinguishable in couple and group images

Do not require photorealistic identity reproduction. Evaluate recognizability through a limited set of meaningful cues.

## Minimalism checks

Confirm:

- Most photographic texture has been removed
- Most clothing folds have been removed
- Interior line density is low
- Negative space is generous
- Facial features are symbolic
- Hair is represented as shapes rather than individual strands
- The output remains readable at thumbnail size
- The image does not trace every visible boundary

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
| Too detailed | Interior lines or clothing folds are too dense | Reduce interior lines only | People, pose, crop, accessories, held objects | Revise once |
| Too realistic | Face, hands, or materials look overly rendered | Simplify facial, hand, or material detail only | Composition, hairstyle, clothing silhouette | Revise once |
| Too generic | A key identity cue is missing | Restore one missing cue only | Existing simplification, pose, crop | Revise once |
| Pose drift | Body stance, gesture, or head direction changed | Restore pose and framing only | Style and approved simplification | Revise once |
| Crop drift | Framing moved too far in or out | Restore source crop only | Subject styling and pose | Revise once |
| Missing accessory | Important glasses, hat, bag, flowers, or object missing | Restore the missing item only | Pose, crop, other accepted details | Revise once |
| Background residue | Leftover lines from removed background remain | Remove background residue only | Subject lines and preserved object | Revise once |
| Extra object | New object appears that is not in the source | Remove the extra object only | Real accessories, people, composition | Revise once |
| Excessive black fill | Too many large solid-black areas | Reduce solid-black fill only | Subject silhouette and identity cues | Revise once |
| Incorrect transparency | Transparency request returned a white or fake transparent background | Restore true transparency only | Subject drawing and composition | Revise once |
| Incorrect number of people | A person is missing or added | No narrow fix is reliable | None | Ask the user before another iteration |
