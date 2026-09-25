---
name: update-github-info
description: Refresh the GitHub info content from Mona's notes and current GitHub Blog updates.
on:
  schedule: daily
  workflow_dispatch:

permissions:
  contents: read
  pull-requests: read

engine: copilot

network:
  allowed:
    - github.blog
    - github.com

tools:
  edit:
  web-fetch:
  github:
    toolsets: [repos, pull_requests]

safe-outputs:
  create-pull-request:
    title-prefix: "[github-info] "
    draft: true
---

# Update GitHub Info

Update [site/content/github-info.md](site/content/github-info.md) with a concise refresh based on Mona's guidance and the latest GitHub public updates.

## Required sources

1. Read [notes/mona-notes.md](notes/mona-notes.md).
2. Read the current [site/content/github-info.md](site/content/github-info.md) before editing it.
3. Use `web-fetch` to read <https://github.blog/latest/>.
4. Use `web-fetch` to read <https://github.blog/changelog/>.
5. If you need repository guidance or reference files, use GitHub repository API tools instead of terminal, CLI, or sandboxed shell commands.
6. If you need external public guidance beyond those repository files, use `web-fetch`.

## Editing task

1. Update only [site/content/github-info.md](site/content/github-info.md).
2. Keep the writing short, practical, and aligned with Mona's editorial angle.
3. Mention the source when an update comes from the GitHub Blog or GitHub Changelog.
4. Prefer the most useful recent items for developers learning GitHub.
5. Do not edit workflow files, compile workflows, or write directly to `main`.

## Pull request task

1. When the content update is ready, use the `create_pull_request` safe output to open a draft pull request for Mona to review.
2. Summarize what changed and cite the GitHub Blog or Changelog items that informed the update.
3. If there is no meaningful update to make, do not invent one. Explain that in the pull request body and keep changes minimal.
