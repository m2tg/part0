Sequence Diagram for adding note in SPA app

```mermaid
sequenceDiagram
    participant browser
    participant server

    Note to right of browser: form.onsubmit event handler is activated on clicking submit button <br>
    Extracts content from the form input

    Note to right of browser: Append newly created note to notes list and invoke redrawNotes funtion to render the newly created note 

    browser->>server: POST https://studies.cs.helsinki.fi/exampleapp/new_note_spa Payload: {"content":"test","date":"2024-01-20T09:02:37.999Z"}
    activate server
    server-->>browser: HTTP status code: 201 (No redirect)
    deactivate server

    
```