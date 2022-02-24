---
marp: true
---
<!-- class: invert -->
# Text Diagrams
Kavi Jivan

---
# General Tips
- Give up some layout control
    - Not going to be perfect
    - Trust the tool to group
    - Revisit layout near the end
    - Use minimal controls like directions/line lengths to layout
- Use a live preview while working on diagrams
- Browse the types of diagrams and see what fits best first
- Try to keep your diagrams minimal

---
# Plant UML
Home - https://plantuml.com/
## Run
- [Online](http://www.plantuml.com/plantuml/uml)
- [VS Code Extension](https://marketplace.visualstudio.com/items?itemName=jebbs.plantuml)
- [Jar](https://github.com/plantuml/plantuml/releases/latest)
    - Install [Graphviz](https://www.graphviz.org/)
        - `brew install graphviz`
    - Create Diagrams
        - `java -jar plantuml*.jar diagram.txt`

---
# Plant UML Tips
- Need `@startuml` and `@enduml` before vscode preview works
- Remember to set direction
    - `left to right direction`
- Use plain theme for black and white
    - `!theme plain`
- Skin components to simple rectangles
    - `skinparam componentStyle rectangle`
- Give your diagram a title
    - `title Awesome Diagram`
- Group statements in diagram
    - Comments - `'Employees`
- Use arrows in one direction

---
# Mermaid
Home - https://mermaid-js.github.io/mermaid/#/

## Run
- [Online](https://mermaid.live/)
- [Github Markdown](https://github.blog/2022-02-14-include-diagrams-markdown-files-mermaid/)
- [VS Code Extension](https://marketplace.visualstudio.com/items?itemName=bierner.markdown-mermaid)
- [Command Line](https://github.com/mermaid-js/mermaid-cli)
    - Install
        - `brew install mermaid-cli`
        - `npm install @mermaid-js/mermaid-cli`
    - Run
        - `mmdc -i input.mmd -o output.svg`

---
# Mermaid Tips
- Use `flowchart` instead of `graph`
    - Subgraphs direction doesn't work with flowcharts
- Group statements in diagram
    - Comments - `%% Employees`
- Select desired theme
    - `%%{init: {'theme':'base'}}%%`
