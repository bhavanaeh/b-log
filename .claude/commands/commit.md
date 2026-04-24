Commit changes in the b-log repo. This command must be run from the repo clone directory.

1. **Check branch**: If the current branch is `v4`, create a feature branch before committing:
   - Derive a short branch name from the staged changes (e.g., `feat/add-post-title`, `fix/broken-link`)
   - Run `git checkout -b <branch-name>`

2. **Review changes**: Run `git status` and `git diff` to see what's changed. Also check `git log --oneline -5` for recent commit style.

3. **Stage relevant files**: Add the changed files. Do not stage files that contain secrets or credentials.

4. **Commit**: Use conventional commit format based on the nature of the changes:
   - `feat:` for new content or features
   - `fix:` for bug fixes
   - `chore:` for config, maintenance, tooling
   - `docs:` for documentation updates
   - `style:` for formatting/theme changes
   - `refactor:` for restructuring without behavior change

   Keep the message concise (1-2 sentences) focused on the "why."

5. If there are no changes to commit, say so and stop.
