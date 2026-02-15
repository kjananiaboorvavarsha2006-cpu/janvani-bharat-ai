# JanVani Bharat — AI Government Scheme Navigator

## Problem Statement

Citizens often fail to access government welfare schemes because eligibility rules are complex, scattered across documents, and difficult to understand in local languages. Manual lookup is slow, confusing, and inaccessible to rural populations.

## Target Users

- Rural and semi-urban citizens
- Farmers and informal workers
- Students and job seekers
- Small business owners
- Local language speakers (Tamil/Hindi)
- Low-connectivity rural users (SMS-based access)

## Why AI Is Needed (Not Just Rule-Based Filters)

Government scheme documents are written in unstructured and complex language with varying eligibility conditions.

AI is required to:

- Understand natural language user queries
- Extract structured user attributes from voice/text
- Perform semantic matching with scheme descriptions
- Handle multilingual variations
- Rank and score scheme relevance

A rule-only filter cannot effectively interpret language variation, incomplete inputs, or complex eligibility descriptions.

## AI Approach

We use NLP-based AI models for:

- Entity extraction (age, income, occupation, location)
- Semantic similarity matching
- Personalized recommendation ranking
- Multilingual response generation

Additionally, we implement:

### Personalized Recommendation Scoring (AI Score Engine)

Each scheme is assigned a 0–100 eligibility confidence score based on:
- Income alignment
- Age criteria
- Occupation match
- Location eligibility
- Scheme-specific weightage

This enables transparent and explainable ranking.

## Rural Offline SMS Mode

To support low-connectivity areas:

- Users can send basic profile details via SMS
- Backend processes the request
- AI evaluates eligibility
- SMS reply returns top 2 matching schemes

This ensures digital inclusion beyond smartphones.

## Expected Output

User provides profile via chat/voice/SMS → system returns:

- Eligible schemes
- AI-based eligibility score
- Reason for eligibility
- Benefit summary
- Required documents
- Step-by-step application guidance

## Responsible & Secure Design

- No permanent storage of sensitive personal data
- Encrypted request handling
- Transparent eligibility explanation
- Human verification recommended before final submission

## Innovation & Hackathon Alignment

- AI-first citizen assistance model
- Multilingual accessibility
- Cloud-native scalable architecture
- Real-world public impact
- Inclusive rural access via SMS
- Explainable AI scoring mechanism
