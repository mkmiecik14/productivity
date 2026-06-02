# Changelog

All notable changes to this template are documented here. Format follows [Keep a Changelog](https://keepachangelog.com/en/1.1.0/); versions follow [Semantic Versioning](https://semver.org/).

## [Unreleased]

### Added
- README and SETUP notes explaining the dashboard's File System Access permission model, browser support, and how to reset a stuck authorization.

### Changed
- **Unified folder onboarding.** One "Connect Folder" pick now loads TASKS.md, CLAUDE.md, memory/, notes/, and weekly-updates/ in a single step. Previously required two separate authorizations (TASKS.md as a file, then the project folder as a directory). Legacy single-file selection is still available as a fallback link under the primary CTA.

## [0.1.0] — 2026-05-31

### Added
- Initial public release of the productivity system template.
- `dashboard.html` — single-file HTML dashboard.
- `CLAUDE.md.template` — working-memory skeleton with Me / People / Projects / Terms / Preferences sections.
- `TASKS.md.template` — Trello-style task file (Inbox / Next Actions / Deep Work / In Review-Waiting / Done / Someday-Maybe).
- `notes/` — per-project wiki structure with `INDEX.md.template`, `_template/index.md` skeleton, and a fully-worked `example-project/` reference.
- `memory/` — two-tier memory scaffolding (`context/`, `people/`, `projects/`) with explanatory README.
- `weekly-updates/` — empty folder with README documenting the cadence pattern.
- `README.md`, `SETUP.md`, `LICENSE` (MIT), `.gitignore`.
