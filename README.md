# Text Image Poster

A single-page tool (`index.html`) that sets a long text in justified, newspaper-style columns and colours the letters from a hidden image, so the picture shows through the type.

Open `index.html` in a browser, then:

- **Text**: paste it, upload a `.txt` file, or drop one onto the page. A line break starts an indented paragraph; a blank line starts a new section. The type size is fitted automatically so the text fills every column.
- **Image**: upload or drop any image. It is scaled to cover the poster and sampled under each letter (or each word).
- **Colour modes**: *Accent* (saturated areas become red, orange, green, blue, etc. spot inks; everything else stays black), *Full colour* (each letter takes the image colour), and *Tone* (ink density follows image brightness).
- **Layout**: format, columns, margin, gutter, leading, typeface, ink and paper colours.
- **Download PNG** exports at print resolution (e.g. 2480×3508 for A-series).

## Bot Avatars

`bots.html` is a plain page showing the animated [Bot avatars from Libraries.dev](https://libraries.dev/bots.html) (`bot-avatars` for React). React and the library load from esm.sh through an import map, so there is no install or build step: just open the file. It shows an agent that switches between idle and working, a roster of all eighteen shapes, and the sleeping state with a few hats and glasses.
