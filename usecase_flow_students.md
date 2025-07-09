```mermaid
graph LR
  subgraph "Sahayak System – Student"
    direction LR
    UC1((Register / Login))
    UC7((Access Assignments & Tests))
    UC8((Submit Assignments & Tests))
    UC9((Use AI Tools))
  end

  Student["Student"] --> UC1
  Student --> UC7
  Student --> UC8
  Student --> UC9
