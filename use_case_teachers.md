```mermaid
graph LR
  subgraph "Sahayak System – Teacher"
    direction LR
    UC1((Register / Login))
    UC2((View Classes))
    UC3((Select Class))
    UC4((View Student Profiles & Marksheets))
    UC5((Upload Sample Marksheet))
    UC6((Manage Assignments & Tests))
    UC9((Use AI Tools))
  end

  Teacher["Teacher"] --> UC1
  Teacher --> UC2
  Teacher --> UC3
  Teacher --> UC4
  Teacher --> UC5
  Teacher --> UC6
  Teacher --> UC9
