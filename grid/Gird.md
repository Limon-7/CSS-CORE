## CSS-GRID

### 1# Grid container

We create a grid container by declaring display: grid or display: inline-grid on an element. As soon as we do this, all direct children of that element become grid items.

- diplay:grid= create a block level grid container.
- diplay:inline-grid= create a inline-grid level container.

#### 1.1# Grid Tracks

We define rows and columns on our grid with the grid-template-columns and grid-template-rows properties. These define grid tracks. A grid track is the space between any two lines on the grid.

#### 1.2# Grid Line

The grid lines represent the vertical columns (column grid lines) and horizontal (row grid lines).

There are two properties grid-template-columns and grid-template-rowsthat are used to define the grid lines of the layout.

#### 1.3# Grid Cell

This is the smallest area within the grid layout which is the space defined by four grid lines.

#### 1.4# Implicit and explicit grid:

When creating column tracks with the grid-template-columns property, but the grid also created rows on its own.It is called implicit grid.

But when we delacerd grid-temple-columns or grid-templete-rows then it is called explicit grid.

#### 1.5# Gutters:

Gutters or alleys are spacing between content tracks.
gird-column-gap:1rem
grid-row-gap:1rem
shortend: grid-gap:1rem

#### 1.6# Subgrid:

which would let us create nested grids that use the track definition of the parent grid.

#### 1.7# Justify Items:

Aligns grid items along the inline (row) axis (as opposed to align-items which aligns along the block (column) axis). This value applies to all grid items inside the container.

- start – aligns items to be flush with the start edge of their cell
- end – aligns items to be flush with the end edge of their cell
- center – aligns items in the center of their cell
- stretch – fills the whole width of the cell (this is the default)

#### 1.8# Align Items:

Aligns grid items along the block (column) axis (as opposed to justify-items which aligns along the inline (row) axis). This value applies to all grid items inside the container.

- align-items: start|end|center|stretch

#### 1.9# Justify Content:

It can set the alignment of the grid within the grid container.It set the whole gird content along with grid container with main axis(row).

- justify-content: start | end | center | stretch | space-around | space-between | space-evenly;

#### 1.10# Align Content:

It can set the alignment of the grid within the grid container.It set the whole gird content along with grid container with cross axis(column).

- align-content: start | end | center | stretch | space-around | space-between | space-evenly;

#### 1.11# Place Content:

place-content sets both the align-content and justify-content properties in a single declaration.

- place-content:align-content justify-content

#### 1.12# Grid Auto Flow:

the auto-placement algorithm kicks in to automatically place the items. This property controls how the auto-placement algorithm works.

- grid-auto-flow:|row|column|dense

- row – tells the auto-placement algorithm to fill in each row in turn, adding new rows as necessary (default)
- column – tells the auto-placement algorithm to fill in each column in turn, adding new columns as necessary
- dense – tells the auto-placement algorithm to attempt to fill in holes earlier in the grid if smaller items come up later

### #2# Sizing Individual Grid Items:

Determines a grid item’s location within the grid by referring to specific grid lines.

- grid-column-start
- grid-column-end
- grid-row-start
- grid-row-end: <number> | <name> | span <number> | span <name> | auto;

**grid-column: grid-column-start/grid-column-end**
**grid-row: grid-row-start/grid-row-end**

#### 2.1# Grid Area

Items can span one or more cells both by row or by column, and this creates a grid area. Grid areas must be rectangular.
**grid-area:grid-row-start/grid-column-start/grid-row-end/grid-column-end**

#### 2.2# Justify-self:

justify-self apply with grid items.

- justify-self:start|end|center|stretch

#### 2.3# Align Self:

align-self applies with grid items.

- align-self: start|end|center|stretch|

#### Properties have no effect on grid children:

float, display: inline-block, display: table-cell, vertical-align and column-\* properties have no effect on a grid item.
