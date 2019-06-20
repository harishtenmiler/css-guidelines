# CSS Guidelines 
### General
- Avoid using HTML tags in CSS selectors
- Don't use ids in selectors
- Don’t nest more than 3 levels deep
- Avoid using nesting for anything other than pseudo selectors and state selectors.
- Don't use `!important` - If you must, leave a comment, and prioritise resolving specificity issues before resorting to `!important`.
- Use shorthand properties
- Avoid user agent detection as well as CSS “hacks”—try a different approach first.

### Spacing
- Put spaces after `:` in property declarations
  - E.g. `color: red;` instead of `color:red;`
- Put spaces before `{` in rule declarations
  - E.g. `.o-modal {` instead of `.o-modal{`
- Write your CSS one line per property
- Add a line break after `}` closing rule declarations
- When grouping selectors, keep individual selectors on a single line
- Place closing braces `}` on a new line
- Add a new line at the end of .scss files
- Trim excess whitespace

### Rule ordering
Properties and nested declarations should appear in the following order
1. Layout and box-model properties
   - margin, padding, box-sizing, overflow, position, display, width/height, etc.
2. Typographic properties
   - E.g. font-*, line-height, letter-spacing, text-*, etc.
3. Stylistic properties
   - color, background-*, animation, border, etc.
4. UI properties
   - appearance, cursor, user-select, pointer-events, etc.
5. Pseudo-elements
    - ::after, ::before, ::selection, etc.
6. Pseudo-selectors
   - :hover, :focus, :active, etc.
7. Modifier classes
8. Child elements if applicable

Here’s a comprehensive example:
```css
.c-btn {
  display: inline-block;
  padding: 6px 12px;
  text-align: center;
  font-weight: 600;
  background-color: red;
  border-radius: 3px;
  color: white;
}
.c-btn::before {
  content: '';
}
.c-btn:focus, .c-btn:hover {
  box-shadow: 0 0 0 1px color(blue, 0.3);
}
.c-btn--big {
  padding: 12px 24px;
}
.c-btn > .c-icon {
  margin-right: 6px;
}
```
