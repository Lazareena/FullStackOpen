sequenceDiagram
    participant browser
    participant server

    browser->>server: POST https://studies.cs.helsinki.fi/exampleapp/new_note_spa
    activate server
    browser->>server: Note JSON data.
    deactivate server

    New note added by server: The server creates a new note object using the javascript code. The note object is retrieved from the JSON payload. The server does not requests for a redirect. So the browser stays on the same page and sends no further HTTP requests.