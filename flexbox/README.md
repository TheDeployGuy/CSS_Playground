
#CSS
BEM - Block Element Modifer is a way of naming your CSS classes.

Block - is a standalone component that is reuseable across a project or even between projects.
Element - Elements make no sense being along, they are tightly connected to their parent which are blocks.
Modifier - is a Flad added to block or element to make it more specific. They usually contain rules like color or size
```css
   /* Styling the Block component e.g. Card, Nav */
  .block {}
  (e.g: .btn)
  /* Styling the element of a block e.g. card__item, nav__item */
  .block__element {}
  (e.g: .btn__text)
  /* Styling the modifier of an element e.g. card__item--success, nav__item--big */
  .block__element--modifier {}
  (e.g: .btn--big)
```

#Flexbox - allows you to arrange items within a contiainer

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

#Grid CSS 

A grid is divided into columns and rows these together in CSS grid are called Tracks. Elements can be places anywhere in the grid.

Grid is like flexbox in that if you make a container ```display:grid``` all its direct children become grid-items. You can customize how your grid appears in a variety of ways one of them being ```grid-template-columns``` e.g ```grid-template-columns: 100px 100px 100px;``` would create a grid with 3 columns each 100px width. You can specify your columns values in rem, px or percentages(with percentages you should be using the fr unit.) ```grid-template-rows``` is the same but for rows instead of columns

By default grid items will be directly next to each other with no margin or padding, to create gaps between your grid items you can use the ```grid-gap``` property on the container.

explicit grid - Solid lines are explicit grid in dev tools, you explicitally set that number of columns or rows.
implicit grid - Dashed lines are implicit grid in dev tools, implicit lines appear when you haven't set a specific value for a column or row. For example if you had just set the ```grid-template-columns``` property all your rows would be implicit.

You can set the size of implicitally created rows/columns by using the ```grid-auto-rows or grid-auto-columns``` property.

By default any extra content will go into a new row not a new column to specifically tell it to use a column instead of a row you need to use the ```grid-auto-flow: column``` css property.

## Sizing in CSS Grid

fr unit/fractional unit is telling CSS to use xfr the available space for an element. Instead of using pixels are percentages we can use this unit to best place items in the grid. ```grid-template-columns: 1fr 1fr``` will result in a two column grid where each item is taking up 1 fraction of the available space. Instead specific setting each column the ```repeat()``` function can be used to make it easier e.g.: a 4 column layout would look like ```repeat(4, 1fr)```.

## Sizing Grid Items
Since Grid is a grid if you set explicit width or heights e.g.: ```width:300px``` for a certain item everything item in that column will be set to 300px not just the element you set. This is a very common occurance when you are using fr units as css grid will place all the items set the width then use the free space for the rest. Now that is annoying so CSS has a way to give grid items a specific size and this way is called spanning. Spanning can be set using the ```span``` property on ```grid-column or grid-row``` e.g: ```grid-column: span 2``` means the item will span 2 columns.

## Placing Grid Items
```grid-column-start and grid-column-end``` can be used to specific set where on your grid you want to place your items. It uses the track numbers so ```grid-column-start:2 + grid-column-end:5``` would start the item at 2 and end it at 5. There is a shorthand for this which is ```grid-column: 2 / 5```. Above applied to rows as well ```grid-row*```. You can use ``` 1 / -1``` for the setting to span it across the entire width or height of the grid. 1 / -1 will only work when you have explicially set the grid-template columns and rows.

