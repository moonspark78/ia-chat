# Mistral Chat – AI Conversational Assistant

An AI-powered conversational application inspired by ChatGPT, built with **Next.js, Python, FastAPI and Mistral AI**.

The goal of this project is to develop a complete AI assistant capable of handling multi-turn conversations, maintaining conversation history, streaming LLM responses and answering questions about uploaded documents using Retrieval-Augmented Generation (RAG).

## Project Overview

Mistral Chat is a full-stack AI application designed to explore and implement modern Generative AI technologies.

Users will be able to:
- Interact with an AI assistant powered by Mistral LLMs.
- Create and manage multiple conversations.
- Access their conversation history.
- Receive real-time streamed responses.
- Upload PDF documents.
- Ask questions about their own documents using RAG.
- Benefit from semantic search powered by embeddings.

## Tech Stack

### Frontend
- Next.js
- React
- TypeScript
- Tailwind CSS
- shadcn/ui
- Lucide React
- React Markdown

### Backend
- Python
- FastAPI
- Uvicorn
- SQLAlchemy
- Pydantic

### AI & Machine Learning
- Mistral AI API
- Large Language Models (LLMs)
- Embeddings
- Retrieval-Augmented Generation (RAG)
- LangChain (planned)

### Database & Infrastructure
- PostgreSQL
- Qdrant (Vector Database)
- Psycopg
- REST API
- Server-Sent Events (SSE)

## Architecture

```text
mistral-chat/
│
├── frontend/
│   ├── src/
│   │   ├── app/
│   │   ├── components/
│   │   ├── hooks/
│   │   ├── lib/
│   │   └── types/
│   ├── public/
│   └── package.json
│
├── backend/
│   ├── app/
│   │   ├── main.py
│   │   ├── routes/
│   │   ├── services/
│   │   ├── models/
│   │   ├── schemas/
│   │   └── core/
│   ├── requirements.txt
│   └── .env
│
├── .gitignore
└── README.md
```

## Getting Started

### 1. Clone the repository

```bash
git clone https://github.com/moonspark78/ia-chat-mistralAI-.git

cd ia-chat-mistralAI-
```

### 2. Frontend Setup

Navigate to the frontend directory:

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

The frontend will be available at:

http://localhost:3000

### 3. Backend Setup

Navigate to the backend directory:

```bash
cd backend
```

Create a Python virtual environment:

```bash
python3 -m venv venv
```

Activate the environment:

```bash
source venv/bin/activate
```

Install dependencies:

```bash
pip install fastapi uvicorn mistralai python-dotenv sqlalchemy "psycopg[binary]"
```

### 4. Environment Variables

Create a `.env` file inside the backend directory:

```env
MISTRAL_API_KEY=your_mistral_api_key

DATABASE_URL=postgresql+psycopg://user:password@localhost:5432/mistral_chat
```

Get your API key from:

https://console.mistral.ai/

**Security:** Never expose your Mistral API key in the frontend or commit your `.env` file to GitHub.

### 5. Run the Backend

Once the FastAPI application has been implemented:

```bash
uvicorn app.main:app --reload
```

The API will be available at:

http://localhost:8000

Interactive API documentation:

http://localhost:8000/docs

## Core Features

| Feature | Description | Status |
|---|---|---|
| AI Chat | Conversational assistant powered by Mistral | Planned |
| Multi-turn conversations | Context-aware conversations | Planned |
| Conversation history | Persistent conversation storage | Planned |
| Streaming responses | Real-time LLM generation using SSE | Planned |
| User authentication | Secure user accounts | Planned |
| PostgreSQL | Persistent data storage | Planned |
| Model selection | Select different Mistral models | Planned |
| PDF upload | Upload and process documents | Planned |
| RAG pipeline | Document-based question answering | Planned |
| Embeddings | Semantic text representations | Planned |
| Qdrant | Vector similarity search | Planned |
| Tool Calling | LLM interaction with external tools | Planned |

## RAG Architecture

The application will integrate a Retrieval-Augmented Generation pipeline to allow users to interact with their own documents.

Expected workflow:

```text
PDF Upload
    |
    v
Text Extraction
    |
    v
Text Chunking
    |
    v
Embedding Generation
    |
    v
Qdrant Vector Database
    |
    v
Semantic Search
    |
    v
Relevant Context Retrieval
    |
    v
Mistral LLM
    |
    v
Contextual Answer + Citations
```

## Development Roadmap

**Phase 1 – Backend Foundation**
- Initialize FastAPI.
- Integrate the Mistral AI API.
- Implement the first chat endpoint.
- Test requests and responses.

**Phase 2 – Frontend Development**
- Build the ChatGPT-inspired interface.
- Implement the conversation sidebar.
- Create the messaging interface.
- Connect Next.js to FastAPI.

**Phase 3 – Persistence & Streaming**
- Integrate PostgreSQL.
- Implement conversation management.
- Add real-time streaming.
- Implement authentication.

**Phase 4 – Generative AI & RAG**
- Implement PDF processing.
- Generate document embeddings.
- Integrate Qdrant.
- Build semantic retrieval.
- Generate answers with document citations.

**Phase 5 – Advanced AI Features**
- Implement Tool Calling.
- Add model selection.
- Improve prompt engineering.
- Optimize retrieval and response quality.

## Learning Objectives

This project aims to develop practical skills in:

- Full-stack application development.
- Large Language Model integration.
- Generative AI application architecture.
- Prompt engineering.
- Embeddings and vector databases.
- Retrieval-Augmented Generation.
- API development with FastAPI.
- Real-time AI response streaming.
- Database design and persistence.

## Author

**Omar**

GitHub: https://github.com/moonspark78

---

*Built as a portfolio project to explore Full-Stack Development, Generative AI, LLMs and RAG systems.*
