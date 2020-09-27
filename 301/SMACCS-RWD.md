# SMACSS and Responsive Web Design

### Shay Howe's Intro to RWD

- Responsive web design is the practice of building a website suitable to work on every device and every screen size, no matter how large or small, mobile or desktop.
- Responsive and adaptive web design are closely related, and often transposed as one in the same. Responsive generally means to react quickly and positively to any change, while adaptive means to be easily modified for a new purpose or situation, such as change.
- Responsive web design is broken down into three main components, including flexible layouts, media queries, and flexible media.
- Media queries were built as an extension to media types commonly found when targeting and including styles.
- Default for media type is "screen".
- The mobile first approach includes using styles targeted at smaller viewports as the default styles for a website, then use media queries to add styles as the viewport grows.
- Apple invented the viewport meta tag.

<hr>

### All About Floats

- Float is a CSS positioning property.
- Floated elements remain a part of the flow of the web page.
- Absolutely positioned page elements are removed from the flow of the webpage, like when the text box in the print layout was told to ignore the page wrap. Absolutely positioned page elements will not affect the position of other elements and other elements will not affect them, whether they touch each other or not.
- Left, right, none, and inherit are the four values of float.
- Float’s sister property is "clear". An element that has the clear property set on it will not move up adjacent to the float like the float desires, but will move itself down past the float.
- Clear has five valid values: none, left, right, inherit, and both.
- Collapsing almost always needs to be dealt with to prevent strange layout and cross-browser problems. We fix it by clearing the float after the floated elements in the container but before the close of the container.
- The Empty Div Method is, quite literally, an empty div.

  ```

  <div style="clear: both;"></div>

  ```

- The Overflow Method relies on setting the overflow CSS property on a parent element. If this property is set to auto or hidden on the parent element, the parent will expand to contain the floats, effectively clearing it for succeeding elements.
- The Easy Clearing Method uses a clever CSS pseudo selector (:after) to clear floats. Rather than setting the overflow on the parent, you apply an additional class like “clearfix” to it. Then apply this CSS:

```

.clearfix:after {
   content: ".";
   visibility: hidden;
   display: block;
   height: 0;
   clear: both;
}

```

- Pushdown is a symptom of an element inside a floated item being wider than the float itself (typically an image). Use overflow: hidden to cut off excess.
- Double Margin Bug – Another thing to remember when dealing with IE 6 is that if you apply a margin in the same direction as the float, it will double the margin. Set display: inline on the float.
- The 3px Jog is when text that is up next to a floated element is mysteriously kicked away by 3px like a weird forcefield around the float. Set a width or height on the affected text.
- the Bottom Margin Bug is when if a floated parent has floated children inside it, bottom margin on those children is ignored by the parent. Use bottom padding on the parent instead.

<hr>

### Scalable and Modular Architecture for CSS (SMACCS)

- SMACSS is a way to examine your design process and as a way to fit those rigid frameworks into a flexible thought process.
- 5 Categories of SMACCS:
  - Base Rules - the defaults(html, body, form)
  - Layout Rules - divide the page into sections(hold one or more modules together)
  - Modules Rules - the callouts, the sidebar sections, the product lists and so on(the reusable, modular parts of a design)
  - State Rules - describes how modules or layouts will look when in a particular state
  - Theme Rules - similar to state rules in that they describe how modules or layouts might look
