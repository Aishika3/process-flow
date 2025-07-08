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
    E2 --> E6([AI Tools])
  end

  subgraph "Student Actions"
    F --> F1([View Assignments/Tests])
    F1 --> F2([Submit Assignment/Test])
    F2 --> F3([Upload to Storage])
    F2 --> F4([Notify Teacher])
    F1 --> F5([AI Tools])
  end

  subgraph "AI Tools"
    E6 & F5 --> G{Choose Tool}
    G --> G1([Hyper-Local Content])
    G --> G2([Differentiated Worksheets])
    G --> G3([Instant Q&A])
    G --> G4([Visual Aids])
    G --> G5([Reading Assessment])
    G --> G6([Game Generation])
    G --> G7([Lesson Planner])
    G --> G8([Translation & Grammar])
  end

  G1 --> H1([Invoke Vertex AI Gemini Text])
  G2 --> H2([OCR → Gemini → PDF])
  G3 --> H3([Gemini QA])
  G4 --> H4([Gemini Multimodal → SVG])
  G5 --> H5([Speech-to-Text / TTS])
  G6 --> H6([Gemini → Cloud Run Game])
  G7 --> H7([Gemini → Firestore → FCM/Email])
  G8 --> H8([Gemini/Gemma Translation])

  H1 & H2 & H3 & H4 & H5 & H6 & H7 & H8 --> I([Return Results → UI])
  I --> Z((End))
