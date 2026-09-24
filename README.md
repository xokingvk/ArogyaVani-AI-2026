
# 🌿 ArogyaVani AI

## Multilingual Voice-First Healthcare & Government Scheme Assistant

ArogyaVani AI is a multilingual, voice-first healthcare assistance platform designed to make healthcare information, government welfare schemes, and local healthcare services more accessible to citizens.

The platform combines **voice interaction, multilingual AI, Retrieval-Augmented Generation (RAG), document-based eligibility assessment, and local healthcare access** into a single user-friendly application.

ArogyaVani AI is designed especially for users who may face language barriers, low digital literacy, complex government scheme procedures, or difficulty accessing reliable healthcare information.

> **Speak naturally. Understand clearly. Access healthcare confidently.**

---

## 📌 Table of Contents

- [About the Project](#-about-the-project)
- [Problem Statement](#-problem-statement)
- [Proposed Solution](#-proposed-solution)
- [Objectives](#-objectives)
- [Key Features](#-key-features)
- [Supported Languages](#-supported-languages)
- [System Architecture](#-system-architecture)
- [How the RAG System Works](#-how-the-rag-system-works)
- [Document Eligibility Pipeline](#-document-eligibility-pipeline)
- [User Workflows](#-user-workflows)
- [Technology Stack](#-technology-stack)
- [Trusted Knowledge Base](#-trusted-knowledge-base)
- [Project Structure](#-project-structure)
- [API Endpoints](#-api-endpoints)
- [Installation](#-installation)
- [Frontend Setup](#-frontend-setup)
- [Backend Setup](#-backend-setup)
- [Android Build](#-android-build)
- [Environment Variables](#-environment-variables)
- [Security and Privacy](#-security-and-privacy)
- [Healthcare Safety](#-healthcare-safety)
- [Project Goals](#-project-goals)
- [Future Improvements](#-future-improvements)
- [Project Status](#-project-status)
- [Disclaimer](#-disclaimer)
- [Contributing](#-contributing)
- [License](#-license)

---

## 🌱 About the Project

Accessing healthcare information and government welfare schemes can be difficult for many citizens.

Users may need to:

- Search through multiple government websites.
- Understand complicated eligibility conditions.
- Identify the correct healthcare scheme.
- Find the required documents.
- Understand healthcare information in a preferred local language.
- Locate nearby public healthcare facilities.
- Navigate complicated digital forms and interfaces.

ArogyaVani AI aims to simplify this process through a single conversational interface.

Users can interact with the application through:

- 🎤 Voice input
- 💬 Text input
- 📄 Document upload
- 🌐 Multilingual interaction
- 🏛️ Government scheme discovery
- 📍 Nearby healthcare facility discovery

The system combines AI-generated assistance with trusted document-based information to provide more useful and explainable responses.

---

## ❗ Problem Statement

Healthcare and government welfare information is often fragmented across different platforms.

Citizens may face the following challenges:

### 1. Language Barriers

Many healthcare and government resources are primarily available in English or use technical terminology.

Users may find it easier to communicate in their native or preferred language.

### 2. Low Digital Literacy

Text-heavy websites, complex forms, and multiple application steps can make government services difficult to access.

### 3. Government Scheme Discovery

Citizens may not know which government scheme is relevant to their situation.

For example:

- Maternal healthcare support
- Child healthcare schemes
- Public health insurance
- Nutrition-related schemes
- Government medical services

### 4. Eligibility Complexity

Government schemes may have different eligibility requirements involving:

- Age
- Location
- Income
- Pregnancy status
- Family details
- Required documents
- Social and economic criteria

### 5. Local Healthcare Access

Knowing that a healthcare facility exists is not always enough.

Users may also need:

- Facility location
- Nearby PHC information
- Public healthcare access points
- Directions to the facility

### 6. Information Reliability

AI-generated responses can be inaccurate if they are not grounded in trusted information.

ArogyaVani AI addresses this through a curated knowledge base and Retrieval-Augmented Generation.

---

## 💡 Proposed Solution

ArogyaVani AI brings multiple healthcare-access features into one voice-first platform.

The system allows users to:

1. Ask general healthcare questions.
2. Interact using supported Indian languages.
3. Discover relevant government health schemes.
4. Retrieve scheme information from trusted documents.
5. Upload documents for structured information extraction.
6. Evaluate potential scheme eligibility using defined rules.
7. View benefits and required documents.
8. Find nearby PHC and PDS facilities.
9. Access official sources and application information when available.

The platform is designed to assist users with understanding and accessing information.

It is not intended to replace qualified healthcare professionals or official government verification.

---

## 🎯 Objectives

The main objectives of ArogyaVani AI are:

- Make healthcare information more accessible.
- Support voice-based interaction.
- Reduce language-related barriers.
- Provide multilingual healthcare assistance.
- Ground government scheme answers in trusted documents.
- Simplify scheme discovery.
- Support document-based eligibility assessment.
- Avoid guessing missing user information.
- Provide explainable scheme responses.
- Connect users with nearby public healthcare facilities.
- Create a simple and accessible user experience.

---

## ✨ Key Features

### 🎤 1. Voice-First Healthcare Assistant

Users can ask questions through voice instead of typing.

The voice interaction flow includes:

1. User speaks into the microphone.
2. Speech is converted into text.
3. The system identifies the user's request.
4. The request is routed to the appropriate service.
5. An AI-generated or document-grounded response is created.
6. The response can be converted into speech.

Example queries:

```text
I have a headache.

What should I do for a cough?

I have fever.

Which government scheme supports pregnant women?

What documents are required for this scheme?
```

The assistant provides general healthcare information and safety-aware guidance.

It does not provide medical diagnosis or prescribe medication.

---

### 🌐 2. Multilingual Interaction

The application is designed to support interaction in multiple Indian languages.

Supported languages in the ArogyaVani prototype include:

- English
- Hindi
- Tamil
- Telugu
- Kannada
- Malayalam

The multilingual workflow is designed to support:

- Speech recognition
- Language processing
- Response generation
- Voice response

The available languages and quality of support may depend on the configured speech and language services.

---

### 🤖 3. General AI Healthcare Assistant

The general healthcare assistant handles common healthcare information queries.

Examples:

```text
I have a headache.

What are common symptoms of fever?

What should I know about malaria?

What are the warning signs that require medical attention?
```

The assistant is designed to:

- Provide general information.
- Use understandable language.
- Avoid unsupported diagnosis.
- Avoid prescribing medication.
- Encourage professional medical assistance when appropriate.
- Identify situations that may require urgent care.

General healthcare queries are handled separately from the government scheme RAG pipeline.

---

### 🏛️ 4. Government Scheme Assistant

Users can ask questions about government healthcare and welfare schemes.

Examples:

```text
Which scheme helps pregnant women?

What benefits does Janani Suraksha Yojana provide?

What documents are needed?

Am I eligible for this scheme?

How can I apply?
```

The scheme assistant uses a dedicated RAG pipeline that retrieves relevant information from curated documents.

The system can provide:

- Scheme name
- Scheme description
- Potential eligibility information
- Benefits
- Required documents
- Application information
- Official sources
- Access instructions when available

The system should not treat an AI-generated response as final government approval.

---

### 📚 5. Retrieval-Augmented Generation

ArogyaVani AI uses Retrieval-Augmented Generation to provide responses grounded in trusted scheme documents.

Instead of relying only on the language model's general knowledge, the system retrieves relevant information from an indexed document collection.

#### RAG Workflow

```text
User Question
      ↓
Question Embedding
      ↓
FAISS Similarity Search
      ↓
Relevant Document Chunks
      ↓
Gemini Grounded Generation
      ↓
Answer and Source Information
      ↓
Relevant Scheme Results
```

The RAG pipeline maintains metadata such as:

- Source document
- Page number
- Similarity score
- Retrieved document content

This helps the system provide more traceable and explainable responses.

---

### 📄 6. Document-Based Scheme Eligibility

Users can upload documents for structured information extraction.

Supported document formats in the prototype include:

- JPG
- PNG
- PDF

The document processing pipeline can identify explicitly available information such as:

- Name
- Age
- State
- Pregnancy status
- Income information
- BPL or ration card information
- Rural or urban information
- Child age

#### Document Eligibility Workflow

```text
Uploaded Document
      ↓
Document Validation
      ↓
Image or PDF Processing
      ↓
Gemini Document Understanding
      ↓
Structured User Profile
      ↓
Rule-Based Eligibility Engine
      ↓
Relevant Government Schemes
      ↓
Eligibility Explanation and Sources
```

The system should only extract information that is visibly available in the uploaded document.

Unknown information must not be guessed.

Missing information should be marked as:

```text
Not provided
```

or represented as a null value in structured data.

---

### ⚖️ 7. Rule-Based Eligibility Engine

The extracted user profile is evaluated against curated scheme criteria.

The eligibility engine is designed to use deterministic rules instead of relying entirely on free-form AI reasoning.

Potential evaluation fields include:

- Age
- State
- Pregnancy status
- Income
- BPL status
- Rural or urban location
- Child age
- Required documentation

The system can provide an explanation of why a scheme may be relevant based on the available information.

Final eligibility must be verified through the appropriate government authority or official scheme portal.

---

### 📋 8. Scheme Results

The application can display relevant scheme information, including:

- Scheme name
- Eligibility status
- Benefits
- Required documents
- Reason for potential eligibility
- How to apply
- How to access the service
- Trusted sources
- Official action links when available

Official URLs should be maintained as curated scheme metadata.

The AI model should not invent application URLs.

---

### 📍 9. Nearby PHC Discovery

The platform is designed to help users find nearby Primary Health Centres.

The location workflow may use:

- Device GPS
- A curated PHC dataset
- Distance calculation
- Facility details
- Google Maps directions

The application can identify nearby healthcare facilities based on the user's current location.

Precise location should be handled carefully and should not be unnecessarily stored in user history.

---

### 🏪 10. Nearby PDS Discovery

The application is also designed to support discovery of nearby Public Distribution System facilities, including Fair Price Shops.

The system can use:

- Device location
- Curated PDS facility datasets
- Distance calculation
- Facility information
- Navigation links

This feature is intended to connect information with local welfare access.

---

### 🔊 11. Voice Responses

The platform supports text-to-speech responses through the configured speech service.

The intended workflow is:

```text
Generated Text Response
      ↓
Language Processing
      ↓
Text-to-Speech Service
      ↓
Audio Response
      ↓
User
```

Voice responses are intended to make the application more accessible to users who prefer listening over reading.

---

### 🔐 12. Authentication and User Data

The planned application architecture includes Supabase-based authentication and persistence.

Potential user-specific data includes:

- User profile
- AI question count
- Scheme check records
- Health alerts
- Emergency contacts
- User preferences

The system should separate sensitive information from general application data and follow secure handling practices.

---

## 🌍 Supported Languages

The ArogyaVani prototype documents the following supported languages:

| Language | Supported |
|---|---|
| English | Yes |
| Hindi | Yes |
| Tamil | Yes |
| Telugu | Yes |
| Kannada | Yes |
| Malayalam | Yes |

Language support depends on the speech recognition, translation, and text-to-speech services configured in the deployment.

---

## 🧠 System Architecture

```text
                         USER
                           │
             ┌─────────────┼─────────────┐
             │             │             │
           VOICE         TEXT        DOCUMENT
             │             │             │
             └─────────────┼─────────────┘
                           ↓
                REACT / CAPACITOR APP
                           ↓
                     FASTAPI BACKEND
                           ↓
                   AI REQUEST ROUTER
                           │
             ┌─────────────┼─────────────┐
             │             │             │
             ↓             ↓             ↓
         GENERAL        SCHEME       DOCUMENT
           AI             RAG        ELIGIBILITY
             │             │             │
             ↓             ↓             ↓
          GEMINI         FAISS       GEMINI
                           │          + RULES
                     TRUSTED PDFs
                           │
                           ↓
                   GROUNDED RESPONSE
                           ↓
                       SARVAM AI
                           ↓
                     VOICE RESPONSE
                           ↓
                          USER
```

### Architecture Components

#### Frontend Layer

- React
- TypeScript
- Vite
- Tailwind CSS
- Voice assistant interface
- Scheme interface
- Eligibility interface
- Dashboard
- Multilingual UI

#### Backend Layer

- FastAPI
- Request routing
- Healthcare service
- Scheme RAG service
- Document processing service
- Eligibility service
- Location services

#### AI Layer

- Google Gemini
- Speech-to-text service
- Text-to-speech service
- Document understanding
- Grounded response generation

#### Knowledge Layer

- Trusted government scheme documents
- Sentence Transformer embeddings
- FAISS vector index
- Scheme metadata
- Source information

#### Persistence Layer

- Supabase Auth
- Supabase PostgreSQL
- User profiles
- User-specific records

---

## 🔎 How the RAG System Works

The RAG pipeline is divided into two primary stages:

1. Knowledge base creation
2. User question retrieval and response generation

### Stage 1: Knowledge Base Creation

```text
Trusted Government PDFs
          ↓
Page-by-Page Text Extraction
          ↓
Text Cleaning
          ↓
Text Chunking
          ↓
Multilingual Embeddings
          ↓
FAISS Vector Index
          ↓
Persistent RAG Artifacts
```

The documented prototype uses:

- 1,000-word chunks
- 150-word overlap
- Multilingual embeddings
- FAISS similarity search

### Stage 2: Query Processing

```text
User Question
      ↓
Question Embedding
      ↓
FAISS Similarity Search
      ↓
Top Relevant Document Chunks
      ↓
Gemini Contextual Prompt
      ↓
Grounded Answer
      ↓
Source and Scheme Information
```

The FAISS index is loaded by the RAG service and is not rebuilt for every user question.

### RAG Artifacts

```text
rag_artifacts/
├── scheme.index
└── chunks.json
```

---

## 📚 Trusted Knowledge Base

The documented ArogyaVani prototype uses the following trusted PDF sources:

1. Government Health Insurance Schemes India Research Paper
2. India Health Schemes Eligibility & Application Dataset
3. JSSK Scheme
4. JSY Scheme
5. NHM Scheme
6. PMMVY Scheme
7. PMSMA Scheme
8. RBSK Scheme

### Document Corpus

| Metric | Value |
|---|---|
| Trusted PDFs | 8 |
| Total pages | 74 |
| Approximate words | 19,567 |
| Indexed chunks | 74 |

The knowledge base is intended to be expanded as additional verified government documents are added.

---

## 🔄 User Workflows

### Workflow 1: General Healthcare Question

```text
User
  ↓
Voice or Text Input
  ↓
Speech-to-Text if Voice
  ↓
Intent Detection
  ↓
General Healthcare Service
  ↓
Gemini
  ↓
Healthcare Response
  ↓
Text-to-Speech if Required
  ↓
User
```

General healthcare questions do not use the government scheme RAG pipeline.

---

### Workflow 2: Government Scheme Question

```text
User
  ↓
Voice or Text Input
  ↓
Speech-to-Text if Voice
  ↓
Scheme Intent Detection
  ↓
Question Embedding
  ↓
FAISS Similarity Search
  ↓
Relevant Trusted PDF Sections
  ↓
Gemini Grounded Answer
  ↓
Relevant Scheme and Sources
  ↓
Text-to-Speech if Required
  ↓
User
```

---

### Workflow 3: Document Eligibility

```text
User
  ↓
Upload JPG, PNG, or PDF
  ↓
FastAPI Backend
  ↓
Document Validation
  ↓
Document Processing
  ↓
Gemini Document Understanding
  ↓
Structured User Profile
  ↓
Eligibility Rules
  ↓
Relevant Schemes
  ↓
Grounded Explanation
  ↓
Eligibility Results
```

---

### Workflow 4: Nearby Healthcare Facility

```text
User
  ↓
Location Permission
  ↓
Device GPS
  ↓
Facility Dataset
  ↓
Distance Calculation
  ↓
Nearby PHC or PDS Results
  ↓
Google Maps Directions
```

---

## 🛠️ Technology Stack

### Frontend

- React.js
- TypeScript
- Vite
- Tailwind CSS
- Framer Motion
- Lucide React
- i18next

### Mobile Application

- Capacitor
- Capacitor Android
- Android Build Tools

### Backend

- Python
- FastAPI
- Uvicorn
- Render

### Artificial Intelligence

- Google Gemini
- Gemini Flash-Lite for grounded generation
- Gemini document understanding

### Speech and Language

- Sarvam AI
- Speech-to-text
- Language processing
- Text-to-speech

### Retrieval-Augmented Generation

- Python RAG pipeline
- Sentence Transformers
- `paraphrase-multilingual-MiniLM-L12-v2`
- FAISS
- FAISS `IndexFlatIP`
- pypdf

### Document Processing

- pypdf
- Gemini document and vision understanding

### Eligibility

- Rule-based eligibility engine
- Curated government scheme criteria

### Database

- Supabase Auth
- Supabase PostgreSQL
- User profiles
- AI question count

### API and Voice

- REST API
- FastAPI
- FormData
- MediaRecorder API

### Development Tools

- Git
- GitHub
- Environment variables
- `.env`

---

## 📁 Project Structure

The following structure represents the documented application architecture.

```text
ArogyaVani AI
│
├── frontend
│   ├── src
│   │   ├── components
│   │   ├── features
│   │   │   ├── voice
│   │   │   └── schemes
│   │   ├── screens
│   │   ├── services
│   │   └── ...
│   ├── android
│   ├── package.json
│   └── capacitor.config.ts
│
└── backend
    ├── main.py
    ├── services
    │   ├── gemini_service.py
    │   ├── sarvam_service.py
    │   ├── rag_service.py
    │   ├── rag_ingestion.py
    │   ├── document_service.py
    │   └── eligibility_service.py
    ├── rag_artifacts
    │   ├── scheme.index
    │   └── chunks.json
    ├── requirements.txt
    └── ...
```

The exact structure may vary depending on the current implementation and deployment branch.

---

## 🌐 Backend API

### Health Check

```http
GET /health
```

Used to check whether the backend service is running.

---

### Voice Query

```http
POST /voice-query
```

Used for processing voice-based healthcare or scheme queries.

---

### Scheme Document

```http
POST /scheme-document
```

Used for scheme-related document processing.

> API paths and request formats should be verified against the backend implementation before production deployment.

---

## 🚀 Installation

### Prerequisites

Install the following tools:

- Node.js
- npm
- Python 3.10 or compatible version
- Git
- Android Studio, if building the Android application
- Required API credentials
- A configured Supabase project, if authentication is enabled

Clone the repository:

```bash
git clone https://github.com/xokingvk/ArogyaVani-AI-2026.git
```

Move into the project directory:

```bash
cd ArogyaVani-AI-2026
```

---

## 💻 Frontend Setup

Move into the frontend directory:

```bash
cd frontend
```

Install dependencies:

```bash
npm install
```

Start the development server:

```bash
npm run dev
```

Build the frontend for production:

```bash
npm run build
```

The production build is generated in the `dist` directory.

---

## 🐍 Backend Setup

Move into the backend directory:

```bash
cd backend
```

Create a virtual environment:

```bash
python -m venv venv
```

Activate the virtual environment.

### Windows

```bash
venv\Scripts\activate
```

### Linux or macOS

```bash
source venv/bin/activate
```

Install the dependencies:

```bash
pip install -r requirements.txt
```

Start the FastAPI server:

```bash
uvicorn main:app --reload
```

The backend will usually be available at:

```text
http://127.0.0.1:8000
```

---

## 📱 Android Build

ArogyaVani AI can be packaged as an Android application using Capacitor.

### Build Process

```text
React Application
       ↓
npm run build
       ↓
dist/
       ↓
Capacitor Sync
       ↓
Android Project
       ↓
Android Build
       ↓
APK
```

### Typical Commands

Build the frontend:

```bash
npm run build
```

Synchronize the Capacitor project:

```bash
npx cap sync android
```

Open the Android project:

```bash
npx cap open android
```

A debug APK is typically generated at:

```text
android/app/build/outputs/apk/debug/app-debug.apk
```

The exact Android build configuration depends on the local project setup.

---

## 🔑 Environment Variables

Store sensitive credentials in backend environment variables.

Example:

```env
GEMINI_API_KEY=your_gemini_api_key
SARVAM_API_KEY=your_sarvam_api_key
SUPABASE_URL=your_supabase_url
SUPABASE_ANON_KEY=your_supabase_anon_key
```

The frontend can use a backend URL such as:

```env
VITE_API_BASE_URL=http://127.0.0.1:8000
```

For production:

```env
VITE_API_BASE_URL=https://your-backend-domain.com
```

### Security Rules

- Never commit API keys to GitHub.
- Never place private API keys in frontend code.
- Use `.env` files locally.
- Add `.env` to `.gitignore`.
- Store production secrets in the hosting platform's environment settings.
- Keep third-party service credentials on the backend.

---

## 🚀 Production Deployment

### Backend

The FastAPI backend is designed to be deployed on Render.

The deployment should include:

- Python runtime
- Dependency installation
- Required environment variables
- Correct startup command
- CORS configuration
- API health check

Example startup command:

```bash
uvicorn main:app --host 0.0.0.0 --port $PORT
```

### Frontend

The frontend can be deployed using a static hosting provider.

Configure the backend URL using:

```env
VITE_API_BASE_URL
```

The frontend must communicate with the deployed backend through the configured API URL.

### Deployment Security

Do not place API secrets in frontend environment variables.

Only public configuration values should be exposed to the frontend.

---

## 🔐 Security and Privacy

ArogyaVani AI is designed with privacy and secure data handling in mind.

### API Key Protection

API keys should remain on the backend.

The frontend should not contain:

- Gemini private API keys
- Sarvam private API keys
- Database service-role keys
- Other secret credentials

### Document Privacy

Uploaded documents may contain sensitive personal information.

The application should:

- Validate uploaded files.
- Process only the required information.
- Avoid extracting unrelated information.
- Avoid guessing missing values.
- Limit unnecessary data storage.
- Apply appropriate access controls.
- Avoid exposing user documents to unauthorized users.

### Location Privacy

Precise GPS information should be used only when needed for nearby facility discovery.

The application should avoid storing precise location history unnecessarily.

---

## 🛡️ Healthcare Safety

ArogyaVani AI is an informational healthcare assistant.

The system should:

- Provide general healthcare information.
- Encourage professional medical care when appropriate.
- Avoid claiming to diagnose diseases.
- Avoid prescribing medication or dosage.
- Avoid presenting AI output as an official medical decision.
- Provide safety guidance for potentially urgent situations.
- Avoid inventing government scheme details.
- Ground scheme answers in trusted documents.
- Preserve source information.
- Avoid guessing missing document information.
- Avoid inventing official application URLs.

### Medical Disclaimer

The application does not replace:

- Doctors
- Nurses
- Hospitals
- Government healthcare professionals
- Emergency services
- Official government authorities

For emergencies, users should seek immediate professional or emergency medical assistance.

---

## 📊 AI Question Count

The documented architecture includes a per-user counter for successful general AI questions.

Example:

```text
AI QUESTIONS
12
```

The documented counting behavior is:

| Query Type | Counted |
|---|---|
| General Home AI questions | Yes |
| Scheme RAG questions | No |
| Document processing | No |

The counter is intended to track question usage and does not represent a complete conversation history.

---

## 🗂️ Scheme Catalog

The curated scheme catalog can contain the following fields:

- Scheme ID
- Scheme name
- Description
- Category
- Eligibility
- Benefits
- Required documents
- How to apply
- How to access
- Action type
- Official website
- Application URL
- Source information

The scheme catalog should remain separate from AI-generated responses.

This separation allows the application to maintain structured scheme metadata and reduce the possibility of invented official links.

---

## 🧪 Example Queries

### General Healthcare

```text
I have a headache.

What are the common symptoms of fever?

What should I know about malaria?
```

### Government Schemes

```text
Which government scheme supports pregnant women?

What are the benefits of Janani Suraksha Yojana?

What documents are required for this scheme?

How can I check whether I may be eligible?
```

### Document Eligibility

```text
Check the information available in my document.

Which details are missing from my profile?

Which schemes may be relevant based on my available information?
```

### Healthcare Access

```text
Find a nearby Primary Health Centre.

Where is the nearest public healthcare facility?

Find a nearby PDS centre.
```

---

## 🔄 Complete System Flow

```text
                         ┌─────────────────┐
                         │      USER       │
                         └────────┬────────┘
                                  │
                     Voice / Text / Document
                                  │
                                  ▼
                  ┌─────────────────────────┐
                  │ React + Capacitor App   │
                  └────────────┬────────────┘
                               │
                               ▼
                    ┌─────────────────────┐
                    │   FastAPI Backend   │
                    │       Render        │
                    └──────────┬──────────┘
                               │
                         Intent Router
                               │
             ┌─────────────────┼─────────────────┐
             │                 │                 │
             ▼                 ▼                 ▼
        General AI         Scheme RAG       Document
             │                 │             Eligibility
             ▼                 ▼                 ▼
          Gemini         SentenceTransformer   Gemini
                              │             Understanding
                              ▼                  │
                            FAISS                ▼
                              │             User Profile
                       Trusted PDFs             │
                              │                  ▼
                              │            Eligibility Rules
                              │                  │
                              └────────┬─────────┘
                                       │
                                       ▼
                               Grounded Response
                                       │
                                       ▼
                                  Voice Output
                                       │
                                       ▼
                                      USER
```

---

## 🎯 Project Goal

ArogyaVani AI aims to reduce the difficulty of accessing healthcare information and government welfare services.

The intended user experience is:

```text
Speak
  ↓
Understand
  ↓
Find Trusted Information
  ↓
Discover Relevant Schemes
  ↓
Understand Potential Eligibility
  ↓
Take the Next Action
```

The project combines:

- Voice accessibility
- Local-language interaction
- AI assistance
- Grounded government scheme retrieval
- Document-based information extraction
- Rule-based eligibility assessment
- Local healthcare facility discovery

---

## 🌟 Expected Impact

### Improved Accessibility

Voice interaction can reduce the difficulty of typing and navigating complex interfaces.

### Better Scheme Awareness

Users can ask conversational questions about government schemes and their benefits.

### More Understandable Information

The assistant can present information in a conversational and accessible format.

### Grounded Responses

RAG can help generate scheme-related answers using trusted documents.

### Simplified Eligibility Understanding

Document extraction and rule-based evaluation can help users understand which details are available and which information may be missing.

### Local Healthcare Access

Nearby PHC and PDS discovery can help connect digital information with physical services.

---

## 🚧 Future Improvements

Potential future improvements include:

- Real-time streaming voice interaction
- Faster voice response latency
- More government scheme documents
- More regional languages
- Additional document formats
- Conversation history
- Scheme analytics
- Document processing history
- Advanced healthcare navigation
- More external healthcare integrations
- Offline resilience
- Improved facility datasets
- Better official service integration
- State-specific scheme support

---

## 📌 Project Status

ArogyaVani AI is a prototype healthcare-access platform concept incorporating the following components:

- React web interface
- Responsive mobile UI
- Capacitor Android support
- Multilingual voice assistant architecture
- FastAPI backend
- Gemini integration
- Speech-to-text integration
- Text-to-speech integration
- Government scheme interface
- FAISS-based RAG pipeline
- Trusted PDF knowledge base
- Scheme source metadata
- Document eligibility pipeline
- Rule-based eligibility engine
- Supabase authentication architecture
- Per-user AI question counter
- Android APK prototype support

Some features may require additional configuration, integration, testing, or deployment work depending on the current branch.

---

## 🤝 Contributing

Contributions are welcome.

To contribute:

1. Fork the repository.
2. Create a new branch.

   ```bash
   git checkout -b feature/your-feature
   ```

3. Make your changes.
4. Test the changes locally.
5. Commit your changes.

   ```bash
   git commit -m "Add your feature"
   ```

6. Push the branch.

   ```bash
   git push origin feature/your-feature
   ```

7. Create a pull request.

### Contribution Areas

- Frontend improvements
- Accessibility
- Multilingual support
- RAG improvements
- Document processing
- Scheme metadata validation
- Security
- Testing
- Healthcare UX
- Performance optimization

---

## ⚠️ Disclaimer

ArogyaVani AI is a prototype intended for educational, research, and innovation purposes.

The application does not replace qualified healthcare professionals, official government authorities, or emergency medical services.

AI-generated information may contain errors. Users should verify healthcare advice, scheme eligibility, required documents, and application details through official sources and qualified professionals.

Final eligibility decisions are made by the relevant government authority, not by the AI system.

---

## 📄 License

Add an appropriate license before publishing the project.

For example:

```text
MIT License
```

The selected license should reflect the permissions and restrictions intended by the project contributors.

---

## ❤️ ArogyaVani AI

### Voice-first. Local-language. Trusted healthcare information.

> A citizen should not need to understand the healthcare system before they can access it.

**ArogyaVani AI — Speak naturally. Understand clearly. Access care confidently.**