# Reference: CLI-first blog publishing workflow

## Best-fit scenarios
- static websites with blog content stored in repo code
- users who want to publish by chatting with an agent
- teams or solo builders who prefer Git history over CMS edits

## Recommended publishing sequence
1. Receive topic from user
2. Read current blog data structure
3. Inspect recent posts for tone and metadata patterns
4. Draft article in native schema
5. Add any related downloadable assets
6. Run local build
7. Commit and push
8. Reply with title, summary, and commit hash

## Suggested commit message patterns
- `feat: publish <topic> blog`
- `feat: add workflow article and skill attachment`
- `chore: refine published article copy`

## Notes on quality
High-quality posts in this workflow usually share three traits:
- they are grounded in a real workflow already used
- they explain trade-offs, not just steps
- they leave behind a reusable artifact (template, skill, checklist, or script)
