---
title: publishing setup
date: 2026-04-23
draft: false
tags: [meta, workflow]
---

obsidian for writing, quartz4 for building, github actions for deploying. notes live in `b-log/content/`, pushes to `v4` trigger a deploy.

### workflow

1. create a new note in obsidian using the template (starts with `draft: true`)
2. write and iterate
3. run `/publish <note-name>` in claude code when ready

### custom claude code commands i set up

`/publish` — the main one. sets `draft: false` in frontmatter, creates a `publish/<note-slug>` branch off `v4`, commits with conventional commit format (`feat: publish <title>`), opens a PR to `v4`, merges it, cleans up.

`/commit` — stages and commits changes using conventional commits. picks the right prefix based on what changed:

- `feat:` for new stuff
- `fix:` for bugs
- `chore:` for config and maintenance
- `docs:` for documentation
- `style:` for formatting/theme changes
- `refactor:` for restructuring without behavior change

`/pr` — pushes the current branch and opens a PR to `v4`. writes a summary and test plan in the body. useful when i want to review before merging instead of going straight through `/publish`.

### note template

every new note starts with:

```yaml
---
title: 
date: {{date}}
draft: true
tags: []
---
```

notes stay hidden until published.
