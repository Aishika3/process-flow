```mermaid
flowchart TD
  A((Start)) --> B{Select Role}
  B -->|Teacher| C([Teacher: Register/Login])
  B -->|Student| D([Student: Register/Login])

  C --> E([Load Teacher Dashboard])
  D --> F([Load Student Dashboard])

  subgraph "Teacher Actions"
    E --> E1([View Classes])
    E1 --> E2([Select Class])
    E2 --> E3([View Student Profiles & Marksheets])
    E2 --> E4([Upload Sample Marksheet])
    E2 --> E5([Manage Assignments/Tests])
    E2 --> E6([Enter AI Tools])
  end

  subgraph "Student Actions"
    F --> F1([View Assignments/Tests])
    F1 --> F2([Submit Assignment/Test])
    F2 --> F3([Upload to Storage])
    F2 --> F4([Notify Teacher])
    F1 --> F5([Enter AI Tools])
  end

  E6 & F5 --> G((Proceed to AI Tools))
