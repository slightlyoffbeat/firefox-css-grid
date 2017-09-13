# CSS Grid Layout
## Part 4: The fr Unit.

### The fr Unit
In our first grid, we created columns with a fixed px width. That's great, but it isn't very flexible. Thankfully, CSS Grid Layout introduces a new unit of length called `fr` (short for fraction). MDN defines the `fr` unit as a unit which "represents a fraction of the available space in the grid container". Lets say we want to create rewrite our previous grid to be 800px wide with three equal width columns. We could write as:

```
.container {
  display: grid;
  width: 800px;
  grid-template-columns: 1fr 1fr 1fr;
  grid-template-rows: 150px 150px;
  grid-gap: 1rem;
}
```

### repeat() notation
A handy tip if you find yourself repeating length units, is to use the `repeat()` notation. The above code could be rewritten like so:

```
.container {
  display: grid;
  width: 800px;
  grid-template-columns: repeat(3, 1fr);
  grid-template-rows: repeat(2, 150px);
  grid-gap: 1rem;
}
```

This provides us with the following result:

[XXXXXX]

DevTools Homework: Try inspecting the above grid and changing the grid-template column to the following: `grid-template-columns: 10px, repeat(2, 1fr)`. What happened? As you can see, you can not only use the `repeat()` notation for just part of the track listing, but you can also mix units (in this case, `px` and `fr`).

We will learn more about mixing units in the next section.
