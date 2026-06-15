# Shownotes Skill

Codex skill for turning podcast transcripts, subtitles, or speaker-labeled text into publishable show notes and platform-specific episode copy.

## What It Produces

- Website show notes
- Apple Podcasts descriptions
- YouTube descriptions with chapter timestamps
- Newsletter teasers
- Social snippets
- Review flags and assumptions for an editor

## Install

Copy this repository into your Codex skills directory:

```sh
mkdir -p ~/.codex/skills/shownotes
cp -R SKILL.md agents references ~/.codex/skills/shownotes/
```

Then use the skill in Codex with:

```text
Use $shownotes to turn this podcast transcript into website show notes and platform-specific episode descriptions.
```

## Structure

- `SKILL.md` defines when and how the skill should be used.
- `references/output-schema.md` contains the field-level output templates and review checklist.
- `agents/openai.yaml` contains display metadata and the default prompt.

## Notes

The skill is designed to compress podcast publishing into a fast editorial pass. It should preserve exact quotes, flag uncertain speaker attribution, and call out claims that need human verification.
