# Prompt Recipes

Use these English prompt shapes as reusable starting points. Keep only the fields that improve clarity for the current request.

## 1. Single-person full-body photo

Use case: Single-person full-body photo
Asset type: Minimalist black-and-white line art illustration
Primary request: Transform the edit target into sparse hand-drawn line art while preserving the person's full-body pose and outfit silhouette.
Input images: Edit target = source photo
Subject invariants: One person, same stance, same body proportions, same head direction, same clothing silhouette, same accessories
Style/medium: Black ink line art only, white background, medium-weight lines, selective broken contours
Composition/framing: Preserve full-body framing and foot direction
Constraints: Preserve recognizability through hairstyle, posture, and clothing shape
Avoid: Grayscale shading, dense folds, extra props, text

## 2. Single-person half-body portrait

Use case: Single-person half-body portrait
Primary request: Reinterpret the portrait as minimal black line art while preserving face direction, expression, hairstyle, and crop.
Input images: Edit target = source portrait
Subject invariants: One person, same crop, same gaze, same hairstyle, same expression
Style/medium: Sparse black ink line drawing, white background, symbolic facial features
Avoid: Realistic skin detail, eye highlights, dense hair strands

## 3. Couple photo

Use case: Couple photo
Primary request: Convert the couple photo into minimalist line art while preserving both people, their relative placement, height difference, and interaction.
Input images: Edit target = couple photo
Subject invariants: Two people, same spacing, same overlap, same pose relationship, same clothing silhouettes
Composition/framing: Preserve crop and the balance between both figures
Constraints: Keep each person visually distinguishable
Avoid: Merging the two people into one silhouette, changing height difference, extra people

## 4. Group photo

Use case: Group photo
Primary request: Convert the group into sparse black-and-white line art while preserving the correct subject count and arrangement.
Input images: Edit target = group photo
Subject invariants: Same number of people, same placement, same overlap, same crop
Constraints: Preserve the key visual cue for each person so the group remains readable
Avoid: Missing people, duplicated limbs, crowd-detail clutter

## 5. Fashion or outfit photo

Use case: Fashion or outfit photo
Primary request: Preserve the overall garment silhouette and styling cues while simplifying the person and removing most fabric detail.
Subject invariants: Same pose, same garment category, same major silhouette, same key seams, straps, cuffs, and waistlines
Style/medium: Editorial-feeling minimalist line art
Avoid: Fabric texture, photorealistic folds, changing the clothing type

## 6. Person holding an important object

Use case: Person holding an important object
Primary request: Preserve both the person and the held object in sparse line art.
Subject invariants: Same pose, same hand gesture, same object identity, same object placement
Constraints: Simplify fingers but keep the gesture readable
Avoid: Dropping the object, replacing the object, inventing extra props

## 7. Person against a complex background

Use case: Person against a complex background
Primary request: Remove the photographic background and isolate the person on white while preserving pose and identity cues.
Constraints: Background should be removed completely unless the user explicitly requests one element to remain
Avoid: Background residue, decorative scenery, texture clutter

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
Avoid: Adding scenery, over-rendering the object

## 10. Reducing excessive line detail

Use case: Correction for excessive line detail
Primary request: Reduce interior line density and remove nonessential contour fragments.
Change only: Interior detail level
Keep unchanged: Subject count, pose, crop, hairstyle, clothing silhouette, accessories, held objects
Avoid: Changing composition, identity cues, or object placement

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
