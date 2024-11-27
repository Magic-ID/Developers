# Hello World
![Hello](./helloWorld.png "Hello World")

This little example app gets a message and last-seen time from the
Web Dæmon it is loaded into.

## Usage
1. Install the app in your Dæmon launcher.
2. When loaded, it echoes your Dæmon name and a "last seen" time.

This shows:

1. How to define a Dæmon app including icon.
2. How the web page frontend and Dæmon backend work together.
3. How to use simple Dæmon storage and lifecycle.

## How It Works
The [helloWorld.html](./helloWorld.html) file defines _both_ the front-end and back-end
for the app. Normally of course, an HTML file defines a front-end alone.

To do this, the HTML markup has just one extra thing:
```html
<link rel='webdaemon' href='helloWorld.yml'>
```
This element is used by the Dæmon just once - when the app is installed. It locates the YAML
file that defines the back-end.

## Files
The source files in this example are fully annotated, read them carefully to see how it fits
together:

- [`helloWorld.html`](./helloWorld.html)
  - This is the app source file, everything hangs off it.
- [`helloWorld.css`](./helloWorld.css)
  - Simple stylesheet for the frontend.
- [`helloWorld.yml`](./helloWorld.yml)
  - YAML file ties the frontend to the backend including authorization and static configuration.
- [`helloWorld.js`](./helloWorld.js)
  - Browser-side Javascript makes the request on the backend and displays the result.
- [`helloWorld.ts`](./helloWorld.ts)
  - Dæmon-side Typescript handles the request and serves the response.
