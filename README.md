# Project Name: BhashaLens
AI-Powered Public Policy Intelligence & Action Platform

---

## 1. Problem Statement

Government schemes, public notices, circulars, taxation rules, and legal documents are often written in complex bureaucratic language and are difficult for citizens to interpret.

While access to information exists, comprehension and actionable clarity remain significant barriers. Many citizens—especially in rural and semi-urban areas—struggle to:

- Interpret eligibility conditions
- Understand legal and taxation implications
- Identify required documents
- Determine compliance obligations
- Take correct next steps
- Raise structured complaints regarding policy issues

This creates a systemic gap between public systems and communities.

There is a need for an AI-powered platform that transforms static public documents into structured, interactive, and actionable intelligence.

---

## 2. Objective

To build an AI-powered Public Policy Intelligence System that:

- Converts complex government documents into simplified, structured summaries.
- Extracts actionable components (eligibility, benefits, documents, deadlines).
- Enables contextual policy-based conversational interaction.
- Provides a complaint & accountability mechanism.
- Assists users in understanding legal and taxation rules during asset purchases.
- Supports local-language and voice-based accessibility.
- Operates efficiently in low-bandwidth environments.

---

## 3. Target Users

- Rural citizens
- Senior citizens
- Farmers
- Students applying for scholarships
- Small business owners
- Property or vehicle buyers
- Community workers (NGOs, Panchayat officials)
- First-time taxpayers

---

## 4. Functional Requirements

---

### FR1: Document Input Module

- Upload PDF (scanned or digital)
- Upload image of notice
- Paste raw text manually
- Support multilingual documents

---

### FR2: OCR & Text Extraction

- Extract text from scanned PDFs or images
- Clean formatting noise
- Normalize and preprocess text
- Handle multi-page documents

---

### FR3: AI-Based Semantic Parsing

System must:

- Identify scheme name
- Extract eligibility criteria
- Detect benefits
- Identify required documents
- Extract deadlines
- Parse compliance conditions
- Extract application process

Output must be structured in JSON format.

---

### FR4: Plain Language Simplification Engine

- Rewrite content in simple Hindi / English
- Reduce bureaucratic complexity
- Convert long paragraphs into:
  - Bullet points
  - Step-by-step instructions
- Highlight critical information

---

### FR5: Action Intelligence Engine

System must generate:

- Step-by-step application roadmap
- Eligibility verdict (Likely Eligible / Needs Clarification)
- Required document checklist
- Missing information alerts
- Deadline reminders

---

### FR6: Policy Conversational Interface

Users must be able to:

- Ask contextual questions related to uploaded document
- Clarify eligibility doubts
- Ask about taxation or compliance clauses
- Receive answers grounded in extracted document data

System must:
- Use document-aware contextual prompts
- Minimize hallucination risk
- Maintain session context

---

### FR7: Complaint & Bounty System

System must allow:

- Structured complaint submission
- AI-assisted complaint drafting
- Categorization (Eligibility Issue / Implementation Delay / Policy Gap)
- Unique complaint ID generation
- Complaint tracking dashboard
- Optional reward points model for verified complaints

---

### FR8: Asset Purchase Legal & Taxation Helper

System must assist users purchasing assets such as:

- Cars
- Residential plots
- Agricultural land
- Commercial property

Features:

- Identify applicable government taxes (GST, Registration, Stamp Duty)
- Provide state-specific rules
- Estimate approximate charges
- Generate legal compliance checklist
- Identify required documentation
- Highlight regulatory risks

---

### FR9: Voice Interface

- Speech-to-text for user queries
- Text-to-speech for AI responses
- Support regional language output

---

### FR10: Low-Bandwidth Mode

- Text-only minimal interface
- Compressed API responses
- Lightweight UI rendering
- Optimized server calls

---

## 5. Non-Functional Requirements

### Performance
- Response time < 10 seconds per document
- Chat response time < 5 seconds

### Scalability
- Modular architecture
- API-based microservice compatibility
- Horizontal scaling capability

### Security
- Secure file upload handling
- Data encryption in transit
- JWT-based authentication (if user accounts enabled)
- Minimal data retention policy

### Reliability
- Graceful failure handling
- Input validation
- OCR fallback mechanisms

### Accessibility
- Mobile-first design
- Multilingual support
- Voice accessibility

---

## 6. Expected Output Format

### Structured Output Example:

{
  "scheme_name": "",
  "eligible_if": [],
  "benefits": [],
  "documents_required": [],
  "deadline": "",
  "steps_to_apply": [],
  "compliance_notes": [],
  "risk_flags": []
}

---

## 7. Success Metrics

- Reduction in comprehension complexity score
- Increased action clarity score
- Multi-language adoption rate
- Complaint resolution tracking efficiency
- Legal awareness improvement in asset purchases
- User satisfaction rating

---

## 8. Unique Value Proposition

BhashaLens transforms public policy documents into:

Access → Understanding → Interaction → Action → Accountability

It is not a static information portal, but a structured AI-powered Public Policy Intelligence Platform designed for real-world Bharat use cases.
