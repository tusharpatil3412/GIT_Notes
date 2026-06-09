# Implementation Plan

## Approach
Open `GIT_Notes.html` and locate the `<title>` element in the `<head>` section. Replace the existing title text with the new value. Also check for any `<h1>`, `<h2>`, or other visible heading elements that display the same text and update them consistently if present.

## Files to Modify

### `GIT_Notes.html`
- Find: `<title>Git Basics – Beginner Guide</title>`
- Replace with: `<title>Git Basics – Beginner Guide(Tushar Patil)</title>`
- Additionally scan for any visible heading (`<h1>`, `<h2>`, etc.) containing the same text and apply the same change for UI consistency.

## Implementation Steps
1. Open `GIT_Notes.html`.
2. Search for the string `Git Basics – Beginner Guide` (note the en-dash `–`).
3. Append `(Tushar Patil)` to each occurrence that should be updated (at minimum the `<title>` tag).
4. Save the file.
5. Open the file in a browser and verify the browser tab shows the new title.

## Edge Cases
- The en-dash (`–`) vs hyphen (`-`) must be preserved exactly as-is.
- If the title text appears in a `<meta>` tag (e.g. `og:title`) it should be updated as well for consistency.
- No spacing before `(` per the issue description.

## Test Strategy
- Open the updated HTML file in a browser and confirm the tab title reads `Git Basics – Beginner Guide(Tushar Patil)`.
- Inspect the DOM to verify `document.title` returns the correct string.
