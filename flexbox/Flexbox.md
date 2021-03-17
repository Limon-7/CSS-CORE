## FLEXBOX

#### 1# Flexbox Container:

CSS that can be applied to the container

```
display: flexbox | inline-flex;
flex-direction: row | row-reverse | column | column-reverse;
flex-wrap: nowrap | wrap | wrap-reverse;
flex-flow: <‘flex-direction’> || <‘flex-wrap’>
justify-content: flex-start | flex-end | center | space-between | space-around;
align-items: flex-start | flex-end | center | baseline | stretch;
align-content: flex-start | flex-end | center | space-between | space-around | stretch;
```

#### 1.1 display:flex

display: flex is tells your browser, "I wanna use flexbox with this container, please."

A div element defaults to display:block.
**display:flex|inline-flex**

- flex:
- inline-flex:Displays an element as an inline-level flex container.

#### 1.2 flex-direction

flex-direction allows you to control how the items will display in the container.

#### 1.3 flex-wrap

Flexbox by default will try to fit all elements into one row. However, you can change this with the flex-wrap property. There are three values you can use to determine when elements go to another row.
**flex-wrap: nowrap:**This will cause everything to stay in one row from left to right.
**flex-wrap:wrap:**wrap will allow items to pop to the next row if there is not enough room on the first row. The items will be displayed from left to right.
**flex-wrap: wrap-reverse:** also allows items to pop to the next row but this time the items are displayed from right to left.

#### 1.4 flex-flow:

flex-flow combines the use of flex-wrap and flex-direction into one property. It is used by first setting the direction and then the wrap. Here is an example: **flex-flow: column wrap;**

#### 1.5 Justify Content

justify-content is a property to align items in the container along the main axis.
justify-content: flex-start | flex-end | center | space-between | space-around | space-evenly | start | end | left | right ... + safe | unsafe;

#### 1.6 align-items

align-items allows us to align items along the cross axis.
**align-items: stretch | flex-start | flex-end | center | baseline | first baseline | last baseline | start | end | self-start | self-end + ... safe | unsafe;**

- baseline: items are aligned such as their baselines align
- For stretch to work how you would expect, the height of the elements must be set to auto instead of a specific height.

#### 1.7 align-content

align-content is used for aligning items with multiple lines. It is for aligning on the cross axis and will have **no effect on content that is one line**.

**align-content: flex-start | flex-end | center | space-between | space-around | space-evenly | stretch | start | end | baseline | first baseline | last baseline + ... safe | unsafe;**

## 2#Properties for the Children(flex items)

#### CSS that can be applied to items/elements in the container

```
order: <integer>;
flex-grow: <number>; /* default 0 */
flex-shrink: <number>; /* default 1 */
flex-basis: <length> | auto; /* default auto */
flex: none | [ <'flex-grow'> <'flex-shrink'>? || <'flex-basis'> ]
align-self: auto | flex-start | flex-end | center | baseline | stretch;
```

#### 2.1 Align Self

align-self allows you to adjust the alignment of a single element.

It has all the same properties of align-items.

#### 2.2 Order:

How an flex item will be ordered. Defalut value 0. All flex item takes deafult value.
**order:1 ; //default:0**

#### 2.3 Flex Grow:

How an items will take extra spaces.
**flex-grow:4;//default:0**

#### 2.4 Flex Shirnk:

How flex items will shrink if screen resize.
**flex-shrink:3; //default:1**

**Note: flex:1 1 0 that is the shortend property respectively of flex-grow flex-shrink flex-basis**

#### 2.5 Flex-basis:

The flex-basis property defines the size of the flex-item along the main axis of the flex container.
**flex-basis: auto | content | <width> | <height>;//default:auto**

- flex-basis: auto: looks up the main size of the element and defines the size. For example, on a horizontal flex container, auto will look for width and height if the container axis is vertical.

- flex-basis: content resolves the size based on the element’s content, unless width or height is set through normal box-sizing.

**In both the cases where flex-basis is either auto or content, if main size is specified, that size will take priority.**

#### 2.6 flex:

This is the shorthand for flex-grow, flex-shrink and flex-basis combined.
**flex:flex-grow flex-shrink flex-basis**

## Note that float, clear and vertical-align have no effect on a flex item.
