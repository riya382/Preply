# Preply - AI-Powered Interview Coach & Performance Diagnostics Platform

Preply is an enterprise-grade technical and behavioral mock interview preparation application designed to help candidates clear rigorous hiring loops. By contextually blending real-world job requirements with candidate profiles, the platform provides tailored mock evaluation queues, real-time analytics, and automatic standard ATS metric reporting.

---

## 🚀 Key Core Architectural Features

* **Context-Aware Question Generation:** Leverages advanced LLM token orchestration through the `gemini-2.5-flash` model to analyze candidate resumes side-by-side with target job descriptions.
* **Multi-Modal Document Parsing:** Intercepts raw binary PDF streams via `multer` middlewares and parses text inputs dynamically using the `pdf-parse` engine.
* **Strict Structural Constraints (Zod Validation):** Enforces rigorous JSON layout payloads utilizing Zod schemas (`zod-to-json-schema`), avoiding downstream unstructured formatting breaks.
* **100% Free Voice Automation (Native Web Speech API):** Implements text-to-speech loops built entirely into standard client-side browser interfaces, eliminating the need for premium, rate-limited cloud voice pipelines.
* **Granular Scorecard Dashboard:** Delivers instant evaluation responses after every submitted answer, wrapping up into a complete dynamic post-interview report outlining candidate attempts, ideal answer benchmarks, and key growth gaps.

---

## 🔥 Key Product Features Included

* **Interactive Coding & Behavioral Panel:** Live timer systems supporting preset intervals ($1\text{m}, 2\text{m}, 3\text{m}, 5\text{m}$) along with custom manual overwriting fields.
* **ATS Compatibility Analytics:** Real-time semantic checking models returning dynamic Match Scores ($0-100\%$) indicating real corporate filtering bypass probabilities.
* **Dynamic Step-by-Step Hints:** Smart hint blocks highlighting key system design patterns or conceptual domains if a candidate gets stuck.
* **End-to-End Performance History:** Complete post-session diagnostic screens displaying overall scorecards, user responses compared side-by-side with ideal answers, and granular structural replacement advice.

---

## 📂 System Directory Tree Structure

```text
Preply/
├── Backend/
│   ├── src/
│   │   ├── controllers/    # Request handlers (interview.controller.js)
│   │   ├── middlewares/    # Authentication & Multi-part upload rules
│   │   ├── models/         # MongoDB Mongoose collection models
│   │   ├── routes/         # Express endpoint definitions
│   │   └── services/       # Core Gemini AI integration (ai.service.js)
│   └── server.js
└── Frontend/
    ├── src/
    │   ├── features/       # Feature-driven layouts (Auth, Interview)
    │   │   └── interview/pages/MockInterview.jsx
    │   ├── App.jsx
    │   └── main.jsx
