sequenceDiagram
    participant browser as Browser
    participant server as Server

    Note over Browser: User writes something in the text field
    Note over Browser: User clicks the "Save" button

    Browser->>Server: POST https://studies.cs.helsinki.fi/exampleapp/new_note
    activate Server
    Note over Server: Server processes the request and saves the note
    Server-->>Browser: Response with success status
    deactivate Server

    Note over Browser: Browser updates the UI with the new note