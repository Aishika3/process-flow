```mermaid
flowchart LR
  G((Proceed to AI Tools)) --> H{Choose Tool}

  subgraph "AI Tools"
    H --> H1([Hyper-Local Content])
    H --> H2([Differentiated Worksheets])
    H --> H3([Instant Q&A])
    H --> H4([Visual Aids])
    H --> H5([Reading Assessment])
    H --> H6([Game Generation])
    H --> H7([Lesson Planner])
    H --> H8([Translation & Grammar])
  end

  H1 --> I1([Invoke Vertex AI Gemini Text])
  H2 --> I2([OCR → Gemini → PDF])
  H3 --> I3([Gemini QA])
  H4 --> I4([Gemini Multimodal → SVG])
  H5 --> I5([Speech-to-Text / TTS])
  H6 --> I6([Gemini → Cloud Run Game])
  H7 --> I7([Gemini → Firestore → FCM / Email])
  H8 --> I8([Gemini/Gemma Translation])

  I1 & I2 & I3 & I4 & I5 & I6 & I7 & I8 --> J([Return Results → UI])
  J --> Z((End))
