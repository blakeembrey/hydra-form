# Hydra Grid

Simple CSS grid utilizing the `inline-block` and `box-sizing` properties for awesome layouts. It can easily be dropped in over the top of another CSS grid and can be used to size any element to the grid widths.

## Installation

```
$ npm install hydra-grid --save
$ bower install hydra-grid --save
$ component install blakeembrey/hydra-grid
```

## Stylus API

```
// Support for old IE - currently enables the `rem` to `px` fallback for IE8
support-for-ie = true

// Grid system configuration
grid-prefix       = "grid" // Prefix all grid classes with this variable (disabled with Bootstrap support)
grid-alignment    = left // Alignment of the grid columns within a grid row
grid-gutter-width = 1.5rem // Gutter spacing between grid columns
grid-force-suffix = false // Force the suffix for single column count grids

grid-generate(columns, prefix)


grid-generate(6 12)

// Results in two grids
.grid-(col|push|pull|prefix|suffix)([0-6])of6
.grid-(col|push|pull|prefix|suffix)([0-12])of12

grid-prefix = "" // Disable grid class prefixing

grid-generate(12)

// Results in a single unprefixed grid without the `of(x)` syntax
.(col|push|pull|prefix|suffix)([0-12])

grid-prefix = "grid"

grid-generate(12, "desktop")

// Results in a grid prefixed and class prefixed grid output
.grid-desktop-(col|push|pull|prefix|suffix)([0-12])
```

## CSS API

```
.grid-container /* Use this class for the page container */
.grid-row /* Use this class to mark up a grid row */
.grid-col-(x) /* This element span 100% / 12 * `x` width */
.grid-(push|pull)-(x) /* Use these classes to rearrange markup for SEO or device context */
.grid-(prefix|suffix)-(x) /* Use these classes to prepend or append `x` width worth of whitespace */
```

By default the CSS grid is built for a single viewport and twelve columns. Using the Stylus API you can easily generate a number of different grid columns at different viewport sizes.

## License

MIT
