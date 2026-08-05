# Exercise: HTML Entities & Code Tag Practice
Covers lessons: 2.37, 2.38, 2.44, 2.45

## What I practiced
- Displaying special characters using HTML entities (`&lt;`, `&gt;`, `&amp;`)
- Fixing errors caused by not escaping special characters
- Using the `code` tag to display code samples correctly

## Challenges faced
- Had to escape `<` and `>` as `&lt;`/`&gt;` in `index-3.1.html` and `index-3.2.html` so the browser would display them as text instead of trying to parse them as tags — easy to forget when pasting code snippets directly into HTML.
- In `index-3.3.html`, combining `<pre>` with `<code>` was key to showing a multi-line snippet exactly as written (indentation and line breaks preserved) instead of having the browser collapse the whitespace.
- Used the named entity `&copy;` in `index-3.1.html` instead of typing the `©` character directly — a good default for special characters that aren't on a standard keyboard.
