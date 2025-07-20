## Flow: Submitting a New Note 

<pre> ```mermaid
flowchart TD
    A[User types note text in input field] --> B[User clicks 'Save' button]

    B --> C[Browser JS prevents default form submission]
    C --> D[Browser creates POST request to /exampleapp/new_note with note data]

    D --> E[Server receives POST request]
    E --> F[Server stores the new note]

    F --> G[Server responds with 302 Redirect to /exampleapp/notes]
    G --> H[Browser follows redirect and makes GET /exampleapp/notes]

    H --> I[Server returns updated HTML page]
    I --> J[Browser reloads and renders the updated list of notes]
    ``` </pre>

    
