# PII Detection & Redaction in Digitized Documents — Frontend

Frontend for a Final Year Project that automatically detects and redacts personally identifiable information (PII) — names, ID numbers, and other sensitive fields — from digitized documents.

Built by a 4-member team as part of our BSCS FYP at NED University of Engineering & Technology. Presented at NED's FYP Exhibition to visiting industry representatives.

## What the full system does

Document → OCR text extraction → PII classification (NER + rule-based hybrid) → bounding-box coordinate extraction → redaction (black-box / blur / pattern masking) → redacted document + audit-log JSON report.

## My role

Primary hands-on ownership of the frontend/UI — site structure, login page, and dashboards, built with Next.js and Tailwind CSS. Beyond the frontend, I was involved across the project's full lifecycle (problem definition, system requirements, architecture discussions), and presented the complete system — OCR pipeline, PII classification, and redaction engine — at the FYP Exhibition demo.

## Tech stack

Next.js · TypeScript · Tailwind CSS · shadcn/ui


## Future work (identified in the project report)

- Real-time redaction
- Cloud deployment (AWS/GCP)
- Multilingual support (Arabic/Urdu)
- Blockchain-based immutable audit logging
