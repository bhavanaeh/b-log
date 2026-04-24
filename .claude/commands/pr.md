Create a pull request for the current branch to v4. This command must be run from the repo clone directory.

1. **Check state**: Run `git status`, `git branch`, and `git log v4..HEAD --oneline` to understand what's being proposed.

2. **Auto-branch**: If the current branch is `v4`, create a feature branch automatically:
   - Derive a short branch name from the commits (e.g., `feat/add-post-title`, `fix/broken-link`)
   - Run `git checkout -b <branch-name>`

3. **Push**: If the branch hasn't been pushed or is behind the remote, push with `-u`.

4. **Create PR**: Use `gh pr create` targeting `v4` with:
   - A short title (under 70 characters) using conventional commit style
   - A body with:
     - `## Summary` — bullet points of what changed
     - `## Test plan` — how to verify the changes

5. Return the PR URL when done.
