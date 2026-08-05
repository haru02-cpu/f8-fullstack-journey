# Daily Progress — Chapter 02

Track what you actually did each day. One entry per day, however small.

---

## Day 1 — 01/08/2026

- [x] Watched: 2.1–2.9 (intro + Client-Server theory)
- [x] Answered quiz questions in `quiz-and-theory.md` (Part A)
- [x] Coded: `01-first-html-page/`
- **Notes / difficulties:**
    - In `index-1.2.html`, the `img` `src` got line-broken by the editor and ended up with a stray newline inside the URL string, right before the closing quote. Browsers tolerate it (the URL parser strips embedded tabs/newlines), but it's a good reminder to keep attribute values on one line or double-check auto-formatting.
    - Left `alt=""` on content images (1.2, 1.3). Empty `alt` is correct for purely decorative images, but for an image that carries meaning (like the linked YouTube thumbnail in 1.3) it should describe the image instead.

## Day 2 — 02/08/2026

- [x] Watched: 2.10–2.19 (images, links)
- [x] Answered quiz questions (Part B)
- [x] Coded: continued `01-first-html-page/`
- **Notes / difficulties:**
    - Practiced wrapping an `img` inside an `a` tag (index-1.3.html) to make an image clickable — straightforward once the nesting order is clear (`<a><img /></a>`).

## Day 3 — 03/08/2026

- [x] Watched: 2.20–2.33 (comments, whitespace, `pre` tag)
- [x] Answered quiz questions (Part C, D)
- [x] Coded: `02-html-comments-practice/`
- **Notes / difficulties:**
    - Comments (`<!-- -->`) hide content from the rendered page but are still visible in View Source / dev tools — worth remembering they're not a way to hide sensitive data, just a note-to-self or a way to temporarily disable markup.

## Day 4 — 04/08/2026

- [x] Watched: 2.34–2.47 (entities, code tag, summary)
- [x] Answered quiz questions (Part E)
- [x] Coded: `03-html-entities-code-tag/`
- [x] Coded: `project/`
- **Notes / difficulties:**
    - Used `&lt;`, `&gt;`, and `&copy;` entities, and combined `<pre>` + `<code>` to display a raw HTML snippet without the browser rendering it as real markup.
    - In `project/index.html`, a leftover `<p>` and `<pre><code>` block ended up placed _after_ `</body>` (before the closing `</html>`) — invalid placement. Worth moving that content back inside `<body>` (or removing it if it was just scratch reference material) next time this file is touched.

---

**When the chapter is fully done:** go back to the root `README.md` and check the box for Chapter 02.
