# Implementation Plan

## Approach
Locate and update the `<title>` tag in `GIT_Notes.html`. Also check for any `<h1>` or other heading elements that display the same text and update them to match.

## Files to Modify

### `GIT_Notes.html`
- Find the `<title>` tag and change its content from `Git Basics – Beginner Guide` to `Git Basics – Beginner Guide(Tushar Patil )`
- Search for any `<h1>`, `<h2>`, or other visible heading that contains the exact text `Git Basics – Beginner Guide` and apply the same update

## Implementation Steps

1. Open `GIT_Notes.html`
2. Locate the `<title>Git Basics – Beginner Guide</title>` tag and replace with `<title>Git Basics – Beginner Guide(Tushar Patil )</title>`
3. Search the file for any heading tags (`<h1>`, `<h2>`, etc.) containing `Git Basics – Beginner Guide` and update them to `Git Basics – Beginner Guide(Tushar Patil )`
4. Save the file

## Test Strategy
- Open the HTML file in a browser and verify the browser tab shows `Git Basics – Beginner Guide(Tushar Patil )`
- Verify any visible page heading also reflects the updated text

## Edge Cases
- Preserve the trailing space inside the parentheses as specified: `(Tushar Patil )` — note the space before the closing parenthesis
- Do not alter any other content in the file