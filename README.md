Iontrace — Physics-Informed Object-Relational Schema

> Functional MVP Prototype: Built for rapid algorithm validation, multi-vendor binary file parsing (.mpr, .nda, .res), and electrochemical physics constraint enforcement.

---

Quick Test Instructions (10-Second Validation)

Reviewers can test the prototype in two ways:

Option A: One-Click Instant Run (Fastest)
1. Launch the [Live Streamlit Prototype](https://isaac96447-iontrace-mvp.streamlit.app).
2. Select " Instant Demo (Pre-loaded CALCE Run)" in the sidebar to execute the pipeline immediately.

Option B: Test Manual Drag-and-Drop
1. Download the raw sample dataset: [`calce_test_run.mpr`](./sample_data/calce_test_run.mpr) (~100 KB).
2. Open the [Live Streamlit Prototype](https://isaac96447-iontrace-mvp.streamlit.app).
3. Drag and drop the downloaded `.mpr` file into the "Hardware Ingest Data" box to observe sub-second multi-vendor parsing, step-indexing, and Butler-Volmer kinetic guardrail checks in real-time.

---

Architecture Overview
- Ingestion Layer: Edge daemon polling & zero-touch binary parsing (`.mpr`, `.nda`).
- Translation Engine: Multi-vendor schema normalization into unified physics tensors.
- Physics Guardrails: Deterministic thermodynamic/kinetic boundary checks preventing AI hallucinations.
