# System Design — JanVani Bharat

## Overall Architecture

User (Web / Voice / SMS)
        →
Input Processing Layer
(Speech-to-Text / Text Normalization)
        →
NLP Attribute Extraction Engine
        →
AI Eligibility Matching Engine
        →
AI Score Engine (0–100 Recommendation Score)
        →
Scheme Knowledge Base (DynamoDB)
        →
Response Generator (Multilingual)
        →
User Output (Chat / Voice / SMS Reply)

--------------------------------------------------

## Workflow

1. User provides profile via:
   - Web chat (text)
   - Voice input
   - SMS (offline rural mode)

2. If voice:
   - AWS Transcribe converts speech to text

3. NLP Engine extracts:
   - Age
   - Income
   - Occupation
   - Location
   - Special categories (if any)

4. AI Eligibility Matcher:
   - Compares user attributes with structured scheme data
   - Performs semantic similarity matching

5. Personalized AI Score Engine:
   - Assigns 0–100 confidence score
   - Applies weighted scoring logic:
     - Income match
     - Age eligibility
     - Occupation alignment
     - Location applicability

6. Recommendation Ranking:
   - Top 3 schemes returned
   - Sorted by eligibility score

7. Multilingual Response:
   - AWS Translate generates local language output
   - Clear explanation of "Why Eligible"

8. SMS Mode:
   - For low-connectivity users
   - SMS sent → Lambda triggered → AI processed → SMS reply returned

--------------------------------------------------

## Core Components

Frontend:
- React Web Interface
- Mobile-responsive UI
- SMS Gateway integration

Backend:
- AWS Lambda (Serverless APIs)
- Node.js processing layer

AI Services:
- AWS Bedrock (LLM processing)
- AWS Transcribe (Speech-to-Text)
- AWS Translate (Multilingual output)

Database:
- Amazon DynamoDB (Scheme rules & metadata)
- Amazon S3 (Scheme documents storage)

--------------------------------------------------

## AI Model Type

- Natural Language Processing (NLP)
- Semantic Matching
- Explainable Recommendation Ranking
- Multilingual Generation

--------------------------------------------------

## External Integrations

- Government scheme datasets
- SMS Gateway provider
- Cloud-based NLP services

--------------------------------------------------

## Security & Privacy

- No permanent Aadhaar storage
- Encrypted API communication
- Temporary session-based processing
- Access-controlled AWS resources

--------------------------------------------------

## Why This Is AI-Driven

- Interprets unstructured user queries
- Performs semantic reasoning over scheme documents
- Generates explainable eligibility decisions
- Provides intelligent ranking using AI score engine

This is not a static rule-based filter — it is a contextual AI reasoning system.
