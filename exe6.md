sequenceDiagram
Note right of user: The user writes inside the textbox

user->>browser: Press save button
activate browser

Note right of browser: Executes form.onsubmit (adds the note in the comment list)

browser-->>user: Update notes with DOM
browser->>server: POST https://studies.cs.helsinki.fi/exampleapp/new_note_spa
activate server
deactivate browser

Note right of server: Adds the comment in the database
deactivate server
