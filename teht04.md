sequenceDiagram
participant Browser
participant Server
participant User

    User>Browser: Enters note text and then press Save
    Browser>Server: HTTP Post /new_note content
    Server: Server receives request and data from content

    Server>Browser: 302 New note
    Broser>User: Refresh user interface(now having new note visible)
