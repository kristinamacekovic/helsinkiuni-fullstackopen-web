# Opening https://studies.cs.helsinki.fi/exampleapp/spa
Note: all routes are in relation to the base URL https://studies.cs.helsinki.fi/exampleapp

```mermaid
sequenceDiagram
  participant B as Browser
  participant S as Server
  Note left of B: Text entered into text box and button to submit pressed
  Note left of B: Submitted content added into the (browser-based) notes list
  Note left of B: Clear form text box content
  Note left of B: Trigger redrawing (browser-based) notes (i.e. page is finished rendering from the users perspective)
  Note left of B: Send the submitted data to the server
  B ->> S: POST /new_note_spa
  S ->> B: 201 Created, response contains the newly submitted content
```
