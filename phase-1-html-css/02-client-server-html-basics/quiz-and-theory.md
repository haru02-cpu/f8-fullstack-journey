# Chapter 02: Quiz & Theory Notes

### Client - Server, HTML Basics — 47 lessons, 05:46:50

This file collects all the short theory/quiz-style lessons (the ones with no code to write) so they don't need a separate folder each. Fill in your own answer under each question as you go — writing it in your own words is the point, not just copying the video.

---

## Part A — Client-Server & Frontend fundamentals

- **2.4** What are the goals of the Frontend learning path?
    > _Master HTML, CSS, JavaScript, and understand how browsers work_
- **2.5** What is the Client-Server model?
    > _The client (e.g. a browser) sends a request to the server, and the server processes it and sends back a response — this request/response cycle is how the web works._
- **2.6** What are the benefits of DNS Cache?
    > _DNS caching stores domain-to-IP lookups that were already resolved, so the next time the same domain is visited the browser/OS skips the DNS lookup step and the site loads faster._
- **2.7** What are online coding tools?
    > _Browser-based editors/sandboxes for writing and running code without installing anything locally — e.g. CodeSandbox, CodePen, JSFiddle._
- **2.8** What does HTML mean?
    > _HyperText Markup Language_
- **2.9** What is hypertext?
    > _Text that contains links (hyperlinks) to other content — text, images, audio, video, etc. — letting the reader jump between pages instead of reading linearly._
- **2.11** Which HTML tag is at the top level of an HTML file?
    > _<html>_

## Part B — Images & links

- **2.16** What is the role of the `alt` attribute in the `img` tag?
    > _alt helps provide information when images don't display or for screen readers._

## Part C — Comments in HTML

- **2.20** What are comments in HTML?
    > _Comments only serve as notes, they don't show up in the browser._
- **2.23** How does the browser interpret comments?
    > _The browser won't show the comments._

## Part D — Whitespace & the `pre` tag

- **2.28** Is whitespace or line breaks collapsed in HTML?
    > _Yes — any run of multiple spaces, tabs, or line breaks in the HTML source is collapsed down to a single space when the page is rendered._
- **2.29** What does it mean when they say 'Many spaces and line breaks in HTML code are treated as just one space by the browser'?
    > _It's what lets us format/indent HTML source code freely (for readability) without that extra whitespace showing up on the actual page — the browser normalizes it away._
- **2.30** Are line breaks preserved inside the `pre` tag?
    > _Yes. `<pre>` (preformatted text) is the exception to the whitespace-collapsing rule — it preserves spaces, line breaks, and tabs exactly as written in the source._

## Part E — HTML entities & code tag

- **2.35** What does the `&lt;` symbol mean in HTML?
    > _`&lt;` is the HTML entity that renders as the literal character `<`._
- **2.36** How do you identify a valid HTML entity?
    > _It's a code that starts with `&` and ends with `;` — either a named entity (`&lt;`, `&amp;`, `&copy;`) or a numeric one (`&#60;`, `&#x3C;`)._
- **2.39** What is "HTML escaping"?
    > _Replacing characters that have special meaning in HTML — `<`, `>`, `&` — with their entity codes (`&lt;`, `&gt;`, `&amp;`) so they display as plain text instead of being parsed as markup._
- **2.40** What is the purpose of HTML entities?
    > _They let you display characters that would otherwise be interpreted as HTML syntax (like `<` and `>`), or characters that are hard to type directly (like `&copy;` or `&nbsp;`), by encoding them as text the parser treats literally._
- **2.43** Which tag is used to wrap computer code?
    > _The `<code>` tag — it marks up a snippet of computer code and is usually combined with `<pre>` when the whitespace/line breaks of that code need to be preserved too._

---

## 🎬 Video lessons watched (check off as you go)

- [x] 2.2 Client - Server, HTML Basics (04:10:33)
- [x] 2.3 Homework introduction (09:08)
- [x] 2.13 Introducing the challenge exercise (02:57)
- [x] 2.26 The `ul` and `ol` tags (08:00)
- [x] 2.27 How browsers display whitespace (03:46)
- [x] 2.31 Learning about the `pre` tag (03:44)
- [x] 2.34 Learning about HTML entities (08:56)
- [x] 2.41 The `code` tag and code highlighting (12:09)
- [x] 2.42 Search mindset when using libraries (11:04)
- [x] 2.46 Sharing tips for writing better HTML (11:21)
- [x] 2.47 Chapter summary (01:00)
