Create a pull request for the current branch to v4.

1. **Check state**: Run `git status`, `git branch`, and `git log v4..HEAD --oneline` to understand what's being proposed.

2. **Push**: If the branch hasn't been pushed or is behind the remote, push with `-u`.

3. **Create PR**: Use `gh pr create` targeting `v4` with:
   - A short title (under 70 characters) using conventional commit style
   - A body with:
     - `## Summary` — bullet points of what changed
     - `## Test plan` — how to verify the changes

4. If the current branch is `v4`, tell the user to create a feature branch first and stop.

5. Return the PR URL when done.
