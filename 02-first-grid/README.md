# CSS Grid Layout
## Part 2: Your First Grid


### Create a grid

The first thing we want to do is to create a grid container. We can do this by declaring `display: grid` on the container element. In this example we are using a div with the class of `container`.

### Define rows and columns

There are many ways to do define rows and columns, but for this grid we will be using the `grid-template-columns` and `grid-template-rows` properties. These properties allow us to define the size of the row and column tracks for our grid. If we want to create three fixed-height rows of 150px and three fixed-width columns of 150px, then we simply add:

```
grid-template-columns: 150px 150px 150px;
grid-template-rows: 150px 150px;
```

If you wanted to add a fourth column that is 70px wide, you could instead write:

```
grid-template-columns: 150px 150px 70px;
```

...and so on.

### Add a gutter
Adding a gutter to your grid is amazingly easy with CSS Grid Layout. Simply add:

```
grid-gap: 1rem;
```

With that simple line, you now have an equal-sized gutter between all rows and columns. If you wish to define the gutter size for columns and rows individually, you can use the `grid-column-gap` and `grid-row-gap` properties instead.

If you put that all together, you have a simple grid that was created with just a few lines of CSS:

```
.container {
  display: grid;
  grid-template-columns: 150px 150px 150px;
  grid-template-rows: 150px 150px;
  grid-gap: 1rem;
}
```

And the result:

[XXXXXXXXX]

Amazing right? Feel free to inspect the above grid with your browsers developer tools. Try changing the column width, or the row height. Swap out the `grid-gap` property with the `grid-column-gap` and `grid-row-gap` properties and play around with different widths and heights.

Having a good set of developer tools when working with CSS Grid Layout is essential. Firefox has some fantastic features that are specifically built to help you create and design grids. Intrigued? Click next to learn about Firefox's CSS Grid Layout Panel.