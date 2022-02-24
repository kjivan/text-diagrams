---
marp: true
---
<!-- class: invert -->
# Text Diagrams
Kavi Jivan

---
# General Tips

- Give up some layout control
    - Use minimal controls like directions/line lengths to layout
    - Trust the tool to group
    - Not going to be perfect
    - Revisit layout near the end
- Use a live preview while creating the diagram
- Browse the diagrams and see what fits best first
- Try to find the right level of detail on the diagram

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
# Plant UML Example
```
@startuml
Alice -> Bob: Authentication Request
Bob --> Alice: Authentication Response

Alice -> Bob: Another authentication Request
Alice <-- Bob: Another authentication Response
@enduml
```

---
# Plant UML Tips
```
@startuml
left to right direction
!theme plain
skinparam componentStyle rectangle
title Some Diagram

    'A
    [A]-->[B]
    [A]-->[C]

    'B
    [B]-->[D]

    'C
    [C]-->[D]

@enduml
```

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
# Mermaid Example
```
graph TD;
    A-->B;
    A-->C;
    B-->D;
    C-->D;
```