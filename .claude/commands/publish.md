Publish an Obsidian note to b-log.

The user will provide the name or path of a note to publish. Follow these steps:

1. **Find the note**: Look for the note in the `quartz/content/` directory of this repo. If the user gives a partial name, search for it. If the note doesn't exist, tell the user and stop.

2. **Update frontmatter**: Set `draft: false` in the note's YAML frontmatter. If there is no frontmatter, add it. If `draft` is already `false`, tell the user the note is already published and ask if they want to continue anyway.

3. **Create a feature branch**: Branch off `v4` with the naming convention `publish/<note-slug>` where `<note-slug>` is the note filename in kebab-case without the `.md` extension.

4. **Commit**: Use conventional commit format: `feat: publish <note title>`
   - Use the note's `title` from frontmatter if available, otherwise use the filename.

5. **Push and open a PR**: Push the branch and open a PR to `v4` with:
   - Title: `feat: publish <note title>`
   - Body: A short summary noting which note is being published, with a link to it.

6. **Merge the PR**: Merge the PR using squash merge, then delete the remote branch.

7. **Clean up**: Switch back to the `v4` branch and pull latest.

If anything fails at any step, stop and report the error clearly.
