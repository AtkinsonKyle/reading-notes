# Daily Reading 7
<hr>

## Javascript

### Chapter 6 - Functions, Objects, and Methods
#### Things To Know
- The new keyword and the object constructor create a blank object. You can then add properties and methods to the object.
  - Create a new object using a combination of the new keyword and the Object() constructor function. ("Object()" used to create functions)
  - Utilizing the blank object, you can add properties and methods to it using dot notation. Each statement that adds a property or method should end with ";"

```
var hotel = new Object();
hotel.name = 'Quay';
hotel.rooms = 40;           <---- properties
hotel.booked = 25;
------------------------------------------------------------
hotel.checkAvailability = function() {
  return this.rooms - this.booked;        <------- methods
};

```

- To update value of properties, use dot notation. They work on objects created using literal or constructor notation. To delete a property, use the delete keyword.
- `This` keyword! Commonly used inside fuctions and objects. Where the function is declared alters what `this` means. It always refers to one object, usually the object in which the function operates
- Arrays are a special type of object. They hold a related set key/value pairs, but the key for each value is its index number
- Arrays and objects are combineable and can create complex data structures: arrays can store a series of objects. Objects can also hold arrays
- The `Math` object has properties and methods for mathematical constants and functions
<hr>

## HTML

### Chapter 3 - Tables
#### Useful Elements
- `<table>` Creates a table
- `<tr>` table row
- `<td>` table data
- `<th>` table heading
- `<thead>` headings of table
- `<tbody>` table body
- `<tfoot>` table footer

#### Things To Know
- The `<table>` element adds tables to a webpage
- Tables are drawn out row by row
- Longer tables can be split up using: `<thead>`, `<tbody>`, and `<tfoot>`