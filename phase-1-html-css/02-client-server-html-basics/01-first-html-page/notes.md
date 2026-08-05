# Exercise: My First HTML Page

Covers lessons: 2.10, 2.12, 2.14, 2.15, 2.17, 2.18, 2.19

## What I practiced

- Declaring the HTML5 doctype
- Completing the opening tags and full file structure
- Adding an image with the `img` tag
- Basic `a` (anchor) tag
- Placing an image inside a link

## Challenges faced

- In `index-1.2.html`, the `img` `src` URL got broken across two lines by the editor, leaving a stray newline right before the closing quote. It still works (browsers strip embedded tabs/newlines out of URLs), but it's a reminder to keep long attribute values on one line, or reformat carefully.
- Left `alt=""` on the images in `index-1.2.html` and `index-1.3.html`. That's correct for decorative images, but for a meaningful image — like the clickable YouTube thumbnail in `index-1.3.html` — the `alt` text should actually describe it, both for accessibility and for when the image fails to load.
- `index-1.3.html` correctly uses `lang="vi"` since its content is a Vietnamese blog post, while `index-1.1.html`/`index-1.2.html` use `lang="en"` — good practice to match `lang` to the actual page content.
