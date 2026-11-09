# PII Detection and Redaction in Digitized Documents (Frontend)

An automated system that detects and redacts personally identifiable information (PII), such as names, ID numbers and other sensitive fields, from digitized documents (PNG, JPEG, PDF). This repository contains the frontend of the system.

Built by a team of four as our Final Year Design Project at NED University of Engineering and Technology. Presented live at NED's FYP Exhibition to visiting industry representatives.

## Problem

Digitized documents frequently carry exposed PII, creating risk across legal, financial, educational and insurance workflows where documents get shared or archived. Manual redaction does not scale, so this project automates detection and redaction while preserving document usability.

## System Architecture

Document Upload → OCR Engine → PII Classifier → Redaction Engine → Output Generator → User Interface

- Input Handler: accepts PNG, JPEG and PDF uploads
- OCR Engine: extracts raw text and positional (bounding-box) data
- PII Classifier: hybrid NER and regex model, detects 13 types of PII
- Redaction Engine: black-box, blur or custom pattern masking
- Output Generator: redacted document and structured JSON audit report

## Key Features

| Feature | Description |
|---|---|
| Document Upload | Supports PNG, JPEG, PDF |
| OCR Integration | High-accuracy OCR via Amazon Textract |
| PII Classification | Detects 13 types of PII |
| Redaction Engine | Black-box, blur and custom pattern redaction |
| JSON Output | OCR and PII data stored in structured format |
| Frontend Interface | Clean UI for upload, preview and download |
| Audit Logging | Full activity logging (admin-only) |

## Technologies Used

| Component | Technology |
|---|---|
| OCR | Amazon Textract |
| PII Classifier | Custom ML model (fine-tuned GLiNER for NER, plus Regex) |
| Backend | Python |
| Frontend (this repository) | React.js (Next.js), Tailwind CSS |
| Storage | AWS S3, JSON format |
| Authentication | JWT Tokens |

## Running the Frontend

```bash
npm install
npm run dev
```

Then open http://localhost:3000.

## Future Work

- Real-time redaction
- Cloud deployment (AWS/GCP)
- Multilingual support (Arabic/Urdu)
- Blockchain-based immutable audit logging
