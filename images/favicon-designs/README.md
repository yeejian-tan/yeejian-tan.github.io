# Parked favicon designs

Custom "Tine-Y" monogram marks — geometric, drawn from strokes (not tied to any
typeface), ink `#14538a`. **Not used in production**: the site currently ships no
favicon by choice.

- `tine-y-round.svg` — round stroke terminals (softer)
- `tine-y-square.svg` — square terminals + mitered junction (sharper)

## To put one into production

1. Copy the chosen file to `images/favicon.svg`.
2. Regenerate the raster sizes:

   ```sh
   rsvg-convert -w 32  -h 32  images/favicon.svg -o images/favicon-32x32.png
   rsvg-convert -w 192 -h 192 images/favicon.svg -o images/favicon-192x192.png
   rsvg-convert -w 512 -h 512 images/favicon.svg -o images/favicon-512x512.png
   # apple-touch-icon: render a full-bleed variant (rx="0") at 180x180
   # favicon.ico: combine 16/32/48 px renders, e.g. `magick f16.png f32.png f48.png images/favicon.ico`
   ```

3. Re-add the favicon `<link>`s (and a web manifest, if wanted) in `_layouts/default.html`.
