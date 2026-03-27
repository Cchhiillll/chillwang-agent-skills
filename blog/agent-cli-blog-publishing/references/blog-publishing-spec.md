# Blog Publishing Spec

## Current repo target
- Blog data file: `src/data/blog.js`
- New posts are inserted into `blogPosts`
- Sorting depends on `publishedAtValue` descending

## Required fields
- `title`: clear Chinese title, specific and decision-oriented when possible
- `slug`: kebab-case English slug
- `path`: `/blog/<slug>`
- `date`: month grouping, currently `2026.03`
- `publishedAt`: human-readable timestamp like `2026.03.27 09:24:00`
- `publishedAtValue`: ISO timestamp with timezone
- `readingTime`: string like `6 min read`
- `eyebrow`: `Blog · YYYY.MM.DD · Latest Post` or `Featured Post`
- `description`: detail-page summary
- `excerpt`: card/list summary
- `sections`: array of `{ title, body }`

## Tone rules
- Keep the writing grounded in real workflow or real judgment
- Prefer clear conclusions over vague scene-setting
- Explain what the thing is, why it matters, and how it applies
- Avoid generic AI enthusiasm and empty praise

## Structural rules
- Prefer 7-10 sections for major articles
- Section titles should read like conclusions, not chapter names
- Each section should advance the argument, not repeat the intro
- `description` and `excerpt` should not duplicate each other word-for-word

## Publishing checks
1. Slug and path are unique
2. `publishedAtValue` is the newest if the post should become Latest Post
3. Build passes locally
4. Card copy still fits homepage and blog list layouts
5. Commit and push succeed before claiming publication
