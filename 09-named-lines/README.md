# CSS Grid Layout
## Part 9: Named Lines

In a previous example, we learned how to place an item on the grid by providing the `grid-column` and `grid-row` properties with specific grid lines. You can also name some or all of your lines when you define your grid. This allows you to use those names instead of grid lines. 

To name a grid line, you simply provide the name in square brackets:

```
.container {
  display: grid;
  width: 750px;
  height: 600px;
  grid-gap: 1rem;
  grid-template-columns:
    [main-start sidebar-start] 200px
    [sidebar-end content-start] 1fr
    [column3-start] 1fr
    [content-end main-end];
  grid-template-rows:
    [row1-start] 80px
    [row2-start] 1fr
    [row3-start] 1fr
    [row4-start] 100px
    [row4-end];
}
```

Now that we have line names, we can use those names when placing items. Lets recreate our basic layout using named lines, instead of line numbers:

```
.header {
  grid-column: main-start / main-end;
  grid-row: row1-start / row4-end;
}

.sidebar {
  grid-column: sidebar-start / sidebar-end;
  grid-row: row2-start / row4-start;
}

.content-1 {
  grid-column: content-start / content-end;
  grid-row: row2-start / row3-start;
}

.content-2 {
  grid-column: content-start / column3-start;
  grid-row: row3-start / row4-start;
}

.content-3 {
  grid-column: column3-start / content-end;
  grid-row: row3-start / row4-start;
}

.footer {
  grid-column: main-start / main-end;
  grid-row: row4-start / row4-end;
}
```

And here is the result:

[ XXXXX ]

**Firefox DevTools Homework**  
Did you know you can customize the color of the grid overlay in Firefox DevTools? The above example is dark, and the default purple may not be the best color to use. When selecting an overlay grid to display, you will see a circle next to the grid name that indicates the color of the overlay. Click on that circle, and you can customize the color to whatever you'd like. Try a different color, such as white.
