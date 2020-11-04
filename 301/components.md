# Components

### EJS Partials

- Partials are like functions, they make large websites easier to maintain as you don’t have to go and change a piece of text in every page it appears in

- In EJS, any JavaScript or non-HTML syntax you include in your templates is always surrounded by `<% %>` delimiters

- To include a partial in EJS is easy. You use <%- include( PARTIAL_FILE ) %> where the partial file is relative to the template you use it in

- 