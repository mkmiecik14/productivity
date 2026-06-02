# Setup

Step-by-step to take this template from clone to working system.

## 1. Make your copy

On GitHub, click **Use this template → Create a new repository**. Clone it locally:

```bash
git clone git@github.com:<you>/<your-repo-name>.git ~/Documents/productivity
cd ~/Documents/productivity
```

The folder name can be whatever you want; the rest of this doc assumes `~/Documents/productivity`.

## 2. Rename the template files

The `.template` extension is there so the skeletons don't accidentally get treated as real data. Rename them:

```bash
mv CLAUDE.md.template CLAUDE.md
mv TASKS.md.template TASKS.md
mv notes/INDEX.md.template notes/INDEX.md
```

These three files are now in `.gitignore` so your personal versions stay out of the public template repo. If you want to commit them to your own private fork, remove the relevant lines from `.gitignore`.

## 3. Fill in `CLAUDE.md`

Open it and replace every `<...>` placeholder. The most important sections:

- **Me** — name, email, one-sentence role.
- **People** — the handful of people Claude should recognize by first name. Add more as needed.
- **Projects** — codenames Claude will see in tasks and notes. Keep them short and memorable.
- **Key Terms / Acronyms** — anything an outsider wouldn't decode.

Don't try to fill everything in on day one. Add rows as Claude encounters things it doesn't understand.

## 4. Set up your first project

```bash
cp -r notes/_template notes/your-project-codename
```

Open `notes/your-project-codename/index.md` and replace the placeholders. Then add a row for it in `notes/INDEX.md` and in the Projects table in `CLAUDE.md`.

There's an `example-project/` folder showing what a project page looks like after a few months of use — keep it as a reference or delete it once you don't need it.

## 5. Open the dashboard

```bash
open dashboard.html
```

(or just double-click it). The dashboard reads from `TASKS.md`, `notes/`, and `CLAUDE.md` and gives you a one-page view of everything.

### How the dashboard reads your files

The dashboard uses the browser's [File System Access API](https://developer.mozilla.org/en-US/docs/Web/API/File_System_Access_API) — it can't see any files until you grant it access. On first load you'll be prompted to select `TASKS.md` (and, in the Memory tab, your project folder). Your selection is persisted in IndexedDB so you don't have to re-pick on every reload.

A few gotchas worth knowing:

- **Authorizations are remembered per-file-path of the HTML page.** If you open two copies of the dashboard from different folders (e.g., this template plus your real one), each remembers its own selection independently — no cross-contamination.
- **But if you ever re-open the same dashboard.html and don't see what you expect**, you may be looking at a previously-authorized folder. To reset: open DevTools (F12) → **Application → Storage → Clear site data**, then reload. The dashboard will prompt for selection again.
- **Chrome and Edge support this API; Safari and Firefox do not** (as of 2026). On unsupported browsers, the dashboard falls back to read-only mode or won't load at all. Use Chrome/Edge for full functionality.
- **The dashboard never sends your data anywhere.** All reads and writes are local; there's no server.

## 6. (Optional) Connect Claude

If you use Cowork or Claude Code, point it at this folder. Claude will pick up `CLAUDE.md` automatically and treat the rest of the structure as your working context.

If you also install the [`productivity` plugin](https://github.com/anthropics/skills) (or whatever plugin you're using), its `task-management`, `memory-management`, and `update` skills know how to read and write the files in this structure.

## 7. Pulling future improvements

```bash
git remote add upstream <template-repo-url>
git fetch upstream
git log upstream/main --oneline
```

Look at [CHANGELOG.md](CHANGELOG.md) in the upstream repo to see what's new. Copy in what you want; ignore the rest. Because nothing here is generated, merges are mostly manual but trivial.
