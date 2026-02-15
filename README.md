# Project Name: BhashaLens
AI-Powered Government & Legal Document Simplifier & Action Engine

## 1. Problem Statement

Government schemes, public notices, circulars, and legal documents are often written in complex bureaucratic language and are difficult for citizens to understand. 

Access to information does not guarantee comprehension. Many citizens—especially in rural and semi-urban areas—struggle to:
- Interpret eligibility conditions
- Understand benefits
- Identify required documents
- Determine actionable next steps

This creates a barrier between public systems and communities.

---

## 2. Objective

To build an AI-powered system that:
- Converts complex government documents into simplified, actionable summaries.
- Extracts structured information (eligibility, benefits, documents required, deadlines).
- Supports local-language and voice-based interaction.
- Works in low-bandwidth environments.

---

## 3. Target Users

- Rural citizens
- Senior citizens
- Farmers
- Students applying for scholarships
- Small business owners
- Community workers (NGOs, Panchayat officials)

---

## 4. Functional Requirements

### FR1: Document Input
- Upload PDF (scanned or digital)
- Upload image of notice
- Paste text manually

### FR2: OCR & Text Extraction
- Extract text from scanned PDFs or images
- Clean and preprocess text

### FR3: AI-Based Semantic Parsing
- Identify:
  - Scheme name
  - Eligibility criteria
  - Benefits
  - Required documents
  - Deadlines
  - Application process
- Convert output into structured JSON format

### FR4: Plain Language Simplification
- Rewrite content in simple Hindi/English
- Reduce legal complexity
- Present in bullet points

### FR5: Action Engine
- Generate step-by-step application guide
- Highlight required documents
- Identify missing information

### FR6: Voice Interface
- Speech-to-text for queries
- Text-to-speech for responses

### FR7: Low-Bandwidth Mode
- Text-only minimal UI
- Optimized API calls
- Compressed responses

---

## 5. Non-Functional Requirements

- Response time < 10 seconds per document
- Mobile-friendly UI
- Scalable backend architecture
- Secure document handling
- Minimal data retention

---

## 6. Expected Output Format

Structured Output Example:

{
  "scheme_name": "",
  "eligible_if": [],
  "benefits": [],
  "documents_required": [],
  "deadline": "",
  "steps_to_apply": []
}

---

## 7. Success Metrics

- Reduction in comprehension difficulty
- Clear actionability score
- Multi-language accessibility
- User satisfaction feedback
