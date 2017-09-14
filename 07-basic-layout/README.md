# CSS Grid Layout
## Part 7: Creating a basic layout


Now that we have learned how to create a grid and position items on that grid, let's create a basic layout. We won't be introducing any new concepts here. We'll simply be using the `grid-row` and `grid-column` shorthand properties to manually place items such as a header, footer etc. 

Here is the HTML:

```
<div class="main">
    <div class="item header">header</div>
    <div class="item sidebar">sidebar</div>
    <div class="item content-1">Content-1</div>
    <div class="item content-2">Content-2</div>
    <div class="item content-3">Content-3</div>
    <div class="item footer">footer</div>
</div>
```

Here is the CSS:

```
.main {
  display: grid;
  width: 750px;
  height: 600px;
  grid-template-columns: 200px 1fr 1fr;
  grid-template-rows: 80px 1fr 1fr 100px;
  grid-gap: 1rem;
}

.header {
  grid-row: 1 / 2;
  grid-column: 1 / 4;
}

.sidebar {
  grid-row: 2 / 4;
  grid-column: 1 / 2;
}

.content-1 {
  grid-row: 2 / 3;
  grid-column: 2 / 4;
}

.content-2 {
  grid-row: 3 / 4;
  grid-column: 2 / 3;
}

.content-3 {
  grid-row: 3 / 4;
  grid-column: 3 / 4;
}

.footer {
  grid-row: 4 / 5;
  grid-column: 1 / 4;
}
```

And here is the result:

[XXXXX]

[Link for Reference](https://slightlyoffbeat.github.io/firefox-css-grid/07-basic-layout/)

[Codepen for Reference](https://codepen.io/drummerdb/pen/ayxMbL)

**Firefox DevTools Homework** 
This is the perfect time to test out the 'display line numbers' setting on the Firefox CSS Grid Layout Panel. Inspect the result above and select the layout panel. Here you can activate the overlay grid and check the box to 'display line numbers'. Handy right? This tool makes it very easy to visualize your grid when positioning items.

