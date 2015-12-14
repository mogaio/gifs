Testing in-browser gif generation from an SVG with [gif.js](https://github.com/jnordberg/gif.js/) and [canvg](https://github.com/gabelerner/canvg).

Uses canvg to render out each "frame" of the SVG to an in-between canvas, so styling via CSS is still a little iffy.  [Rendering more directly](http://bl.ocks.org/veltman/1071413ad6b5b542a1a3) seems like it makes more sense. The only upside to this is that the frames can be added synchronously, before the browser paints at all.  At the very least, would need to add [SVG Crowbar](https://github.com/NYTimes/svg-crowbar)-style traversal with explicit styling in before the canvas conversion.