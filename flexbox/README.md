
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
Flex has 2 axis, main and cross axis. Axis are affected by flex-direction, by default flex-direction is row. When the flex-direction is row the main axis goes from left to right across the screen and the cross axis is from top to bottom. When flex-direction is changed to column the axises switch. Main is now top to bottom and cross is now left to right. This is extremely important as some flex properties only affect certain axises. For example:
- justify-content affects the main axis
- align-items affects the cross axis

Flex container properties:
  - display: flex | inline-flex
  - flex-direction: row | column - Default is row
  - align-items: flex-start | center | flex-end | stretch*
  - justify-content: flex-start* | center | flex-end | space-between | space-around (margins on side)
     - This is centering horizontally.
  - flex-wrap: wrap (wrap flex items around when they can no longer shrink)
   

Flex item properties:
  - flex: 2, take up 2x as much spaces as rest of elements, flex: 3, take up 3x as much space etc...
    - flex [flex-grow-rate] [flex-strink-rate] [flex-basis] (shorthand)
  - flex-grow is a way of defining how many columns we want an element to take up
    - e.g. flex-grow of (4, 6, 2) on 3 elements would be like a bootstrap grid of 12. (2, 3, 1) could also be used as its a rate.
  - flex-shrink is a way of telling your elements to shrink at a certain rate when the browser is resized.
  - flex-basis: better way to define widths for columns (alternative to width), width will not strink whereas flex-basis will so there will be less chance of horizontal scrollbars.
  - order: 1 will be placed at the start, this can be used to rearrange elements without editing the html although this is not a good idea due to accessibility.  

  