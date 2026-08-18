# Test Cases

Do not execute these tests yet. Use owned, licensed, consented, or freely reusable source images only.

## T01

- Test ID: T01
- Scenario: Single-person half-body portrait
- Input characteristics: One person, chest-up framing, clear face direction, visible hairstyle
- Example user request: "Use $minimalist-portrait-line-art to turn this portrait photo into clean black-and-white minimal line art."
- Must preserve: Crop, face direction, hairstyle, expression
- Must simplify: Skin detail, small wrinkles, background
- Must avoid: Grayscale shading, text, mechanical tracing
- Expected behavior: Produce one sparse portrait result with symbolic facial marks
- Pass criteria: The person remains recognizable through face direction, hair, and expression

## T02

- Test ID: T02
- Scenario: Single-person full-body walking pose
- Input characteristics: One person walking, both legs visible, full-body crop
- Example user request: "Use $minimalist-portrait-line-art to turn this full-body walking photo into minimal black line art and remove the background."
- Must preserve: Walking stance, leg position, body proportions, crop
- Must simplify: Clothing folds, ground detail
- Must avoid: Pose drift, extra limbs
- Expected behavior: Preserve the walking gesture with sparse line economy
- Pass criteria: The stance and foot direction still read correctly

## T03

- Test ID: T03
- Scenario: Person holding a hat
- Input characteristics: One person holding a hat near the torso
- Example user request: "Use $minimalist-portrait-line-art and keep the hat in the person's hand."
- Must preserve: Hand gesture, hat shape, object placement
- Must simplify: Finger detail, background
- Must avoid: Dropping or changing the hat
- Expected behavior: The hat remains clearly identifiable without over-detailing
- Pass criteria: The held hat is present and readable

## T04

- Test ID: T04
- Scenario: Person holding flowers
- Input characteristics: One person holding a bouquet
- Example user request: "使用 $minimalist-portrait-line-art，使用透明背景，並保留人物手中的花束。"
- Must preserve: Bouquet presence, hand gesture, pose
- Must simplify: Petal detail, finger detail, background
- Must avoid: Replacing bouquet with a generic object
- Expected behavior: Preserve bouquet silhouette with sparse detailing
- Pass criteria: Bouquet and gesture are both recognizable

## T05

- Test ID: T05
- Scenario: Fashion photo with wide clothing silhouette
- Input characteristics: One person wearing a coat or dress with a strong silhouette
- Example user request: "Use $minimalist-portrait-line-art to preserve the outfit silhouette and simplify everything else."
- Must preserve: Garment silhouette, key seams, straps, cuffs, waistline
- Must simplify: Fabric texture, folds, realistic shading
- Must avoid: Changing clothing category
- Expected behavior: Editorial-feeling line art with clear garment shape
- Pass criteria: Outfit silhouette remains the strongest cue

## T06

- Test ID: T06
- Scenario: Couple with height difference
- Input characteristics: Two people standing close together with visible height difference
- Example user request: "使用 $minimalist-portrait-line-art，保留兩個人的身高差、姿勢和服裝輪廓，移除背景。"
- Must preserve: Subject count, height difference, spacing, pose relationship
- Must simplify: Facial detail, minor clothing texture
- Must avoid: Merging the two figures
- Expected behavior: Both people remain distinguishable and correctly proportioned
- Pass criteria: Height difference and relationship remain clear

## T07

- Test ID: T07
- Scenario: Two people overlapping
- Input characteristics: Couple or friends with overlapping shoulders or arms
- Example user request: "Use $minimalist-portrait-line-art and preserve the overlap between both people."
- Must preserve: Overlap order, subject count, relative placement
- Must simplify: Interior clothing detail
- Must avoid: Broken occlusion logic
- Expected behavior: Overlap remains readable with sparse contours
- Pass criteria: Front and back figure relationships are still clear

## T08

- Test ID: T08
- Scenario: Group of three or more people
- Input characteristics: Three or more subjects with distinct relative positions
- Example user request: "Use $minimalist-portrait-line-art to turn this group photo into minimalist black line art."
- Must preserve: Subject count, arrangement, major cues for each person
- Must simplify: Background, minor features
- Must avoid: Missing or duplicated people
- Expected behavior: Group remains legible without dense clutter
- Pass criteria: Every person is still accounted for

## T09

- Test ID: T09
- Scenario: Complex indoor background
- Input characteristics: Person indoors with furniture, shelves, or decor behind them
- Example user request: "Use $minimalist-portrait-line-art and remove the indoor background completely."
- Must preserve: Person, pose, clothing silhouette
- Must simplify: Entire background
- Must avoid: Background residue
- Expected behavior: Subject isolated cleanly on white
- Pass criteria: No irrelevant indoor lines remain

## T10

