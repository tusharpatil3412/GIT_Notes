# Implementation Plan

## Approach
The repository currently has no `README.md` — only `GIT_Notes.html`. We will create `README.md` with a `## Common Git Commands` section placed near the bottom of the file. Each of the five commands will be listed with a brief one-line description in a clean Markdown format.

## Files to Create

### `README.md`
A new top-level README for the repository. It will include a `## Common Git Commands` section near the bottom with the five specified commands.

## Files to Modify
_None_ — no existing files need to be changed.

## Implementation Steps

1. **Create `README.md`** at the repository root.
2. Add a minimal top-level heading (e.g. `# Git Notes`) so the file is well-formed.
3. Add the `## Common Git Commands` section near the bottom with the following content:

```markdown
## Common Git Commands

- `git status` — Show the working tree status, including staged, unstaged, and untracked files.
- `git add` — Stage changes (files or hunks) to be included in the next commit.
- `git commit` — Record staged changes to the repository with a descriptive message.
- `git push` — Upload local branch commits to the corresponding remote branch.
- `git pull` — Fetch changes from the remote and merge them into the current branch.
```

4. Review the Markdown renders correctly (headings, inline code, bullet list).

## Test Strategy
This is a documentation-only change. Validation steps:
- Confirm the file renders correctly in a Markdown previewer (GitHub, VS Code, etc.).
- Confirm all five commands are present and each has a one-line description.
- Confirm the section heading is exactly `## Common Git Commands`.
- Confirm the section appears near the bottom of the file.

## Edge Cases
- If a `README.md` already exists at the time of implementation (e.g. added by another PR), insert the section near the bottom of the existing file rather than creating a new one.
- Ensure no trailing whitespace or Windows-style line endings (`\r\n`) are introduced.