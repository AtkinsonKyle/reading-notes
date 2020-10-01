# jQuery, Events, and The DOM

## jQuery Notes

- jQuery is the JavaScript file that you include in your webpages. It finds elements using CSS selectors and then do something with the elements using jQuery methods.
- `$` accesses jQuery
- (selector) finds HTML elements
- action() is then performed on the element
- Basic syntax is: $("selector").action()

- `$("div.menu")` - all `<div>` elements with class="menu"

- `$("p:first")` - the first `<p>` element

- `$("h1, p")` - all `<h1>` and all `<p>` elements

- `$("div p")` - all `<p>` elements that are inside `<div>` elements

- `$("*")` - all elements of the DOM

- attr() method is used for getting the value of an attribute
- href, src, id, class, style are all examples of HTML attributes
- The attr() method also allows us to set a value for an attribute by specifying it as the second parameter.
- removeAttr() method is used for removing any attribute of an element
- html() method is used to get the content of the selected element, including the HTML markup
- If you need only the text content, without the HTML markup, you can use the  text() method. JUST TEXT, NO STYLE
- html() and text() methods can be used to change the content of HTML elements

* If the content you are setting contains HTML markup, you should use the html() method instead of text(). *

- the val() method allows us to get and set the values of form fields, such as textboxes, dropdowns, and similar inputs

- text() sets or returns the text content of selected elements.
- html() sets or returns the content of selected elements (including HTML markup).
- val() sets or returns the value of form fields.
- attr() sets or returns the value of attributes.
- removeAttr() removes the specified attribute

- append() inserts content at the end of the selected elements.
- prepend() inserts content at the beginning of the selected elements.
- after() inserts content after the selected elements.
- before() inserts content before the selected elements.
- append(), prepend(), before() and after() methods can also be used to add newly created elements
  `$("<div></div>")` creates a new div
- addClass( ) method adds one or more classes to the selected elements

* To specify multiple classes within the addClass() method, just separate them using spaces. For example, $("div").addClass("class1 class2 class3"). *

- removeClass() method removes one or more class names from the selected elements
- toggleClass() method toggles between adding/removing classes from the selected elements, meaning that if the specified class exists for the element, it is removed, and if it does not exist, it is added
- the css() method can be used to get and set CSS property values

```

  $(function() {
  alert($("p").css("background-color"));
  $("p").css("background-color", "blue");
});

```

- the css() method uses JSON syntax

```

  css({"property":"value","property":"value",...});

```

- width() and height() methods can be used to get and set the width and height of HTML elements
- The width() and height() methods get and set the dimensions without the padding, borders and margins.
- The innerWidth() and innerHeight() methods also include the padding.
- The outerWidth() and outerHeight() methods include the padding and borders

- parent() method returns the direct parent element of the selected element
- parent() method can only traverse a single level up the DOM tree.
To get all ancestors of the selected element you can use the parents() method
- eq() method can be used to select a specific element from multiple selected elements
- remove selected elements from the DOM using the remove() method
  You can also use the remove() method on multiple selected elements, for example $("p").remove() removes all paragraphs
- empty() method is used to remove the child elements of the selected element

### Common Events (Event Handlers)

- The following are the most commonly used events:
  - Mouse Events:
    - click occurs when an element is clicked.
    - dblclick occurs when an element is double-clicked.
    - mouseenter occurs when the mouse pointer is over (enters) the selected element.
    - mouseleave occurs when the mouse pointer leaves the selected element.
    - mouseover occurs when the mouse pointer is over the selected element.

  - Keyboard Events:
    - keydown occurs when a keyboard key is pressed down.
    - keyup occurs when a keyboard key is released.

  - Form Events:
    - submit occurs when a form is submitted.
    - change occurs when the value of an element has been changed.
    - focus occurs when an element gets focus.
    - blur occurs when an element loses focus.

  - Document Events:
    - ready occurs when the DOM has been loaded.
    - resize occurs when the browser window changes size.
    - scroll occurs when the user scrolls in the specified element.

- keydown event, occurs when a key on the keyboard is pressed
- on() method is used to attach an event to the selected element

* The on() method is useful for binding the same handler function to multiple events. You can provide multiple event names separated by spaces as the first argument. For example, you could use the same event handler for the click and dblclick events. *

* The argument of the off() method is the event name you want to remove the handler for. *

- You can remove event handlers using the off() method.
- pageX, pageY the mouse position (X & Y coordinates) at the time the event occurred, relative to the top left of the page.
- the type of the event (e.g. "click").
- which the button or key that was pressed.
- data any data that was passed in when the event was bound.
- target the DOM element that initiated the event.
- preventDefault() prevent the default action of the event (e.g., following a link).
- stopPropagation() Stop the event from bubbling up to other elements.
- trigger events programmatically using the trigger() method. For example, you can trigger a click event without the user actually clicking on an element
- speed of trigger() method is in milliseconds
- the fadeIn/fadeOut methods, which fade an element in and out of visibility.
- the fadeToggle() method fades in and out
- fadeTo(), which allows fading to a given opacity (value between 0 and 1)
- slideUp() and slideDown() methods are used to create a sliding effect on elements
- the slideToggle() method switches between the sliding effects and can take two optional parameters: speed and callback
- animate() method lets you animate to a set value, or to a value relative to the current value
  ("key":"value" pairs)
- To stop an animation before it is finished, jQuery provides the stop() method.

### Dropdown Menu

HTML

```

<div class="menu">
  <div id="item">Drop-Down</div>
  <div id="submenu">
    <a href="#">Link 1</a>
    <a href="#">Link 2</a>
    <a href="#">Link 3</a>
  </div>
</div>

```

JavaScript

```

$("#item").click(function() {
  $("#submenu").slideToggle(500);
});

```

## Pair Programming Notes

- Why Pair Programming?
  1. Greater efficiency
  2. Engaged collaboration
  3. Learning from fellow students/coworkers
  4. Building social skills
  5. Job interview readiness
  6. Work environment readiness
