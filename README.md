# front-end-rules
collection of best practices culled from all across the web

## HTML
#### set `html lang`, not `meta lang`
#### `img` prefers to have min- or `max-width` set in HTML, not in CSS
only for images that don't have any other style rules
this is to avoid clutter in the CSS and ease maintenance for images 

#### `img` tag should not be used for decorative images
use CSS background-image instead, according to W3

#### `a` prefers text not `img` for links
SEO thing

#### use as many specialized elements as often as possible
if it can be considered a table, make it one
helps accessibility/SEO

## CSS
### Setup
#### 1. `box-sizing: border-box`
just in case Flexbox isn't enough and some elements have to have layout specified

#### 2. set baseline font-size in `px`
```css
html, body {font-size: 20px}
```
has to be on both html and body for some reason

#### 3. set `flex-flow: <flex-direction> <flex-wrap>;`
usually flex-flow: row wrap

#### use margin for all spacing

#### optionally use padding 
only to make an element bigger or make breathing room with a border

#### rarely, use `width` and `height` last
even after min- and max-width and height
it is explicit, so it's bad for accessibility and Flexbox

### Layout

#### summary
from W3C on edX:
During its short lifetime, CSS has often played "catch up" especially with respect to layout.  Here is a short list of techniques and CSS properties used historically for layout:

tables and "slicing"
absolute positioning
floats and clear
css columns
css tables
flexbox
Except for some basic required concepts, we are going to skip all of this and go straight to flexbox. After many stumbles, flexbox finally brings sanity to the much needed world of layout in CSS.

#### `position: relative` is rarely useful
it is only to dislocate one specific thing without moving its siblings
or `z-index`, because z-index doesn't work on default position elements

#### `position: absolute` is never useful
there's always a better way

#### set all font-sizes using `rem`

#### never use `margin top:`; always use `margin bottom:`
keeps things consistent so you don't have confusion over margin math

#### `img` prefers to have min- and `max-width` set in HTML, not in CSS
only for images that don't have any other style rules
this is to avoid clutter in the CSS and ease maintenance for images 

#### `li` can have image used as bullet point
but use `background-image` rather than `list-style-image` bc `list-style-image` lacks options