- Test ID: T10
- Scenario: Complex outdoor background
- Input characteristics: Person outdoors with trees, buildings, or street detail
- Example user request: "Use $minimalist-portrait-line-art to isolate the person and remove the outdoor background."
- Must preserve: Person, pose, proportions
- Must simplify: Outdoor environment
- Must avoid: Decorative scenery
- Expected behavior: Clean subject-only result
- Pass criteria: Background is removed without harming the subject silhouette

## T11

- Test ID: T11
- Scenario: Transparent-background request
- Input characteristics: One person with clear silhouette
- Example user request: "Use $minimalist-portrait-line-art with a transparent background."
- Must preserve: Subject lines, silhouette, crop
- Must simplify: Background
- Must avoid: Fake transparency, checkerboard pattern
- Expected behavior: True transparent output
- Pass criteria: Background is genuinely transparent

## T12

- Test ID: T12
- Scenario: Preserve one chair or environmental object
- Input characteristics: Person seated with one chair the user wants kept
- Example user request: "Use $minimalist-portrait-line-art and preserve the chair, but remove the rest of the background."
- Must preserve: Person, chair identity, relative placement
- Must simplify: Other background elements
- Must avoid: Adding extra scenery
- Expected behavior: Only the requested chair remains, simplified
- Pass criteria: Chair is present and the rest of the background is removed

## T13

- Test ID: T13
- Scenario: Person wearing glasses
- Input characteristics: One person with glasses that affect recognizability
- Example user request: "Use $minimalist-portrait-line-art and keep the glasses as a key identity cue."
- Must preserve: Glasses shape and placement, face direction
- Must simplify: Lens detail, skin detail
- Must avoid: Omitting glasses
- Expected behavior: Glasses remain visible with minimal lines
- Pass criteria: The glasses help preserve identity

## T14

- Test ID: T14
- Scenario: Person with distinctive tied hair
- Input characteristics: Ponytail, bun, or tied hairstyle
- Example user request: "使用 $minimalist-portrait-line-art，把這張人物照片轉換成黑白極簡人物線稿。"
- Must preserve: Hair silhouette, tied-hair structure, face direction
- Must simplify: Individual strands
- Must avoid: Generic short-hair substitution
- Expected behavior: Hairstyle remains a clear identity cue
- Pass criteria: Tied-hair silhouette is clearly retained

## T15

- Test ID: T15
- Scenario: Source image with partially hidden hands
- Input characteristics: Hands partially occluded by clothing or objects
- Example user request: "Use $minimalist-portrait-line-art and keep the existing hand visibility exactly as in the photo."
- Must preserve: Occlusion logic, gesture implication
- Must simplify: Finger detail
- Must avoid: Inventing missing fingers
- Expected behavior: Hands stay simplified without invented anatomy
- Pass criteria: Hidden parts remain hidden

## T16

- Test ID: T16
- Scenario: Source image with partially hidden legs
- Input characteristics: Legs partly hidden behind an object or other person
- Example user request: "Use $minimalist-portrait-line-art and preserve the leg occlusion exactly."
- Must preserve: Leg visibility, stance, overlap
- Must simplify: Fabric detail
- Must avoid: Adding a full extra leg
- Expected behavior: Occlusion remains consistent with the source
- Pass criteria: No invented lower-body anatomy appears

## T17

- Test ID: T17
- Scenario: Result that is too detailed
- Input characteristics: Initial output has too many interior lines
- Example user request: "Use $minimalist-portrait-line-art and reduce interior lines only."
- Must preserve: Pose, crop, hairstyle, clothing silhouette
- Must simplify: Interior details only
- Must avoid: Reframing or identity drift
- Expected behavior: One targeted correction reduces line density
- Pass criteria: Detail drops while pose and identity cues remain stable

## T18

- Test ID: T18
- Scenario: Result that loses identity cues
- Input characteristics: Initial output misses glasses, bangs, or a key collar
- Example user request: "Use $minimalist-portrait-line-art and restore the missing identity cue only."
- Must preserve: Existing accepted composition and simplicity
- Must simplify: Nothing beyond the original accepted simplification
- Must avoid: Adding unrelated new detail
- Expected behavior: One targeted correction restores only the missing cue
- Pass criteria: Recognizability improves without broader restyling

## T19

- Test ID: T19
- Scenario: Result with pose drift
- Input characteristics: Initial output changes gesture or crop
- Example user request: "Use $minimalist-portrait-line-art and restore the original pose and framing only."
- Must preserve: Accepted style and identity cues
- Must simplify: No new simplification pass
- Must avoid: New creative changes
- Expected behavior: One targeted correction restores the original pose
- Pass criteria: Pose matches the source more closely after correction

## T20

- Test ID: T20
- Scenario: Result with an extra object
- Input characteristics: Initial output adds an invented prop
- Example user request: "Use $minimalist-portrait-line-art and remove the extra object only."
- Must preserve: Subject, pose, crop, real accessories
- Must simplify: Nothing else
- Must avoid: Removing legitimate objects
- Expected behavior: One targeted correction removes only the extra object
- Pass criteria: The invented prop is gone and the rest remains stable
