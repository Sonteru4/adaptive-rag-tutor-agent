# Adaptive RAG Tutor Agent

Personalized document-grounded tutoring agent with conversational memory, quiz generation, and multi-format document ingestion.

## Overview

Sir Learnsworth is a Flask web application that acts as an AI tutor over user-uploaded documents. Students authenticate, upload PDFs or DOCX files, and chat with a GPT-4 powered agent that answers questions using Retrieval-Augmented Generation over a per-user vector store. The agent supports configurable language, word limits, and focus areas.

Beyond Q&A, the system generates quizzes from uploaded material and conversation history using LangChain chains, stores conversation logs in Azure Cosmos DB, and provides a full web UI for chat, quiz, and authentication flows.

## Tech Stack

- Python, Flask, Flask-CORS
- LangChain (ConversationalRetrievalChain, LLMChain)
- OpenAI GPT-4
- Azure Cosmos DB (conversation persistence)
- PyPDF2, pdf2image, python-docx (document processing)
- Vector store per user (LangChain)

## Features

- User authentication with session management
- Document upload and chunking into per-user vector stores
- Conversational RAG chat with memory
- Configurable response language, word limit, and focus areas
- Quiz generation from documents and conversation context
- Conversation history stored in Azure Cosmos DB
- Web UI templates for login, homepage, chat, and quiz

## Getting Started

```bash
pip install -r requirements.txt
python main.py
```

Configure `.env` with `OPENAI_API_KEY`, `SECRET_KEY`, and Azure Cosmos DB settings (see `app/config/config.py`).

## Use Case

Deployed education and training scenarios where teams need a document-grounded tutor agent that adapts to uploaded material, maintains conversation context, and auto-generates assessments.
