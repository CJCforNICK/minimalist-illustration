[繁體中文](README.zh-TW.md)

# Minimalist Portrait Line Art

Minimalist Portrait Line Art is a repository-local Codex Skill for transforming portrait, full-body, fashion, couple, and group photos into clean black-and-white minimalist line art. It is designed to preserve the people, pose, composition, clothing silhouette, and important identity cues while simplifying photographic detail into intentional hand-drawn lines.

## What the Skill does

- Turns supplied photos into sparse black-and-white portrait line art
- Preserves the number of people, pose, crop, major accessories, and key held objects
- Removes the original photographic background by default
- Uses built-in image editing or image generation capabilities from the user's ChatGPT or Codex environment when available
- Supports multilingual user requests while keeping structured internal prompts in English

## What the Skill does not do

- It does not host, train, or bundle an image model
- It does not create a website, backend, server, database, or MCP server
- It does not add OpenAI API calls or require `OPENAI_API_KEY`
- It does not install Stable Diffusion, ComfyUI, ControlNet, or another local model
- It does not guarantee photorealistic identity preservation

## Example workflow

1. Attach a source photo.
2. Invoke `$minimalist-portrait-line-art`.
3. The Skill analyzes the people, pose, crop, clothing silhouette, accessories, and held objects.
4. The Skill builds a structured English editing prompt.
5. The host image tool generates one result by default.
6. The Skill checks recognizability, simplicity, and prohibited elements, then optionally applies one narrow correction.

## Main style characteristics

- Pure black lines on a pure white background by default
- Mostly consistent medium line weight
- Slight organic hand-drawn character
- Selective broken contours
- Large areas of white space
- Symbolic facial features
- At most one or two restrained solid-black accent regions

## Requirements

- A ChatGPT or Codex environment that exposes image generation or image editing for the current task
- A user-supplied source photo
- Owned, licensed, consented, or freely reusable images for public examples and tests

No server is required. No database is required. No local GPU is required. The repository itself does not include an image model.

## Repository-local installation

Place this repository where your Codex environment can access repository-local skills, then use the skill directly from `.agents/skills/minimalist-portrait-line-art/`.

## Personal installation guidance

If you want a personal copy outside this repository, copy the skill folder into your personal Codex skills directory while preserving:

- `SKILL.md`
- `agents/openai.yaml`
- `references/`

## Usage in Codex

Invoke the skill explicitly with `$minimalist-portrait-line-art`.

Example:

`Use $minimalist-portrait-line-art to turn this portrait photo into clean black-and-white minimal line art.`

## English usage examples

- `Use $minimalist-portrait-line-art to turn this portrait photo into clean black-and-white minimal line art.`
- `Use $minimalist-portrait-line-art to preserve the couple's height difference, pose, and clothing silhouettes while removing the background.`
- `Use $minimalist-portrait-line-art with a transparent background and keep the flowers in the subject's hands.`

## Language guide

Traditional Chinese documentation is available at [README.zh-TW.md](README.zh-TW.md).

## Project structure

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

## Testing approach

This repository currently uses a textual test plan in [tests/test-cases.md](tests/test-cases.md). The tests cover single-person, couple, group, fashion, accessory, transparency, and correction scenarios, including multilingual trigger examples. Do not execute the tests with private or unlicensed images.

## Privacy guidance

- Do not commit private portrait photos
- Do not store user-uploaded photos inside the skill
- Remind contributors to obtain consent before publishing identifiable portraits
- Do not embed reference photos as base64 data

## Copyright guidance

- Do not publish copyrighted style-reference book pages
- Do not reproduce text or graphics from photographed reference pages
- Convert visual observations into abstract style rules instead
- Public examples must use owned, licensed, or freely reusable images

## Cost and infrastructure

The repository does not pay for, proxy, or meter user generations. Image generation depends on capabilities available in the user's own ChatGPT or Codex environment, and usage may count against the user's own plan or image-generation allowance. The repository introduces no recurring infrastructure cost.

## Current limitations

- Output quality depends on the host's image editing capability
- Some hosts may expose generation but not strong identity-preserving edits
- Complex group scenes may need an additional user-approved iteration
- Transparent-background support depends on the active host tool

## Roadmap

- Refine prompt recipes for more difficult multi-person poses
- Improve guidance for preserving one requested environmental object
- Add more acceptance examples for transparent-background outputs

## Contributing

Keep the skill focused on one task, preserve progressive disclosure, avoid API fallbacks, and do not add infrastructure that changes the project's cost model. When contributing examples or tests, use only consented, owned, licensed, or freely reusable images.

## License status

A license will be selected before public release. Do not invent or guess a copyright owner's name.
