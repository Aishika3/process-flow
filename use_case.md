```mermaid
flowchart LR
  subgraph "Sahayak System"
    direction TB
    UC1((Register / Login))
    UC2((View Classes))
    UC3((Select Class))
    UC4((View Student Profiles & Marksheets))
    UC5((Upload Sample Marksheet))
    UC6((Manage Assignments & Tests))
    UC7((Access Assignments & Tests))
    UC8((Submit Assignments & Tests))
    UC9((Use AI Tools))
    UC10((Hyper-Local Content))
    UC11((Differentiated Worksheets))
    UC12((Instant Q&A))
    UC13((Visual Aids))
    UC14((Reading Assessment))
    UC15((Game Generation))
    UC16((Lesson Planner))
    UC17((Translation & Grammar))
  end

  Teacher[Teacher] --- UC1
  Teacher --- UC2
  Teacher --- UC3
  Teacher --- UC4
  Teacher --- UC5
  Teacher --- UC6
  Teacher --- UC9

  Student[Student] --- UC1
  Student --- UC7
  Student --- UC8
  Student --- UC9

  UC9 --- UC10
  UC9 --- UC11
  UC9 --- UC12
  UC9 --- UC13
  UC9 --- UC14
  UC9 --- UC15
  UC9 --- UC16
  UC9 --- UC17
