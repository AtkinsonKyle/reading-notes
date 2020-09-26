# Daily Reading 9
## HTML
<hr>

### Chapter 7 - Forms
#### Things to Know
- Forms live inside of a `<form>` element and are used for collecting information from visitors
- Information from forms are sent in name/value pairs
- Form controls are given a name and the text the user types in or the values of the options they select are sent to the server
- HTML5 makes it easier for visitors to fill in forms
#### Elements to Know
- `<form>` Carries the action attribute and will usually have a method and id attribute
- `<input>` Creates different form controls
  - `type = text` Creates a single line text input
  - `type = radio` Allows users to pick just one of a number of options
  - `type = checkbox` Allows users to select and deselect one or more options as an answer to a question
  - `type = password` Creates a text box that acts like a single-line text input, except characters are blocked out
  - `type = file` Creates a box with "Browse" next to it
  - `type = submit` Used to send a form to the server
  - `type = image` Use an image for the "submit" button
  - `type = hidden` Form controls that don't show on the page
  - `type = date` Date value
- `<textarea>` Creates a multi-line text input. Not an empty element. Appears in text box.
- `<select>` A drop down list box
- `<option>` Used to specify the options that the user can select from
- `<label>` Makes the form accesible to vision-impaired users
  - Wrap around text description and form input
  - Kept separate from form control and use the for attribute to indicate which form control it is a label for
- `<fieldset>` Helpful for longer forms. Groups related form controls together
- `<legend>` Contains a caption which helps identify the purpose of a specific group of form controls

### Chapter 14 - Lists, Tables, and Forms
#### Things to Know
- List markers can have different appearances using `list-style-type` and `list-style` image properties
- Table cells can have different borders
#### CSS Properties and Attributes
`empty-cells` Specifies whether or not empty cell's border should be shown
- Styling Submit Buttons
  - `color`
  - `text-shadow`
  - `border-bottom`
  - `background-color`
  - `:hover`

<hr>

## Javascript
### Chapter 6 - Events
#### Things To Know
- Events indicate when something has happened
- Binding states which event you are waiting to happen, and which element you are waiting for that event to happen upon
- You can use event delegation to monitor for events that happen on all of the children of an element
- When an event occurs on an element, it can trigger a Javascript function