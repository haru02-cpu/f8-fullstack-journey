# Project — Chapter 02

Graded assignment (see lesson 2.3 / 2.13 for the exact brief)

## Assignment requirements

_(Inferred from the exercise below — replace with the exact wording from lesson 2.3 / 2.13 if it differs.)_

- Recreate an existing web article as a plain HTML page, using only the tags covered in this chapter: headings (`h1`–`h3`), paragraphs, `b`/`i`/`em`/`strong`/`mark`/`u`, lists (`ul`/`ol`), links (`a`), images (`img`), and line breaks (`br`) — no CSS layout required yet, since styling hasn't been taught at this point in the course.
- Keep the document structurally valid: single `doctype`, one `html` > `head` + `body`, everything else nested inside `body`.

## What I built

- `index.html` — a full-length article ("How 60 Minutes a Day Can Change Your Life") marked up with headings, paragraphs, bold/italic/underline/`mark` emphasis, an image with a caption/credit link, and both an unordered and an ordered list.
- `style.css` — a small readability pass on top of the HTML (box-sizing reset, base font, line-height, and a centered max-width column). Not required by this chapter's brief, but a nice touch to preview what's coming in the CSS chapters.

## Known issue to fix

- A trailing `<p><strong>Cấu trúc tiêu chuẩn của HTML 5:</strong></p>` plus a `<pre><code>` block currently sit **after** the closing `</body>` tag (before `</html>`) in `index.html`. That's invalid placement — move it back inside `<body>`, or drop it if it was just scratch reference material and not meant to be part of the graded page.

## Feedback received (if any)

-
