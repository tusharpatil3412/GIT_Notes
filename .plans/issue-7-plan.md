# Implementation Plan

## Approach
Open `GIT_Notes.html` and locate the `<title>` element in the `<head>` section. Replace the existing title text with the new value. Also check for any `<h1>` or other heading tags that display the same title text on the page and update them consistently.

## Files to Modify
- `GIT_Notes.html` — update the page title and any matching visible headings

## Implementation Steps
1. Open `GIT_Notes.html`.
2. Find the `<title>` tag in the `<head>` section:
   ```html
   <title>Git Basics – Beginner Guide</title>
   ```
   Change it to:
   ```html
   <title>Git Basics – Beginner Guide(Tushar Patil )</title>
   ```
3. Search the rest of the file for any `<h1>`, `<h2>`, or other elements that render the same text ('Git Basics – Beginner Guide') and apply the same update for consistency.
4. Save the file.

## Edge Cases
- The em dash character (`–`) should be preserved exactly as-is (not replaced with a hyphen).
- Preserve any trailing space inside the parentheses as specified: `(Tushar Patil )`.

## Test Strategy
- Open the updated HTML file in a browser and verify the browser tab shows 'Git Basics – Beginner Guide(Tushar Patil )'.
- Verify any on-page heading also reflects the updated title if it was changed.