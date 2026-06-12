``` mermaid
sequenceDiagram
    participant Zen
    participant helsinki

    Zen-->>helsinki: GET https://studies.cs.helsinki.fi/exampleapp/spa
    activate helsinki
    helsinki-->>Zen: HTML document [Status:304]
    deactivate helsinki

    Zen-->>helsinki: GET https://studies.cs.helsinki.fi/exampleapp/main.css
    activate helsinki
    helsinki-->>Zen: Stylesheet [Status:304]
    deactivate helsinki

    Zen-->>helsinki: GET https://studies.cs.helsinki.fi/exampleapp/spa.js
    activate helsinki
    helsinki-->>Zen: Script [Status:304]
    deactivate helsinki

    Zen-->>helsinki: GET https://studies.cs.helsinki.fi/exampleapp/data.json
    activate helsinki
    helsinki-->>Zen: json file containing data -[{ date: "2026-06-11T22:21:24.246Z", content: "" },...] [Status:200]
    deactivate helsinki

    Zen-->>helsinki: GET https://studies.cs.helsinki.fi/exampleapp/new_note_spa
    activate helsinki
    helsinki-->>Zen: Json file-[message:"note created"] [Status:201]
    deactivate helsinki

```
