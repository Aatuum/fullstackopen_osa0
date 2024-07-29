sequenceDiagram
participant User
participant Browser
participant Server

    User>Browser: Open page https://studies.cs.helsinki.fi/exampleapp/spa
    Browser>Server - HTTP Get /spa
    server activated
    Server-Browse - Spa's HTML-file
    server deactivated

    Note: Browser JS runs and loads main.css
    Browser>Server - HTTP Get /main.css
    server activated
    Server>Browser - main.css file
    server deactivated

    Browser>Server - HTTP get /content.json
    server activated
    Server>Browser - All notes as JSON
    server deactivated

    Browsers JS handles and shows all notes in the user interface
