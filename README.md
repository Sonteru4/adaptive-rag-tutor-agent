# Adaptive RAG Tutor Agent

A document-grounded tutoring agent with conversational memory, quiz generation, and multi-format document ingestion.

Sir Learnsworth is a Flask app that tutors over user-uploaded PDFs and DOCX files. Students sign in, upload documents, and chat with a RAG agent that answers from a per-user vector store. Quizzes can be generated from the same corpus, and language, word limits, and focus areas are configurable.

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
