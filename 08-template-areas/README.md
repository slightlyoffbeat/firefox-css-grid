# CSS Grid Layout
## Part 8: Template Areas

In our previous example, we learned how to create a basic layout by positioning items with grid lines. Another method for positioning items is to use named grid areas with the `grid-template-areas` and `grid-area` properties. The best way to explain this is with example. Let's recreate the grid from our previous example with the `grid-template-areas` property:

```
.container {
  display: grid;
  width: 750px;
  height: 600px;
  grid-template-columns: 200px 1fr 1fr;
  grid-template-rows: 80px 1fr 1fr 100px;
  grid-gap: 1rem;
  grid-template-areas:
      "header header header"
      "sidebar content-1 content-1"
      "sidebar content-2 content-3"
      "footer footer footer";
}
```

Here we have defined 3 columns and 4 rows. Instead of placing each individual item, we can define the entire layout using the `grid-template-areas` property. We can then assign those areas to each of our grid items using the `grid-area` property.

HTML:
```
<div class="container">
    <div class="item header">header</div>
    <div class="item sidebar">sidebar</div>
    <div class="item content-1">Content-1</div>
    <div class="item content-2">Content-2</div>
    <div class="item content-3">Content-3</div>
    <div class="item footer">footer</div>
</div>
```

CSS:
```
.header {
  grid-area: header;
}

.sidebar {
  grid-area: sidebar;
}

.content-1 {
  grid-area: content-1;
}

.content-2 {
  grid-area: content-2;
}

.content-3 {
  grid-area: content-3;
}

.footer {
  grid-area: footer;
}
```

And here is the result:

[XXXX]

[Link for Reference](https://slightlyoffbeat.github.io/firefox-css-grid/08-template-areas/)

[Codepen for Reference](https://codepen.io/drummerdb/pen/BdEbKX)

This example only touches on what is possible with grid template areas. [Check out MDN](https://developer.mozilla.org/docs/Web/CSS/CSS_Grid_Layout/Grid_Template_Areas) for more detailed documentation.

**Firefox DevTools Homework**  
Did you know that FireFox DevTools can display the area names? Try it out! Inspect the grid above and open the layout panel. From here you can toggle the overlay grid and the 'Display Area Names' feature.