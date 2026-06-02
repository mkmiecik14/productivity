# Weekly Updates

Cadence-based status writeups, one Markdown file per week. The pattern: each Thursday (or whatever day fits your team), generate a markdown summary covering the trailing seven days, then paste it into wherever your team reads updates (Confluence, Notion, a Slack channel, etc.).

## File naming

`YYYY-MM-DD.md` — use the date the update covers *up to* (e.g., the Thursday).

## Suggested template

```markdown
# Weekly Update — YYYY-MM-DD

## Highlights
- <The 2–4 things worth surfacing>

## Progress by project
### <Project Codename>
- <What moved this week>
- <Blockers / open questions>

## Next week
- <What you're picking up>

## Asks
- <Anything you need from the team>
```

## Automation

If you have a productivity plugin with a `weekly-update` skill, point it at this folder and it can draft each update by pulling from `TASKS.md`, your calendar, and your inbox. Otherwise, write them by hand.

The folder ships empty — your weekly updates aren't part of the template.
