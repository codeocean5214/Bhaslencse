# BhashaLens - System Design Document

## 1. System Overview

BhashaLens is an AI-powered document interpretation system that transforms complex public documents into simplified, actionable intelligence for citizens.

It operates in four layers:
1. Document Processing Layer
2. AI Semantic Engine
3. Simplification & Action Layer
4. Voice & Accessibility Layer

---

## 2. High-Level Architecture

User → Frontend → Backend API → AI Processing Pipeline → Structured Output → UI Display

---

## 3. Detailed Architecture Components

### 3.1 Frontend Layer
- Web-based responsive UI
- Document upload module
- Voice input interface
- Display simplified summary and action steps

---

### 3.2 Backend Layer (FastAPI / Django)

Handles:
- File upload
- Text extraction
- API orchestration
- JSON structuring
- Voice response generation

---

### 3.3 Document Processing Layer

Pipeline:
- PDF/Image Upload
- OCR (Tesseract or AWS Textract)
- Text Cleaning
- Chunking for LLM processing

---

### 3.4 AI Semantic Engine

Tasks:
- Named entity extraction
- Eligibility condition parsing
- Deadline detection
- Benefit identification
- Structured JSON generation

Prompt-driven structured extraction.

---

### 3.5 Simplification Engine

- Rewrite in simple language
- Convert paragraphs into:
  - Bullet points
  - Step-by-step instructions
- Translate into local language

---

### 3.6 Action Engine

Generates:
- Checklist of documents
- Eligibility summary
- Application steps
- Deadline alerts

---

### 3.7 Voice Layer

- Speech-to-Text (user query)
- Text-to-Speech (AI response)

---

## 4. Process Flow Diagram (Text Format)

START
  ↓
User Uploads Document
  ↓
OCR / Text Extraction
  ↓
Text Cleaning & Preprocessing
  ↓
LLM Semantic Parsing
  ↓
Structured JSON Output
  ↓
Simplification Engine
  ↓
Action Plan Generator
  ↓
Language Translation
  ↓
Display on UI / Voice Output
  ↓
END

---

## 5. Use Case Diagram (Textual)

Actor: Citizen

Use Cases:
- Upload government document
- Ask voice query
- View simplified summary
- Check eligibility
- View required documents
- Get step-by-step action guide

---

## 6. Architecture Diagram (Text Representation)

[User Device]
      ↓
[Frontend UI]
      ↓
[Backend API Server]
      ↓
------------------------------------
| OCR Engine                      |
| AI Semantic Parser              |
| Simplification Module           |
| Action Generator                |
| Translation Module              |
------------------------------------
      ↓
[Structured JSON + Voice Output]

---

## 7. Technologies Used

Frontend:
- React / HTML + Tailwind

Backend:
- FastAPI / Django
- Python

AI:
- LLM API (OpenAI / AWS Bedrock)
- Prompt Engineering

OCR:
- Tesseract OCR / AWS Textract

Voice:
- Web Speech API
- AWS Polly (optional)

Database:
- PostgreSQL / MongoDB

Hosting:
- AWS EC2 / Render / Vercel

---

## 8. Estimated Implementation Cost (Hackathon Prototype)

- Cloud hosting: Minimal (Free Tier)
- LLM API calls: Controlled usage
- Total estimated cost: <$20 for prototype

---

## 9. USP of BhashaLens

- Converts documents into structured action intelligence
- Focuses on comprehension, not just access
- Supports local language and voice
- Low-bandwidth optimized
- AI-driven semantic extraction, not keyword search

