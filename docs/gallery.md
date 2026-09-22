# AI safety student gallery

The standalone gallery is `public/gallery/index.html`, published at `/gallery/`, with a Flyers tab at `/gallery/flyers/`. It is deliberately not linked from the main site. It uses plain HTML and one shared stylesheet, with no JavaScript, external fonts, or runtime dependencies. The tabs are ordinary links and work without JavaScript.

“Submit yours” opens an email to `harrywatermanb@gmail.com`, the contact address on the homepage, with fields for group name, category, and optional credits. Visitors attach their images manually. Submissions arrive in email and are not published automatically. This requires a configured email app; there is no upload service or database.

## Add a photo

1. Save an optimized WebP image in `public/gallery/images/` (up to 1600 pixels wide), plus a 640-pixel-wide version named `your-photo-small.webp`.
2. Copy a `<figure>` block in `public/gallery/index.html` and change the image filenames, `srcset` widths, original `width` and `height`, descriptive `alt` text, link label, and caption. Keep `loading="lazy"` on new photos.
3. Commit and push through the website's usual publishing workflow. No gallery-specific build step is needed.

The order of the figure blocks is the display order. Clicking a photo opens the larger image using an ordinary link. To remove a photo, remove its figure block and unused image files.

## Add a flyer

Replace the empty-state paragraph in `public/gallery/flyers/index.html` with a `<div class="gallery">` containing figure blocks like the Merch page. Use image paths beginning with `/gallery/images/` so they resolve from either tab. For portrait flyers, override `aspect-ratio` on the image (for example `style="aspect-ratio: 2 / 3"`); keep `object-fit: contain` so nothing is cropped.

Edit `public/gallery/style.css` to change the appearance of both tabs. If the submission address changes, update the mail links on both pages.

The previous `/merch/` and `/merch/flyers/` addresses redirect to their new `/gallery/` equivalents.
