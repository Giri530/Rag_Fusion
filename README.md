📚 RAG Fusion Chatbot using LangChain and ChromaDB

This project implements a Retrieval-Augmented Generation (RAG) pipeline for answering questions based on PDF documents. It leverages LangChain, ChromaDB, and Hugging Face Transformers to retrieve relevant context and generate accurate responses.

🚀 Features

📄 Load and process PDF documents
🧠 Generate embeddings using all-MiniLM-L6-v2
🔍 Retrieve relevant chunks with ChromaDB
🤖 Answer queries using LLM from Hugging Face
🧠 Maintain conversational context with memory

🛠️ Tech Stack

LangChain
ChromaDB (as the vector store)
sentence-transformers/all-MiniLM-L6-v2 (Embeddings)
HuggingFaceHub (for LLM)
PyPDFLoader (PDF loading)
Python

📂 Workflow

Document Loading:

PDFs are loaded using PyPDFLoader and split into manageable text chunks.

Embeddings and Vector Store:

Each chunk is converted into a vector using all-MiniLM-L6-v2.
The vectors are stored and indexed using ChromaDB (in-memory).

Conversational Retrieval and Generation:

User questions are passed into a ConversationalRetrievalChain.
The chain retrieves relevant context and generates answers using an LLM from Hugging Face.
Conversation history is maintained using a memory buffer.

✅ Requirements

Install the required packages:

pip install langchain chromadb PyPDF2 sentence-transformers

HUGGINGFACEHUB_API_TOKEN=your_huggingface_api_key
