# 0.4 New note diagram
```mermaid
sequenceDiagram
Note left of Browser: User fill in the form and click save button
Browser->> Server: HTTP POST request https://studies.cs.helsinki.fi/exampleapp/new_note
activate Server
Server-->> Browser: Status Code: 302
Note left of Browser: URL redirect
Browser->> Server: HTTP GET request /exampleapp/notes
Server-->> Browser: HTML document
Browser->> Server: HTTP GET request https://studies.cs.helsinki.fi/exampleapp/main.css
Server-->> Browser: CSS document
Browser->> Server: HTTP GET request https://studies.cs.helsinki.fi/exampleapp/main.js
Server-->> Browser: JavaScript document
Browser->> Server: HTTP GET request https://studies.cs.helsinki.fi/exampleapp/data.json
Server-->> Browser: data.json document

```
