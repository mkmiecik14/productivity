# Productivity System Template

A lightweight, file-based productivity system designed to work with [Claude](https://claude.ai/) (Cowork mode, Claude Code, or just regular chat with file access). It gives you:

- A **dashboard** (`dashboard.html`) that shows your tasks, projects, and notes in one place.
- A **memory layer** (`CLAUDE.md` + `memory/`) so Claude understands your people, projects, and jargon at the start of every session.
- A **task system** (`TASKS.md`) in Trello-style sections — Inbox, Next Actions, Deep Work, Waiting, Done, Someday.
- A **notes wiki** (`notes/`) with one folder per project, cross-linked via `[[wikilinks]]`.
- A **weekly-update folder** (`weekly-updates/`) for cadence-based status writeups.

Everything is plain Markdown + one HTML file. No database, no app, no lock-in. You own your data.

> **Browser support:** the dashboard relies on the [File System Access API](https://developer.mozilla.org/en-US/docs/Web/API/File_System_Access_API), which works in Chrome and Edge but not Safari or Firefox. All file access is local — nothing is uploaded anywhere. See [SETUP.md](SETUP.md#how-the-dashboard-reads-your-files) for details.

## Why this exists

I built this for my own work and kept improving it until it stopped getting in my way. Sharing it as a template so others can fork it, fill it in, and make it their own. If you improve it, send a PR or tag me — I'd love to see what you build.

## Quick start

See [SETUP.md](SETUP.md) for step-by-step instructions. The short version:

1. Click "Use this template" on GitHub to make your own copy.
2. Clone it locally.
3. Rename the `.template` files (drop the extension) and fill them in.
4. Open `dashboard.html` in a browser, or connect the folder to Cowork.

## Versioning

This repo uses [semantic versioning](https://semver.org/) and a [keep-a-changelog](https://keepachangelog.com/) format — see [CHANGELOG.md](CHANGELOG.md). If you've already forked the template and want to pull improvements, you can:

```bash
git remote add upstream <this-repo-url>
git fetch upstream
git log upstream/main --oneline   # see what's changed
```

…then cherry-pick or copy what you want. Because the template is mostly inert Markdown skeletons, merges are usually painless.

## What's NOT included

- Anyone's real tasks, people, or project data.
- Any plugin code, skills, or MCP server configs. Those (if applicable) live separately.
- An opinion about your task tracker. Use whatever you want — Asana, Jira, Todoist, a sheet. `TASKS.md` is just a local mirror.

## License

MIT — see [LICENSE](LICENSE).
