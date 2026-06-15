---
name: shownotes
description: Generate podcast show notes, episode descriptions, chapter timestamps, takeaways, quotes, and platform-specific promo copy from a transcript or subtitle file. Use when the user wants website show notes, Apple Podcasts descriptions, YouTube descriptions, newsletter blurbs, or social copy derived from podcast audio, transcripts, SRT, VTT, or speaker-labeled text.
---

# Shownotes

## Overview

Use this skill when the user wants a podcast transcript turned into a clean, reviewable content package instead of a single generic summary. The skill is optimized for multi-output publishing: website show notes, Apple Podcasts, YouTube, newsletter, and social variants.

Read [references/output-schema.md](references/output-schema.md) when you need the full field list, destination-specific templates, or the human review checklist.

## Workflow

### 1. Confirm the usable inputs

Prefer these inputs, in order:

- Transcript or subtitle file: `SRT`, `VTT`, speaker-labeled text, or cleaned plain transcript
- Episode context: working title, guest name, show name, audience, publish destinations
- Brand voice material: tone notes, vocabulary preferences, 2-3 past examples, CTA rules
- SEO hints: target keyword, related topics, internal links to related episodes

If some inputs are missing, proceed with reasonable defaults and label assumptions instead of blocking.

### 2. Normalize the transcript before writing

Do a light editorial cleanup for analysis:

- Normalize speaker labels
- Remove filler words only when they do not affect meaning
- Detect topic shifts for chapter timestamps
- Extract books, tools, companies, URLs, and named people
- Preserve exact wording for direct quotes

If speaker attribution is uncertain, mark it as uncertain rather than inventing confidence.

### 3. Produce only the destinations the user needs

Default to a website-first package plus any explicitly requested destinations.

Common destinations:

- Website show notes
- Apple Podcasts description
- YouTube description with timestamps
- Newsletter teaser
- Social snippets

If the user says "all formats" or does not specify, start with the website package and add Apple Podcasts and YouTube. Only add newsletter and social when they are clearly useful.

### 4. Keep the package editorially useful

Prioritize structured outputs that save review time:

- Strong working title
- Clear executive summary
- Accurate chapter timestamps
- Actionable takeaways
- Quotable lines with attribution
- Resource list
- Guest bio when a guest is present

Do not pad the output with generic praise, exaggerated claims, or AI-style filler. Keep summaries concrete and episode-specific.

### 5. Apply brand voice and SEO without making it robotic

When brand guidance exists, follow it closely. Examples beat abstract instructions.

If SEO is requested or obviously relevant:

- Put the primary topic naturally near the top
- Use descriptive section headings
- Suggest meta description copy for website versions
- Suggest internal link opportunities when related episodes are known

Do not force keywords into every sentence.

### 6. Mark what still needs a human

Always flag items that require editorial review:

- Strategic hook choice
- Possible sarcasm, jokes, or subtext
- Sensitive claims in health, finance, legal, or technical domains
- Statistics or factual claims that need verification
- Sponsor mentions, lead magnets, or brand-sensitive positioning

The goal is not full autonomy. The goal is to compress production into a fast editorial pass.

## Output Rules

- Match the user's requested format first
- Keep timestamps consistent: `MM:SS - Label`
- Keep takeaways actionable, not abstract
- Attribute quotes to a speaker when possible
- Separate assumptions and review flags from final copy
- If the transcript quality is poor, say so briefly and note where that may affect timestamps or summaries

## Default Deliverable Shape

Unless the user asks for a different layout, return:

1. Final copy for each requested destination
2. A short `Review flags` section
3. A short `Assumptions` section only when needed

## When To Load The Reference

Open [references/output-schema.md](references/output-schema.md) when:

- The user wants a full multi-platform package
- You need field-by-field templates
- You need a reusable review checklist
- You want the recommended website, Apple, YouTube, newsletter, or social output structure
