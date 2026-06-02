# Memory

This folder is the long-form half of a two-tier memory system used with Claude.

## The two tiers

**Tier 1 — `CLAUDE.md` (working memory)** lives at the project root. Claude reads it at the start of every session. Keep it concise: who you are, who you work with, what your projects are called, key acronyms, working preferences. If it would take more than one screenful per section, push the detail down to tier 2.

**Tier 2 — `memory/` (long-form knowledge)** is what you're looking at. Claude consults these files when working on a specific topic. Organize semantically by topic, not chronologically.

Suggested structure:

```
memory/
├── glossary.md        # one big alphabetized glossary of terms/acronyms
├── context/           # broader background (company.md, domain.md, etc.)
├── people/            # one file per person who needs more than a one-line bio
└── projects/          # one file per project that needs deeper context
```

## When to write into memory

- You learn something durable about a person, project, tool, or domain that you'll want Claude to remember next time.
- A `CLAUDE.md` row is getting too long — promote the detail into a tier-2 file and link from `CLAUDE.md`.
- An acronym or piece of jargon keeps tripping Claude up.

## When NOT to write into memory

- Ephemeral task state (that's `TASKS.md`).
- Project decisions and meeting notes (those go in `notes/<project>/`).
- Anything sensitive: passwords, private health info, government IDs, home addresses.

## Compatibility with the `productivity` plugin

If you're using the Cowork `productivity` plugin, its `memory-management` skill knows how to read and write into this structure. If you're not, the files are still plain Markdown — Claude will read them either way.
