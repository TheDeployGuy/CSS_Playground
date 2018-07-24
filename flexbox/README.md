
Flexbox - allows you to arrange items within a contiainer

[Video #1](https://www.youtube.com/watch?v=JJSoEo8JSnc)
[Video #2](https://www.youtube.com/watch?v=Y8zMYaD1bz0)

- Do not have to use Floats to arrange elements
- Responsive and Mobile Friendly
- Order of elements can be changed without the changing the source HTML.
- Allows us to control the position, size and space of elements relative to their parent elements and each other.

# Benefits
- Navigation bars + Menus
- Grid layouts
- Bar Charts
- Equal height columns

# Concepts
- Alter width and height to best git in its containers
- Flexbox is direction-agnostic
- Used for small-scale layouts

Flex containers contain flex items.
Flex has 2 axis, main and cross axis.

Flex container properties:
  - display: flex | inline-flex
  - flex-direction: row | column - Default is row
  - align-items: flex-start | center | flex-end | stretch*
  - justify-content: flex-start* | center | flex-end | space-between | space-around (margins on side)
  - flex-wrap: wrap (wrap flex items around)

Flex item properties:
  - flex: 2, take up 2x as much spaces as rest of elements, flex: 3, take up 3x as much space etc...
  - order: 1 will be placed at the start, this can be used to rearrange elements without editing the html although this is not a good idea due to accessibility. 
  - flex-basis: better way to define widths for columns

  