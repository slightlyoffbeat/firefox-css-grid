# CSS Grid Layout
## Part 6: Position Items on the Grid


### Understanding Grid Lines

Now that we are comfortable creating a grid and defining the row and column sizes, we can move on to placing items on this grid. There are several ways to place items, but we will start with a basic example. Consider a simple 3x2 grid:

[ image needed ]


Each item within this grid will be placed automatically in the default order. 

If we wish to have greater control, we can position items on the grid using grid line numbers. Grid lines are numbered left to right and top to bottom (if you are working in a right-to-left language, then grid lines are numbered right to left). The above example would be numbered like so:

[ image needed ]

### Position an item

Say we want to position our first grid item (with a class of `item1`) to be in the second row and occupy the second column. This item will need to start at the second row line, and span to the third row line. It will also need to start at the second column line and span to the third column line. We could write our CSS like so:

```
.item1 {
    grid-row-start: 2;
    grid-row-end: 3;
    grid-column-start: 2;
    grid-column-end: 3;
}
```

### Shorthand Property

We can also rewrite this with shorthand properties:

```
.item1 {
    grid-row: 2 / 3;
    grid-column: 2 / 3;
}
```

Here is the result:

[XXXXX]

[Link for Reference](https://slightlyoffbeat.github.io/firefox-css-grid/06-position-items/)

[Codepen for Reference](https://codepen.io/drummerdb/pen/GvLYmd)

**Firefox DevTools Homework**  
Try changing the `grid-row` property of `item1` to the following:

```
.item1 {
    grid-row: 3 / 4;
    grid-column: 1 / 3;
}
```

See what happened? The item spanned multiple columns from grid line 1 to 3. It also was placed between grid row lines 3 and 4 which results in a new row being created. This new row is an implicit row, and its height is set by the `grid-auto-rows` property on the parent grid. You can learn more about default rules for auto-placement on [MDN](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Grid_Layout/Auto-placement_in_CSS_Grid_Layout#Default_rules_for_auto-placement).

Now let's put this new knowledge to work by creating a basic layout.

