sequenceDiagram
participant User
participant Browser
participant Server

    User>Browser - Writes new note and press button Save
    Browser>Server - HTTP Post /new_note_spa [content]
    server activated
    Server>Browser - HTTP 201 (new note as JSON)
    server deactivated

    Note: Browser JS refresh user interface with new note and note list without refreshing whole page again
