# AI safety student gallery

The standalone gallery is `public/gallery/index.html`, published at `/gallery/`, with a Flyers tab at `/gallery/flyers/`. It is deliberately not linked from the main site. It uses plain HTML and one shared stylesheet, with no JavaScript, external fonts, or runtime dependencies. The tabs are ordinary links and work without JavaScript.

“Submit yours” and “Send one in” link to the Google Form at https://forms.gle/c2aXo5JbRZ6fJLfu7. Submissions are collected through the form and are not published automatically.

## Add a photo

1. Save an optimized WebP image in `public/gallery/images/` (up to 1600 pixels wide), plus a 640-pixel-wide version named `your-photo-small.webp`.
2. Copy a `<figure>` block in `public/gallery/index.html` and change the image filenames, `srcset` widths, original `width` and `height`, descriptive `alt` text, link label, and caption. Keep `loading="lazy"` on new photos.
3. Commit and push through the website's usual publishing workflow. No gallery-specific build step is needed.

The order of the figure blocks is the display order. Clicking a photo opens the larger image using an ordinary link. To remove a photo, remove its figure block and unused image files.

## Add a flyer

Copy a figure block in `public/gallery/flyers/index.html` to add another flyer. Use image paths beginning with `/gallery/images/` so they resolve from either tab. The Flyers grid preserves each image’s natural aspect ratio so nothing is cropped. Keep captions to the official club name, linked to its website.

Edit `public/gallery/style.css` to change the appearance of both tabs. If the submission form changes, update its links on both pages.

The previous `/merch/` and `/merch/flyers/` addresses redirect to their new `/gallery/` equivalents.
