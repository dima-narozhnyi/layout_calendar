1. [BEM] - Check your BEM structure using BEM-linter (`npm run lint`) and
[this list](https://mate-academy.github.io/fe-program/css/typical-bem-mistakes)
2. [BEM] - Make sure to follow BEM naming convention for complex modifiers:
`block-name--modifier-name--modifier-value`;
3. [SASS] - Make use of SASS nesting - write pseudo-class, pseudo-element
selectors inside general selector. As well as media queries.

GOOD example:
```scss
&__buy-link {
  display: flex;
  margin-top: 20px;

  &:hover {
    color: blue;
  }
}
```

BAD example:
```scss
&__buy-link {
  display: flex;
  margin-top: 20px;
}

&__buy-link:hover {
  color: blue;
}
```

4. [SASS] - Check your import syntax. It's differs from plain CSS.
5. [SASS] - use variables for the main values so that you'll be able to reuse
them and give them descriptive names. But don't overuse them, don't create
variable for the value that's used just once.
6. [SASS] - Don't use SASS loops for styles that stay the same for all elements
of the group, e.g. `display` or `position`.
7. [STYLES] - Make sure to list all styles that you apply transition to. If
there are more than 3 - use `all`.
8. [STYLES] - Make sure to add transition style under general selector, not the
one with `:hover` - this way transition will work smoothly both ways.

GOOD example:
```scss
.box {
  color: gray;
  transition: color 0.5s;

  &:hover {
    color: aquamarine;
  }
}
```

BAD example:
```scss
.box {
  color: gray;

  &:hover {
    color: aquamarine;
    transition: 0.5s;
  }
}
```

9. [FUNCTIONALITY] - Your project should work correctly (have 31 days and start
on Monday) with invalid modifier values, like `start-day--ghy` or `days--27`.
10. [STYLES] - Don't be greedy, add some top paddings, so the top row don't go over
top of the page on hover.
