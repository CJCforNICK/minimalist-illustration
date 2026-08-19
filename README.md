[繁體中文](README.zh-TW.md)

# Minimalist Portrait Line Art

Minimalist Portrait Line Art is a repository-local Codex Skill for transforming portrait, full-body, fashion, couple, group, and action-pose photos into clean black-and-white minimalist line art.

The Skill is not a photo-tracing filter. It is designed to rebuild a person as a sparse symbolic illustration: preserve the pose, crop, gesture, clothing silhouette, face direction, and key identity cues, then remove photographic detail until the drawing feels simple, readable, and hand-drawn.

## Project Status

This repository is publicly shareable as an early, documentation-first skill project. It contains skill instructions, prompt structure, quality criteria, and text-based test cases. It does not contain a hosted service, an image model, API scripts, or bundled portrait examples.

The current focus is prompt and evaluation logic for minimalist portrait reconstruction, especially difficult cases such as group hand relationships, compact poses, obscured faces, and foreground gestures.

## Quick Start

1. Open this repository in a Codex environment that supports repository-local skills.
2. Attach a user-owned, licensed, consented, or otherwise usable source photo.
3. Invoke `$minimalist-portrait-line-art`.
4. Ask for one clean black-and-white minimalist line-art result.

Example:

`Use $minimalist-portrait-line-art to turn this photo into sparse black-and-white minimalist line art while preserving the pose, face direction, clothing silhouette, and hand gesture.`

## Core Approach

The Skill works best when it treats the photo as structure, not as surface detail.

- It builds a `Pose Map` before generating the image.
- It turns the pose map into a `Drawing Plan`.
- It preserves posture, gaze, hand ownership, object ownership, clothing layers, and important occlusions.
- It uses symbolic marks for faces and hands instead of realistic anatomy.
- It removes background, shadows, texture, readable clothing text, dense folds, and photographic rendering.

This makes the output closer to a minimalist lifestyle doodle or editorial line figure than a polished portrait sketch.

## What The Skill Does

- Turns supplied photos into sparse black-and-white portrait line art.
- Preserves the number of people, relative placement, pose, crop, major accessories, and key held objects.
- Prioritizes hand gestures, contact relationships, and object ownership in couple and group photos.
- Handles compact and action poses by preserving body compression, support points, bent knees, foot placement, and occlusion.
- Preserves face visibility accurately: if the source face is hidden by a cap brim, hair, sunglasses, mask, angle, motion, object, or crop, the drawing should not invent a full face.
- Removes the original photographic background by default.
- Uses built-in image editing or image generation capabilities from the user's ChatGPT or Codex environment when available.
- Accepts multilingual user requests while keeping structured image prompts in English.

## What The Skill Does Not Do

- It does not host, train, or bundle an image model.
- It does not create a website, backend, server, database, or MCP server.
- It does not add OpenAI API calls or require `OPENAI_API_KEY`.
- It does not install Stable Diffusion, ComfyUI, ControlNet, or another local model.
- It does not guarantee photorealistic identity preservation.
- It does not store uploaded portraits inside the repository.

## Example Workflow

1. Attach a source photo.
2. Invoke `$minimalist-portrait-line-art`.
3. The Skill inspects the photo and identifies the visual features that must be preserved.
4. The Skill writes a `Pose Map`, including face visibility, hand positions, held objects, support points, and occlusions.
5. The Skill writes a `Drawing Plan`, including black fills, primary contours, layer breaks, face symbols, and intentional omissions.
6. The host image tool generates one result by default.
7. The Skill checks pose accuracy, recognizability, simplicity, and prohibited elements.
8. If needed, the Skill performs one narrow correction, such as reducing facial realism or restoring an obscured face.

## Main Style Characteristics

- Pure black lines on a pure white background by default.
- Mostly consistent medium line weight.
- Slight organic hand-drawn character.
- Selective broken contours instead of fully closed outline tracing.
- Large areas of white space.
- Symbolic facial features made from dots, dashes, and short curves.
- Simplified hands that preserve gesture without anatomical detail.
- Simplified clothing shapes with only essential collars, hems, cuffs, waistlines, pockets, straps, or layer breaks.
- At most one or two restrained solid-black accent regions.

## Important Drawing Rules

