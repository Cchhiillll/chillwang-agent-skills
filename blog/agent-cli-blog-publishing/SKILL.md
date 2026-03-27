---
name: agent-cli-blog-publishing
description: Publish high-quality blog posts to a static site entirely through CLI and agent collaboration, without any CMS or backend admin page. Use when the user wants to draft, structure, refine, publish, or attach reusable workflow assets for blog posts managed in code (for example blog data files inside a frontend repo).
---

# Agent CLI Blog Publishing

Use this skill when the site is code-driven and blog posts are stored directly in the repository instead of a CMS.

## Core outcome

Turn a chat request into a publishable post by following one CLI-first path:
1. clarify the article angle
2. inspect the repository's existing blog schema
3. draft title / slug / metadata / excerpt / sections in the site's native format
4. edit the content into the repo directly
5. build locally to validate rendering
6. commit and push
7. report the published result back to the user

## Workflow

### 1. Confirm the publishing target
Identify where posts live in the repo.
For code-driven sites, inspect files such as:
- `src/data/blog.js`
- `content/blog/*`
- `posts/*`
- route data files or markdown collections

Do not invent a new publishing system if one already exists.

### 2. Mirror the existing editorial schema
Match the site's current structure exactly:
- title
- slug
- path
- published time
- reading time
- eyebrow / category fields
- description
- excerpt
- sections or markdown body

Before adding a post, inspect 2-3 recent posts and copy the same level of density, tone, and field naming.

### 3. Write for the site's actual voice
Keep the article aligned with the current blog voice.
Prefer:
- a clear argument in the opening
- section titles that read like conclusions
- paragraphs that explain both "what it is" and "why it matters"
- concrete workflow steps when the article is operational

Avoid:
- generic AI filler
- vague praise without mechanism
- introducing terminology not used elsewhere on the site unless needed

### 4. If the article describes a workflow, make the workflow explicit
For process-heavy posts, include:
- trigger: what starts the workflow
- inputs: repo / notes / links / context
- transformation: drafting, structuring, refining
- validation: build / preview / schema checks
- publish step: commit / push
- reuse pattern: how to repeat the workflow later

### 5. Treat publishing as code
After editing:
- run the local build
- fix any rendering or data-shape errors
- commit with a clear message
- push to the canonical branch

Do not claim a post is published until the build passes and the push succeeds.

### 6. When asked for an attachment, package the workflow as a reusable asset
If the user wants the workflow turned into a skill or attachment:
- create a compact skill folder
- keep `SKILL.md` short and procedural
- move deeper guidance to `references/` if needed
- package as a `.skill` or zip-style downloadable artifact when practical
- place it in a stable, user-accessible path

## Checklist before finalizing
- Does the article fit the site's existing blog schema?
- Is the title specific enough?
- Does the excerpt say something real?
- Does the body contain reusable insight, not just narrative?
- Did the local build pass?
- Was the change committed and pushed?
- If an attachment was requested, is the file actually created and reachable?
