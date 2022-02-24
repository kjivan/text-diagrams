# Test Mermaid Diagram
# Basic Diagram
```mermaid
graph TD;
    A-->B;
    A-->C;
    B-->D;
    C-->D;
```

# Basic Diagram Forest Themed
[List of Themes](https://github.com/mermaid-js/mermaid/tree/master/src/themes)
```mermaid
%%{init: {'theme':'forest'}}%%
graph TD;
    A-->B;
    A-->C;
    B-->D;
    C-->D;
```

# Broken Graph
```mermaid
graph TD;
    A-->B;
    A-->C;
    B-->D;
    C-->D;
    subgraph B1
        direction RL
        i1 -->f1
    end
```

# Working flow chart
```mermaid
flowchart TD;
    A-->B;
    A-->C;
    B-->D;
    C-->D;
    subgraph B1
        direction RL
        i1 -->f1
    end
```

# More complex subgraph
```mermaid
flowchart LR
  subgraph TOP
    direction TB
    subgraph B1
        direction RL
        i1 -->f1
    end
    subgraph B2
        direction BT
        i2 -->f2
    end
  end
  A --> TOP --> B
  B1 --> B2
```

# Node Links
```mermaid
flowchart TD;
    A-- This is the text! ---->B
    A--->|This is the text|C;
    B-.->D;
    click B "http://www.github.com" "This is a tooltip for a link"
    C===>D;
```
# Node Shapes
```mermaid
flowchart TD;
    A(A);
    B[(B)];
    C{C};
    D[/D/];
    A-->B;
    A-->C;
    B-->D;
    C-->D;
```
# Links!
```mermaid
flowchart TD;
    A-->B;
    A-->C;
    B-->D;
    click B "http://www.github.com" "This is a tooltip for a link"
    C-->D;
```

# Sequence Diagram
```mermaid
sequenceDiagram
    participant Alice
    participant Bob
    Alice->>John: Hello John, how are you?
    loop Healthcheck
        John->>John: Fight against hypochondria
    end
    Note right of John: Rational thoughts <br/>prevail!
    John-->>Alice: Great!
    John->>Bob: How about you?
    Bob-->>John: Jolly good!
```

# Gantt 
```mermaid
gantt
dateFormat  YYYY-MM-DD
title Adding GANTT diagram to mermaid
excludes weekdays 2014-01-10

section A section
Completed task            :done,    des1, 2014-01-06,2014-01-08
Active task               :active,  des2, 2014-01-09, 3d
Future task               :         des3, after des2, 5d
Future task2               :         des4, after des3, 5d
```

# Class Diagram
```mermaid
classDiagram
Class01 <|-- AveryLongClass : Cool
Class03 *-- Class04
Class05 o-- Class06
Class07 .. Class08
Class09 --> C2 : Where am i?
Class09 --* C3
Class09 --|> Class07
Class07 : equals()
Class07 : Object[] elementData
Class01 : size()
Class01 : int chimp
Class01 : int gorilla
Class08 <--> C2: Cool label
```

# Git Graph - Experimental
```mermaid
gitGraph:
options
{
    "nodeSpacing": 150,
    "nodeRadius": 10
}
end
commit
branch newbranch
checkout newbranch
commit
commit
checkout master
commit
commit
merge newbranch
```

# Entity Relationship Diagram - Experimental
```mermaid
erDiagram
    CUSTOMER ||--o{ ORDER : places
    ORDER ||--|{ LINE-ITEM : contains
    CUSTOMER }|..|{ DELIVERY-ADDRESS : uses
```

# User Journey Diagram
```mermaid
journey
    title My working day
    section Go to work
      Make tea: 5: Me
      Go upstairs: 3: Me
      Do work: 1: Me, Cat
    section Go home
      Go downstairs: 5: Me
      Sit down: 5: Me
```