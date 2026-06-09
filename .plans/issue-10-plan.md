# Implementation Plan

## Approach
Locate all occurrences of the text `Git Basics – Beginner Guide` in `GIT_Notes.html` and replace them with `Git Basics – Beginner Guide by Tushar`. This includes the `<title>` tag in the `<head>` section and any visible heading elements in the `<body>` that display the same text.

## Files to Modify

### `GIT_Notes.html`
- Find the `<title>` tag and update its content:
  - **Before:** `<title>Git Basics – Beginner Guide</title>`
  - **After:** `<title>Git Basics – Beginner Guide by Tushar</title>`
- Find any heading tags (e.g., `<h1>`, `<h2>`) containing `Git Basics – Beginner Guide` and update their text:
  - **Before:** `Git Basics – Beginner Guide`
  - **After:** `Git Basics – Beginner Guide by Tushar`

## Implementation Steps
1. Open `GIT_Notes.html`.
2. Search for all occurrences of `Git Basics – Beginner Guide` (note: the dash may be an en-dash `–` or a regular hyphen `-`; match exactly).
3. Replace each occurrence with `Git Basics – Beginner Guide by Tushar`.
4. Save the file.
5. Verify the change renders correctly by opening the file in a browser.

## Edge Cases
- Ensure the en-dash character (`–`) is preserved and not accidentally converted to a hyphen or double-dash.
- Check for any meta tags (e.g., `og:title`, `twitter:title`) that may also contain the title text and update those as well.

## Test Strategy
- Open the updated HTML file in a browser and confirm the browser tab shows `Git Basics – Beginner Guide by Tushar`.
- Confirm any visible heading on the page also reflects the updated title.