- Reconstruct the figure from a pose plan instead of tracing every photographic edge.
- Preserve body structure before adding any style marks.
- Use black fills as graphic anchors, not shadows.
- If a face is barely visible, keep it barely visible.
- If a hand or limb is ambiguous, simplify it or hide it in the silhouette instead of inventing anatomy.
- If clothing layers merge, add the minimum boundary break needed for readability.
- If a result looks like cleaned realistic line art, restart from the drawing plan instead of polishing the same image.

## Requirements

- A ChatGPT or Codex environment that exposes image generation or image editing for the current task.
- A user-supplied source photo.
- Owned, licensed, consented, or freely reusable images for public examples and tests.

No server is required. No database is required. No local GPU is required. The repository itself does not include an image model.

## Repository-Local Installation

Place this repository where your Codex environment can access repository-local skills, then use the skill directly from `.agents/skills/minimalist-portrait-line-art/`.

## Personal Installation Guidance

If you want a personal copy outside this repository, copy the skill folder into your personal Codex skills directory while preserving:

- `SKILL.md`
- `agents/openai.yaml`
- `references/`

## Usage In Codex

Invoke the skill explicitly with `$minimalist-portrait-line-art`.

Examples:

- `Use $minimalist-portrait-line-art to turn this portrait photo into clean black-and-white minimal line art.`
- `Use $minimalist-portrait-line-art to preserve the couple's height difference, pose, and clothing silhouettes while removing the background.`
- `Use $minimalist-portrait-line-art and keep the face mostly hidden under the cap brim, as in the source photo.`
- `Use $minimalist-portrait-line-art to preserve the crouching skateboard pose and simplify the face, hands, shoes, and clothing folds.`

## Language Guide

Traditional Chinese documentation is available at [README.zh-TW.md](README.zh-TW.md).

## Project Structure

```text
.agents/
  skills/
    minimalist-portrait-line-art/
      SKILL.md
      agents/openai.yaml
      references/
        style-guide.md
        prompt-recipes.md
        quality-checklist.md
tests/
  test-cases.md
README.md
README.zh-TW.md
.gitignore
```

## Testing Approach

This repository currently uses a textual test plan in [tests/test-cases.md](tests/test-cases.md). The tests cover single-person, couple, group, fashion, accessory, transparency, correction, obscured-face, and compact-pose scenarios. Do not execute the tests with private or unlicensed images.

## Privacy Guidance

- Do not commit private portrait photos.
- Do not upload private portraits into public issues, pull requests, or example folders.
- Do not store user-uploaded photos inside the skill.
- Remind contributors to obtain consent before publishing identifiable portraits.
- Do not embed reference photos as base64 data.

## Copyright Guidance

- Do not publish copyrighted style-reference book pages.
- Do not reproduce text or graphics from photographed reference pages.
- Convert visual observations into abstract style rules instead.
- Public examples must use owned, licensed, or freely reusable images.

## Cost And Infrastructure

The repository does not pay for, proxy, or meter user generations. Image generation depends on capabilities available in the user's own ChatGPT or Codex environment, and usage may count against the user's own plan or image-generation allowance. The repository introduces no recurring infrastructure cost.

## Public Sharing Checklist

Before sharing this repository publicly, confirm:

- No private portraits were committed.
- No copyrighted reference pages were copied into the repository.
- Public examples use owned, licensed, or freely reusable images.
- You are comfortable sharing the current no-license-yet project status.

## Current Limitations

- Output quality depends on the host's image editing capability.
- Some hosts may expose generation but not strong identity-preserving edits.
- Complex group scenes may need one additional user-approved iteration.
- Strong foreground foreshortening and hand gestures can still require targeted correction.
- Transparent-background support depends on the active host tool.

## Roadmap

- Add more text-based tests for compact poses, action poses, and obscured faces.
- Improve guidance for foreground hand gestures without over-rendering anatomy.
- Improve guidance for preserving one requested environmental support object, such as a chair, curb, or car roof.
- Add more acceptance examples for transparent-background outputs.

## Contributing

Keep the skill focused on one task, preserve progressive disclosure, avoid API fallbacks, and do not add infrastructure that changes the project's cost model. When contributing examples or tests, use only consented, owned, licensed, or freely reusable images.

## License Status

A license will be selected before public release. Do not invent or guess a copyright owner's name.
