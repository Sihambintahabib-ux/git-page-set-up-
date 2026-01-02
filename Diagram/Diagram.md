## Diagram-

![](https://youtu.be/RuvtgvJ2UXU?si=u50VOnD6t6H3CK2n)
![](./001DIAGRAM.drawio.svg)

<!-- ![](./Untitled-2025-12-26-1431.excalidraw) -->
<!-- ![](./DIAGRAM.dio) -->
<!-- ![](./DIAGRAM.drawio) -->
<!-- ![](./DIAGRAM.drawio.png) -->
<!-- ![](./Diagram.md) -->

---

mermaid : https://mermaid.js.org/syntax/flowchart.html 2. https://www.mermaidflow.app/editor

```mermaid
graph TD;
    A[Start] --> B{Decision};
    B --> C{Option 1};
    B --> D{Option 2};
    C --> E[End];
    D --> E;

```

```markdown
![Alt text for the diagram](./NextJS.drawio.svg)
```

```mermaid
graph LR
    %% Define the Server Node as a cylinder
    Server[("server")]

    %% Define the Client side within a Subgraph
    subgraph Browse
        Client["client site"]
    end

    %% Define the relationships
    %% Arrow from Client to Server labeled 'Request'
    Client -- "Request" --> Server

    %% Arrow from Server to Client labeled 'Response'
    Server -- "Response" --> Client
```
