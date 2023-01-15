# Assignment 1

When a user enters an URL in the browser, how does the browser fetch the desiredresult ? Explain this with the below in mind and Demonstrate this by drawing a diagramfor the same

- What is the main functionality of the browser?
- High Level Components of a browser.
- Rendering engine and its use.
- Parsers (HTML, CSS, etc)
- Script Processors
- Tree construction
- Order of script processing
- Layout and Painting

---

# What is the main functionality of the browser?

[main-functionality](./images/main-functionality.png)

- User loads browser
- Type in browser https://pesto.com
- Browser sends request to DNS Server
- DNS finds IP address (i.e. 192.168.100.100) of pesto.com server from its db
- Request sent to Pesto Server
- Response sent ( HTML document ) to browser

# High Level Components of a browser

[browser-component](./images/browser-component.png)

1. UI - User interface:

   Address bar,

   Back, Forward, Refresh buttons,

   Bookmar Menu etc.
2. The browser engine:

   A link between the user interface and the rendering engine.
3. Rendering engine:

   The Rendering Engine renders the requested web page on the browser screen.
   Rendering engine converts HTML document and data to an visual format ( Text , image, or video ).

   Rendering engines used by browsers

   - Blink – Google Chrome, Opera, Microsoft Edge (previously used EdgeHTML).
   - WebKit – Safari.
   - Gecko – Mozilla Firefox.
   - Trident – Internet Explorer.
   - Presto – Legacy rendering engine for Opera.

   Note :  Browsers such as Chrome run multiple instances of the rendering engine: one for each tab. Each tab runs in a separate process.
4. Networking:

   The Networking component handles internet communication and security.
   It retrieves the URLs using common internet protocols.

   Common Internet protocols include TCP/IP (Transmission Control Protocol/Internet Protocol),
   UDP/IP (User Datagram Protocol/Internet Protocol),
   HTTP (HyperText Transfer Protocol) and FTP (File Transfer Protocol).
5. UI backend:

   UI Backend helps to draw basic widgets like a select box, an input box, a window, a check box, etc.
   It uses the device's operating system user interface methods for the same.
6. JavaScript interpreter.

   Used to parse (Interprets) and executes the JavaScript code embedded in a website.
   The results then are sent to the rendering engine for display.
7. Data storage.

   Used to save data locally ( into browser ) including Cookies, Local Storage, Session Storage, IndexedDB, WebSQL, and FileSystem.


# Parsers (HTML, CSS, etc)

[parser](./images/parser.png)

    - Building the DOM tree
    - Building the CSSOM tree
    - Combining the trees into the render tree
    - Preload Scanner
    - JavaScript Compilation
    - Building the Accessibility Tree

# Script Processors

    Front end script processor
    - HTML Parser -> DOM
    - Js engine -> DOM
    - CSS Parser -> CSSOM

# Tree construction

[tree-construction](./images/tree-construction.png)

Tree construction is essentially creating a tree-based of the parsed tokens and what we will be focusing on—The DOM tree.


