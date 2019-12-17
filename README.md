# front-end-rules
collection of best practices culled from all across the web

## HTML
#### set `html lang`, not `meta lang`
#### `img` prefers to have width set in HTML, not in CSS
only for images that don't have any other style rules
this is to avoid clutter in the CSS and ease maintenance for images 

## CSS
### Setup
#### 1. set baseline font-size in `px`
```css
html, body {font-size: 20px}
```
has to be on both html and body for some reason

### Layout
#### set all font-sizes using `rem`

#### never use `margin top:`; always use `margin bottom:`
keeps things consistent so you don't have confusion over margin math

#### `img` prefers to have width set in HTML, not in CSS
only for images that don't have any other style rules
this is to avoid clutter in the CSS and ease maintenance for images 

#### `li` can have image used as bullet point
but use `background-image` rather than `list-style-image` bc `list-style-image` lacks options
