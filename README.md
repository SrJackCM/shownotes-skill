# Shownotes Agent Skill

Agent skill for turning podcast transcripts, subtitles, or speaker-labeled text into publishable show notes and platform-specific episode copy. It is written to work with Claude, Gemini, and Codex workflows.

## What It Produces

- Website show notes
- Apple Podcasts descriptions
- YouTube descriptions with chapter timestamps
- Newsletter teasers
- Social snippets
- Review flags and assumptions for an editor

## Use With Codex

Copy this repository into your Codex skills directory:

```sh
mkdir -p ~/.codex/skills/shownotes
cp -R SKILL.md agents references ~/.codex/skills/shownotes/
```

Then use the skill in Codex with:

```text
Use $shownotes to turn this podcast transcript into website show notes and platform-specific episode descriptions.
```

## Use With Claude

Use the repository as a Claude Skill folder. The core skill instructions are in `SKILL.md`, with reusable templates in `references/output-schema.md`.

Suggested prompt:

```text
Use the shownotes skill to turn this podcast transcript into website show notes, Apple Podcasts copy, and a YouTube description with timestamps.
```

## Use With Gemini

Gemini Gems use saved instructions rather than this exact skill-folder format. Copy the instructions from `GEMINI.md` into a custom Gem, and add `references/output-schema.md` as a knowledge file if your Gemini interface supports knowledge uploads.

## Structure

- `SKILL.md` defines when and how the skill should be used.
- `references/output-schema.md` contains the field-level output templates and review checklist.
- `agents/openai.yaml` contains display metadata and the default prompt.
- `GEMINI.md` contains a paste-ready Gemini Gem instruction version.

## Notes

The skill is designed to compress podcast publishing into a fast editorial pass. It should preserve exact quotes, flag uncertain speaker attribution, and call out claims that need human verification.
