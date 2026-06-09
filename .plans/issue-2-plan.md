# Implementation Plan

## Approach

Modify `GIT_Notes.html` to insert a new `git fetch` documentation section. The section should be placed near the existing remote-interaction commands (`git pull`, `git push`) to maintain logical grouping. All content must follow the existing HTML structure, heading levels, code block styles, and class naming conventions.

## Files to Modify

### `GIT_Notes.html`
- Locate the section containing `git pull` and/or `git push`
- Insert a new `git fetch` section in the appropriate position (before `git pull` is recommended since fetch is a subset of pull)
- Section must include:
  1. **What `git fetch` does** — downloads remote refs and objects without merging into the working branch
  2. **`git fetch` vs `git pull`** — clearly explain that `git pull` = `git fetch` + `git merge`/`git rebase`
  3. **Three usage forms** with explanations:
     - `git fetch` — fetch all branches from the default remote
     - `git fetch <remote>` — fetch all branches from a named remote
     - `git fetch <remote> <branch>` — fetch a specific branch from a named remote
  4. **Practical example** — show `git diff main origin/main` after fetching to inspect changes before merging

## Implementation Steps

1. Open `GIT_Notes.html` and identify the location of the `git pull` and `git push` sections.
2. Insert the new `git fetch` section immediately before `git pull` (or between pull and push, depending on existing order).
3. Use the same heading level (e.g., `<h2>` or `<h3>`) as surrounding sections.
4. Use the same code block style and CSS class names as existing command examples.
5. Escape all HTML special characters: `<remote>` → `&lt;remote&gt;`, `<branch>` → `&lt;branch&gt;`.
6. Ensure all tags are properly opened and closed.
7. Validate the file with an HTML validator (e.g., validator.w3.org).

## Example Section Structure

```html
<section>
  <h2>git fetch</h2>
  <p>
    <code>git fetch</code> downloads commits, files, and refs from a remote repository
    into your local repo, but does <strong>not</strong> merge them into your working branch.
    This lets you review changes before integrating them.
  </p>

  <h3>git fetch vs git pull</h3>
  <p>
    <code>git pull</code> is shorthand for <code>git fetch</code> followed by
    <code>git merge</code> (or <code>git rebase</code>). Use <code>git fetch</code>
    when you want to inspect remote changes before merging.
  </p>

  <h3>Usage</h3>
  <pre><code>git fetch</code></pre>
  <p>Fetch all branches from the default remote (usually <em>origin</em>).</p>

  <pre><code>git fetch &lt;remote&gt;</code></pre>
  <p>Fetch all branches from the specified remote.</p>

  <pre><code>git fetch &lt;remote&gt; &lt;branch&gt;</code></pre>
  <p>Fetch a specific branch from the specified remote.</p>

  <h3>Example</h3>
  <pre><code>git fetch origin
git diff main origin/main</code></pre>
  <p>After fetching, use <code>git diff</code> to compare your local branch with the remote version before merging.</p>
</section>
```

## Test Strategy

1. Open `GIT_Notes.html` in a browser and visually verify the new section renders correctly.
2. Confirm the section appears near `git pull`/`git push`.
3. Confirm all three usage forms are visible and labelled.
4. Run the file through an HTML validator (validator.w3.org) to confirm no markup errors.
5. Check that `<remote>` and `<branch>` placeholders render as literal angle-bracket text (not as HTML tags).

## Edge Cases

- Ensure no unclosed tags are introduced.
- Verify that the new section does not break existing CSS layout or styling.
- Confirm heading hierarchy is consistent (no skipped levels).
- Check that the `.plans/issue-1-plan.md` file added to the branch is either intentional or removed per team convention.