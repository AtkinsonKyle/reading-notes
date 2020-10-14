# Node, Express, and APIs

### An Introduction to Node.js

- Node.js is an event-based, non-blocking, asynchronous I/O runtime that uses Google’s V8 JavaScript engine and libuv library
- The V8 engine is the open-source JavaScript engine that runs in Google Chrome and other Chromium-based web browsers, including Brave, Opera, and Vivaldi. It was designed with performance in mind and is responsible for compiling JavaScript directly to native machine code that your computer can execute
- The creator of Node, Ryan Dahl, took the V8 engine and enhanced it with various features, such as a file system API, an HTTP library, and a number of operating system–related utility methods
- Node.js is a JavaScript runtime
- npm is a package manager that comes bundled with Node
- Node.js is single-threaded. It’s also event-driven, which means that everything that happens in Node is in reaction to an event

<img src="https://uploads.sitepoint.com/wp-content/uploads/2012/10/1516152673node_event_loop.png" alt="picture of node.js">

- Blocking I/O calls should be avoided, CPU-intensive operations should be handed off to a worker thread, and errors should always be handled correctly for fear of crashing the entire process
- Node is suited to building applications that require real-time interaction — chat sites, or CodeShare, where you can watch a document being edited live by someone else.
- A good fit for building APIs where you’re handling lots of requests that are I/O driven, or for sites involving data streaming, as Node makes it possible to process files while they’re still being uploaded
- Node speaks JSON!
