## Flow: Sumitting a note in a Single Page Application 
<pre> ```mermaid

flowchart TD
    A[User types a note in input field] --> B[Clicks 'Save']

    B --> C[JavaScript captures input and builds note object]
    C --> D[JavaScript sends POST request to /new_note_spa]

    D --> E[Server receives request and saves note]
    E --> F[Server responds with 201 Created]

    F --> G[JavaScript logs or handles response]
    G --> H[UI updates dynamically]
    ``` </pre>