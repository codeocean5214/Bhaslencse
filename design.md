# BhashaLens - System Design Document

---

# 1. System Overview

BhashaLens is an AI-powered Public Policy Interpretation and Action Platform that transforms complex government documents into simplified, structured, and actionable intelligence.

Unlike traditional information portals, BhashaLens enables:

- Document interpretation
- Policy-based conversational interaction
- Complaint filing & tracking
- Asset purchase legal & taxation assistance
- Voice & local-language accessibility

The system operates across six core layers:

1. Document Processing Layer
2. AI Semantic Intelligence Layer
3. Simplification & Action Layer
4. Policy Conversational Layer
5. Complaint & Governance Layer
6. Voice & Accessibility Layer

---

# 2. High-Level Architecture

User
  ↓
Frontend Application
  ↓
Backend API Gateway
  ↓
-------------------------------------------------
| Document Processing Engine                   |
| AI Semantic Engine                           |
| Simplification & Action Engine               |
| Policy Chat Module                           |
| Complaint & Bounty Module                    |
| Asset Legal & Taxation Advisory Module       |
-------------------------------------------------
  ↓
Structured Output + Voice Response
  ↓
User Interface Display

---

# 3. Detailed Architecture Components

---

## 3.1 Frontend Layer

Technology: React / Next.js

Features:
- Document upload interface (PDF/Image/Text)
- Chat interface (policy discussion)
- Complaint submission portal
- Asset purchase helper form
- Voice input/output interface
- Low-bandwidth text-only mode
- Dashboard for complaint tracking

---

## 3.2 Backend Layer (FastAPI / Django)

Responsibilities:
- File handling
- OCR orchestration
- LLM API calls
- Structured JSON validation
- Complaint storage & tracking
- Taxation rule processing
- API routing & security

---

## 3.3 Document Processing Layer

Pipeline:

PDF/Image Upload
   ↓
OCR Engine (Tesseract / AWS Textract)
   ↓
Text Cleaning & Normalization
   ↓
Chunking for LLM Input
   ↓
Semantic Extraction Trigger

Handles:
- Scanned documents
- Noisy formatting
- Multilingual inputs

---

## 3.4 AI Semantic Intelligence Layer

Core Tasks:

- Named Entity Recognition (Scheme, Department, State)
- Eligibility Condition Extraction
- Deadline Detection
- Benefit Identification
- Document Requirement Parsing
- Compliance Condition Detection

Output Format:

{
  "scheme_name": "",
  "eligible_if": [],
  "benefits": [],
  "documents_required": [],
  "deadline": "",
  "application_steps": []
}

This structured output feeds downstream modules.

---

## 3.5 Simplification & Action Layer

Transforms extracted data into:

- Plain-language summaries
- Bullet-point explanations
- Step-by-step instructions
- Eligibility verdict (Likely Eligible / Needs Clarification)
- Required document checklist
- Deadline alerts

Includes:
- Readability reduction engine
- Translation module
- Action roadmap generator

---

## 3.6 Policy Conversational Layer

Enables contextual chat grounded in uploaded documents.

User can:
- Ask clarifications
- Query taxation clauses
- Understand compliance requirements
- Request examples

Architecture:

User Query
   ↓
Context Retrieval (From Parsed Document JSON)
   ↓
LLM Contextual Prompt
   ↓
Structured Response

Prevents hallucination by grounding answers in extracted data.

---

## 3.7 Complaint & Bounty Module

Purpose:
Improve transparency and accountability.

Features:

- AI-assisted complaint drafting
- Categorization (Eligibility Issue / Policy Gap / Implementation Delay)
- Unique complaint ID generation
- Status tracking dashboard
- Community validation scoring
- Optional reward points model for verified issues

Architecture:

User Complaint
   ↓
Structured Form
   ↓
AI Enhancement & Formatting
   ↓
Database Storage
   ↓
Tracking & Notification System

---

## 3.8 Asset Legal & Taxation Advisory Module

