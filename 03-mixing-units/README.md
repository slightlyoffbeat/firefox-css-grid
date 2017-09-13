# CSS Grid Layout
## Part 5: Mixing Units

When declaring track sizes, you can use fixed sizes with units such as `px` and `em`. You can also use flexible sizes such as percentages or the `fr` unit. The real magic of CSS Grid Layout, however, is having the ability to mix these units. The best way to understand is with an example:

```
.container {
  width: 800px;
  display: grid;
  grid-template-columns: 100px 30% 1fr;
  grid-template-rows: 200px 100px;
  grid-gap: 1rem;
}
```

Here, we have declared an 800px wide grid with three columns. The first column is a fixed width of 100px. The second column will occupy 30% of the available space, and the third column is `1fr` which means it will take up a fraction of the available space. In this case, it will take up all of the remaining space (1/1). Here is the result:

[xxxx]

**DevTools Homework**  
Inspect the grid above, and change the `grid-template-columns` property to the following: 

```
grid-template-columns: 100px 30% 2fr 1fr
```

Do you see what happened? Instead of 3 columns, you now have a 3rd column that is `2fr` and occupies 2/3 of the remaining space, and a 4th column that is `1fr` and occupies the final 1/3 of the remaining space. Continue to play around in DevTools and try different units and combinations.

When you are done, continue on to learn about how to position items on the grid.