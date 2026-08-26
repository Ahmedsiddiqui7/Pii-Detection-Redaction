# PII Detection & Redaction in Digitized Documents — Frontend

An automated system that detects and redacts personally identifiable information (PII) — names, ID numbers, and other sensitive fields — from digitized documents (PNG, JPEG, PDF).

Built by a 4-member team as our Final Year Design Project at NED University of Engineering & Technology. Presented live at NED's FYP Exhibition to visiting industry representatives.

## Problem

Digitized documents frequently carry exposed PII, creating risk across legal, financial, educational, and insurance workflows where documents get shared or archived. Manual redaction doesn't scale — this project automates detection and redaction while preserving document usability.

## System Architecture

```
Document Upload → OCR Engine → PII Classifier → Redaction Engine → Output Generator → User Interface
```

- **Input Handler** — accepts PNG, JPEG, PDF uploads
- **OCR Engine** — extracts raw text and positional (bounding-box) data
- **PII Classifier** — hybrid NER + regex model, detects 13 types of PII
- **Redaction Engine** — black-box, blur, or custom pattern masking
- **Output Generator** — redacted document + structured JSON audit report

## Key Features

| Feature | Description |
|---|---|
| Document Upload | Supports PNG, JPEG, PDF |
| OCR Integration | High-accuracy OCR via Amazon Textract |
| PII Classification | Detects 13 types of PII |
| Redaction Engine | Black-box, blur, and custom pattern redaction |
| JSON Output | OCR and PII data stored in structured format |
| Frontend Interface | Clean UI for upload, preview, and download |
| Audit Logging | Full activity logging (admin-only) |

## Technologies Used

| Component | Technology |
|---|---|
| OCR | Amazon Textract |
| PII Classifier | Custom ML model (NER + Regex) |
| Backend | Python (FastAPI) |
| Frontend | React.js (Next.js) |
| Storage | AWS S3, JSON format |
| Authentication | JWT Tokens |

## My Role

Primary hands-on ownership of the frontend/UI — site structure, login page, and dashboards, built with Next.js and Tailwind CSS. Beyond the frontend, I was involved across the project's full lifecycle (problem definition, system requirements, architecture discussions), and presented the complete system — OCR pipeline, PII classification, and redaction engine — at the FYP Exhibition demo.

## Future Work

- Real-time redaction
- Cloud deployment (AWS/GCP)
- Multilingual support (Arabic/Urdu)
- Blockchain-based immutable audit logging
