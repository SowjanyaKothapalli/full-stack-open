## Flow: Opening a Single Page Application 
<pre> ```mermaid
flowchart TD
    A[User opens /exampleapp/spa] --> B[Browser requests HTML page]
    B --> C[Server responds with HTML]

    C --> D[Browser requests main.css]
    C --> E[Browser requests spa.js]

    D --> F[Server responds - 200 OK or 304 Not Modified]
    E --> G[Server responds with spa.js file]

    G --> H[JavaScript - spa.js runs in browser]
    H --> I[JS sends GET request to /exampleapp/data.json]

    I --> J[Server responds with JSON data]
    J --> K[JS parses JSON and builds DOM nodes]
    K --> L[Notes are rendered into the page dynamically]
    ``` </pre>