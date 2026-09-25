# GitHub Info

## Mona's editorial angle

Mona's website focuses on practical GitHub guidance backed by official references from:

- docs.github.com
- github.blog
- github.blog/changelog

## Current homepage themes

- GitHub collaboration basics: repositories, branches, pull requests, and merges.
- GitHub Copilot as an AI coding assistant across the IDE, CLI, and GitHub.
- GitHub Actions as the automation layer behind repository workflows.
- Recent GitHub Blog and Changelog stories worth watching.

## What's new

### GitHub Copilot Agentic Workflows

GitHub Copilot now supports **agentic workflows** — declarative YAML files that let Copilot run multi-step automation on your repository. Workflows can be triggered on schedules, slash commands, or events, and they use safe outputs to write back to GitHub (issues, PRs, comments) without direct API credentials.

Popular ready-made workflows from the [Awesome Copilot community](https://awesome-copilot.github.com/workflows/) include:

- **Daily Issues Report** — generates a daily summary of open issues as a GitHub issue, scheduled on weekdays.
- **OSPO Contributors Report** — monthly contributor activity metrics across an organization's repositories, including new-vs-returning contributor breakdown. *(Source: awesome-copilot.github.com/workflows/)*
- **Relevance Check** — a `/relevance-check` slash command that analyzes whether an issue or PR is still applicable, already resolved, or superseded, and posts its verdict as a comment. *(Source: awesome-copilot.github.com/workflows/)*
- **Weekly Comment Sync** — finds stale inline comments or README snippets, updates them to match current code, and opens a draft PR automatically. *(Source: awesome-copilot.github.com/workflows/)*

### Growing Copilot ecosystem

The Awesome Copilot repository tracks external plugins and skills contributed by the community. Recent additions include Azure-focused skills (azure-resources-query, azure-cost-health-check, azure-functions-hosted-skills), a postgres-skills plugin, and canvas-authoring tooling — showing rapid ecosystem growth around Copilot extensibility.

### Copilot in code review

Copilot code review quality guidance is now part of the Awesome Copilot project itself, with an advisory PR quality-signal workflow that evaluates incoming community contributions for fit, provenance, and validation. *(Source: github/awesome-copilot)*

## Resources

- [GitHub Docs](https://docs.github.com) — official reference for all GitHub features
- [GitHub Blog](https://github.blog/latest/) — announcements, tutorials, and developer stories
- [GitHub Changelog](https://github.blog/changelog/) — feature releases and updates
- [Awesome Copilot Workflows](https://awesome-copilot.github.com/workflows/) — community-built agentic workflow templates
