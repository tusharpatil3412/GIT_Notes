# Implementation Plan

## Approach
Create a single new file `CONTRIBUTING.md` at the repository root. The file will follow standard open-source contributing guide conventions and include exactly the four sections specified in the acceptance criteria, each with 1-2 sentences of practical, concise guidance.

## Files to Create

### `CONTRIBUTING.md`
A Markdown document at the repo root with the following structure:

```markdown
# Contributing

Thank you for your interest in contributing!

## Getting Started
Fork the repository and clone it locally. Make sure you have all dependencies installed before making changes.

## Branching
Create a new branch for each feature or bug fix using a descriptive name (e.g. `feature/my-feature` or `fix/issue-123`). Never commit directly to `main`.

## Commit Messages
Write clear, concise commit messages in the imperative mood (e.g. "Add login validation"). Reference relevant issue numbers where applicable.

## Pull Requests
Open a pull request against `main` with a clear description of what was changed and why. Ensure all checks pass before requesting a review.
```

## Files to Modify
None.

## Implementation Steps
1. Create `CONTRIBUTING.md` at the repository root with the content above.
2. Verify the four required sections are present: Getting Started, Branching, Commit Messages, Pull Requests.
3. Verify each section contains 1-2 sentences of guidance.
4. Confirm no other files have been modified.

## Test Strategy
- Manual review: confirm file exists at repo root.
- Manual review: confirm all four sections are present and correctly headed.
- Manual review: confirm no other files were changed.

## Edge Cases
- None applicable for a pure documentation task.