Supports asset purchases such as:

- Cars
- Residential plots
- Agricultural land
- Commercial property

Functionality:

- Calculate applicable taxes (GST, Registration, Stamp Duty)
- Identify state-specific charges
- Provide legal documentation checklist
- Estimate compliance cost
- Highlight regulatory risks

Processing Flow:

User Asset Input
   ↓
State & Asset Rule Engine
   ↓
Tax & Legal Condition Retrieval
   ↓
Structured Advisory Output

---

## 3.9 Voice & Accessibility Layer

- Speech-to-Text (User Query)
- Text-to-Speech (Response)
- Multilingual Output
- Low-bandwidth optimization

Designed for:
- Rural users
- Senior citizens
- Limited digital literacy environments

---

# 4. End-to-End Process Flow Diagram

START
  ↓
User Uploads Document
  ↓
OCR & Text Extraction
  ↓
Text Cleaning & Chunking
  ↓
AI Semantic Parsing
  ↓
Structured JSON Generation
  ↓
Simplification Engine
  ↓
Action Plan Generation
  ↓
-----------------------------------
| Optional Extensions            |
| - Policy Chat                  |
| - Complaint Filing             |
| - Asset Legal Helper           |
-----------------------------------
  ↓
Language Translation
  ↓
Voice / UI Output
  ↓
END

---

# 5. Use Case Diagram (Textual Representation)

Primary Actor: Citizen

Use Cases:
- Upload Government Document
- View Simplified Summary
- Check Eligibility
- Ask Policy Questions
- File Complaint
- Track Complaint Status
- Use Asset Purchase Helper
- Listen via Voice Output

Secondary Actor: NGO Worker

Use Cases:
- Assist Community Members
- Batch Document Analysis
- Track Regional Complaints

---

# 6. Refined Architecture Diagram (Text Representation)

[User Device]
        ↓
[Frontend UI Layer]
        ↓
[API Gateway / Backend Server]
        ↓
--------------------------------------------------
| Document Processing Engine                    |
| AI Semantic Extraction Engine                 |
| Simplification & Action Generator             |
| Policy Chat Module                            |
| Complaint Management System                   |
| Asset Legal & Taxation Rule Engine            |
| Translation & Voice Module                    |
--------------------------------------------------
        ↓
[Database Layer]
(PostgreSQL / MongoDB)
        ↓
[Structured Output + Voice Response]

---

# 7. Technologies Used

Frontend:
- React / Next.js
- Tailwind CSS

Backend:
- FastAPI / Django
- Python

AI & NLP:
- LLM API (OpenAI / AWS Bedrock)
- Prompt Engineering
- Context-grounded generation

OCR:
- Tesseract OCR / AWS Textract

Voice:
- Web Speech API
- AWS Polly

Database:
- PostgreSQL (Structured)
- MongoDB (Document storage optional)

Hosting:
- AWS EC2 / Lambda
- Render / Vercel

Security:
- JWT Authentication
- Input validation
- Secure file handling

---

# 8. Estimated Implementation Cost (Prototype)

Cloud Hosting: Free Tier
LLM Usage: Controlled API calls
OCR: Open Source
Database: Free Tier

Estimated Total Cost: < $20 for hackathon prototype

---

# 9. Updated USP of BhashaLens

BhashaLens is not a chatbot.

It is a structured Public Policy Intelligence System that:

- Converts unstructured government documents into structured action intelligence
- Enables contextual policy-based conversation
- Introduces a complaint & accountability mechanism
- Provides legal & taxation clarity for asset purchases
- Supports voice and multilingual accessibility
- Optimized for low-bandwidth environments
- Uses AI-driven semantic extraction instead of keyword search

It bridges:

Access → Understanding → Action → Accountability

---

# 10. Scalability & Future Scope

- Integration with government APIs
- WhatsApp bot deployment
- State-wise legal database expansion
- District-level analytics dashboard
- Automated deadline reminders
- Community transparency reports
