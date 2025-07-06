# Medical AI RAG Assistant

A sophisticated medical document analysis and Q&A system built with RAG (Retrieval Augmented Generation) architecture, combining advanced language models with document processing capabilities.

## Features

- **Document Processing**: Upload and process medical PDFs for knowledge base creation
- **Intelligent Q&A**: Chat interface for medical document queries using Groq's LLaMA 3 70B model
- **RAG Architecture**: Utilizes vector store for efficient document retrieval and contextual answers
- **User-Friendly Interface**: Streamlit-based chat UI for seamless interaction
- **Source Attribution**: Provides reference to source documents for transparency

## Architecture

### Frontend (Streamlit)
- Interactive chat interface
- PDF document upload functionality
- Real-time response display
- Chat history management

### Backend (FastAPI)
- RESTful API endpoints for document upload and queries
- PDF processing and vectorization
- Integration with Groq's LLM
- Pinecone vector store for efficient retrieval

## Setup

1. Clone the repository
2. Install dependencies:
   ```bash
   cd server
   pip install -r requirements.txt
   cd ../client
   pip install -r requirements.txt
   ```
3. Set up environment variables in `.env`:
   - GROQ_API_KEY
   - PINECONE_API_KEY
   - GOOGLE_API_KEY
   - PINECONE_INDEX_NAME

## Usage

1. Start the backend server:
   ```bash
   cd server
   uvicorn main:app --reload
   ```

2. Launch the frontend:
   ```bash
   cd client
   streamlit run app.py
   ```

3. Upload medical documents and start asking questions through the chat interface

