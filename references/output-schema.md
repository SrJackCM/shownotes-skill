# Podcast Shownotes Output Schema

Use this reference when the user wants a full package rather than a single summary.

## Recommended Input Contract

- Transcript source: `SRT`, `VTT`, plain text, or speaker-labeled transcript
- Episode title or working topic
- Host and guest names
- Audience description
- Brand voice notes
- Requested destinations
- SEO keyword or theme, if applicable

## Recommended Website Package

Use this set when the user asks for "show notes" without narrowing the channel.

- `episode_title_suggestion`
  - Aim for fewer than 70 characters
  - Clear, specific, and searchable
- `meta_description`
  - Aim for fewer than 155 characters
  - Include the main topic naturally
- `executive_summary`
  - Usually 250 to 400 words
  - Explain what the episode covers and why it matters
- `chapter_timestamps`
  - Usually 8 to 15 entries
  - Format: `MM:SS - Description`
- `key_takeaways`
  - Usually 3 to 7 bullets
  - Must be actionable or memorable
- `notable_quotes`
  - Usually 3 to 5 quotes
  - Include speaker attribution
- `resources_mentioned`
  - Books, tools, people, companies, URLs
  - Prefer a clean bulleted list
- `guest_bio`
  - 2 to 3 sentences
  - Only when relevant

## Apple Podcasts Description

- `short_summary`
  - Front-load the strongest hook
  - Keep it concise enough to scan quickly
  - Avoid website-only formatting clutter

## YouTube Description

- `description`
  - Open with the episode hook
  - Include timestamps
  - Include key links
  - Add subscribe or next-step CTA if the brand uses one
- `tags`
  - 10 to 15 relevant tags only when specifically requested

## Newsletter Teaser

- `hook`
  - 1 to 2 sentences
  - Create curiosity without sounding manipulative
- `key_insight`
  - The single most valuable idea from the episode
- `cta`
  - Give a concrete reason to click and listen

## Social Variants

- `twitter_thread`
  - 3 to 5 posts
  - Lead with the strongest insight or quote
- `linkedin_post`
  - 150 to 200 words
  - Angle toward professional relevance

## Brand Voice Guidance

If the user gives a voice guide, apply it in this priority order:

1. Real examples from past episodes
2. Vocabulary include and avoid lists
3. Audience sophistication
4. Tone labels such as conversational, technical, or authoritative
5. Formatting preferences

If the instructions conflict, prefer the examples.

## SEO Guidance

Use only when requested or clearly beneficial.

- Mention the main topic naturally near the beginning
- Use descriptive headings for website versions
- Suggest related internal links when the show catalog is known
- Write meta descriptions like search snippets, not ad slogans

## Human Review Checklist

Attach or use this checklist when the user wants a production-ready workflow:

- Does the summary capture the real core insight, not just the topic list?
- Are timestamps accurate? Spot-check at least 3.
- Are quotes natural and attributed correctly?
- Are resources described correctly?
- Does the tone match the brand voice?
- Are there factual claims that need verification?
- Are CTAs placed appropriately?
- Is the hook strong enough to drive a click or listen?

## Known Failure Modes

Flag these instead of hiding them:

- Weak speaker diarization
- Jokes or sarcasm interpreted literally
- Tangents treated as main takeaways
- Hallucinated links or overconfident resource identification
- Overly generic titles and summaries

## Default Assembly Order

When building a full package, assemble in this order:

1. Title and meta description
2. Executive summary
3. Timestamps
4. Takeaways
5. Quotes
6. Resources
7. Destination-specific variants
8. Review flags
