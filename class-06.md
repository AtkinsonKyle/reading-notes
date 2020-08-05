# Daily Reading 6

## Javascript
<hr>

### Chapter 3 - Object Literals
#### Things To Know
- If a variable is a part of an object, it is called a property
  - Properties tell us about the object
- A function that is a part of an object is called a method
  - Methods represent tasks that are associated with the object
- Properties and methods have a name and value. In an object, that name is called a key
- Literal notation is one of the easiest ways to create objects
- You acces the properties or methods of an object using dot notation or square brackets
<br>
<hr>

### Chapter 5 - Document Object Model
#### Things To Know
- The browser represents the page using a DOM tree
- DOM trees have four nodes
  - Document Nodes
  - Element Nodes
  - Attribute Nodes
  - Text Nodes
- You can select element nodes by their id or class attributes, by tag names, or using CSS selector syntax
- Whenever a DOM query can return more than one node, it will always return a NodeList
- Browsers have tools that can show you the DOM tree
- In older browsers, showing the DOM is inconsistent
- Element nodes can contain multiple text nodes and child elements that are siblings of each other
- When you have a NodeList, you can loop through each node in the collection and apply the same statements to each
```
var hotItems = document.querySelectorAll('li.hot');
for (var i = 0; i < hotItems.length; i++) {
  hotItems[i].className = 'cool';
}
```
<br>
<hr>

### Problem Domain
#### Key Notes on Problem Domains
- Repetition is key!
- Problem domains are hard

[Link to Reading Notes](https://atkinsonkyle.github.io/reading-notes/)