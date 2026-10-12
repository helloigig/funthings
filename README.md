# Text Image Poster

A single-page tool (`index.html`) that sets a long text in justified, newspaper-style columns and colours the letters from a hidden image, so the picture shows through the type.

Open `index.html` in a browser, then:

- **Text**: paste it, upload a `.txt` file, or drop one onto the page. A line break starts an indented paragraph; a blank line starts a new section. The type size is fitted automatically so the text fills every column.
- **Image**: upload or drop any image. It is scaled to cover the poster and sampled under each letter (or each word).
- **Colour modes**: *Accent* (saturated areas become red, orange, green, blue, etc. spot inks; everything else stays black), *Full colour* (each letter takes the image colour), and *Tone* (ink density follows image brightness).
- **Layout**: format, columns, margin, gutter, leading, typeface, ink and paper colours.
- **Download PNG** exports at print resolution (e.g. 2480×3508 for A-series).

# Jelly Bag

`jelly-bag/index.html` is a single self-contained page: an interactive 3D jelly tote, simulated and rendered live in the browser with WebGPU and WGSL. It needs a browser with WebGPU (current Chrome/Edge, Safari 26, Firefox with WebGPU enabled). If WebGPU isn't available, the page says so and doesn't fall back to another renderer.

- **Physics**: a volumetric XPBD soft body. The thick walls, gusseted base and rolled rim are one layer of hexahedra split into about 2,000 tetrahedra, with distance and volume constraints. A one-sided cavity-pressure constraint keeps the bag puffy. Handles are separate stiffer chains attached to the rim. Edge damping, ground contact with friction, fixed 1/120 s steps.
- **Rendering**: the smooth surfaces, glitter, bubbles, rings and rivets are embedded in the deforming cells. WGSL passes handle thickness-based absorption, a depth-peeled inside back wall, screen-space refraction with slight dispersion, Fresnel reflections of studio soft boxes, and a tinted soft contact shadow.
- **Interaction**: drag the bag to grab, stretch, squash or swing it. Scroll, press Q/E, or use a second finger while holding to twist. Drag the background to orbit. Space pauses and R resets.
