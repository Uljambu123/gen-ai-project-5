# RAG Document Q&A With Groq And Llama3

## 1. Project Overview

This project implements a **Retrieval-Augmented Generation (RAG)** system using **Groq API and Llama3** to answer questions based on research papers. The application utilizes **LangChain**, **FAISS**, and **Hugging Face Embeddings** (or OpenAI embeddings) to create a vector database of document embeddings for efficient retrieval. 

The system is designed to take a user query, retrieve the most relevant document passages, and generate accurate responses using Llama3.

## 2. Objective

The goal of this project is to develop an **AI-powered Q&A system** that:

- Efficiently retrieves relevant information from research documents.
- Provides **context-aware** answers using **Groq-powered Llama3**.
- Allows document embeddings using **Hugging Face** or **OpenAI embeddings**.
- Uses **FAISS** for scalable document vector storage.
- Is built as an interactive **Streamlit** application.

## 3. Key Steps in the Project

1. **Load Environment Variables**:
   - Load API keys for OpenAI, Hugging Face, and Groq from `.env`.

2. **Initialize Llama3 and Embeddings**:
   - Use **Hugging Face Embeddings** (`all-MiniLM-L6-v2`) or **OpenAI Embeddings**.
   - Set up **Llama3-8B-8192** as the LLM.

3. **Document Ingestion and Preprocessing**:
   - Load **PDF documents** from a directory (`research_papers`).
   - Split text into **overlapping chunks** using `RecursiveCharacterTextSplitter`.

4. **Create Vector Embeddings**:
   - Convert document text into embeddings.
   - Store embeddings in a **FAISS** vector database.

5. **User Query Processing**:
   - Accept **user queries** through the Streamlit UI.
   - Retrieve **relevant document chunks** using the FAISS retriever.
   - Generate a response using **Llama3 and Groq API**.

6. **Display Results**:
   - Show the AI-generated response.
   - Display relevant document excerpts in a collapsible **Streamlit Expander**.

## 4. Conclusions

- The project successfully implements a **RAG-based Q&A system**.
- The **FAISS vector store** efficiently retrieves relevant research content.
- **Llama3** provides **context-aware, human-like responses**.
- The system can be **extended to different document types and LLM models**.

## 5. Technologies Used

- **Python**
- **Streamlit** (UI Framework)
- **LangChain** (LLM integration)
- **FAISS** (Vector search)
- **Groq API** (Llama3 model)
- **Hugging Face Embeddings** (`all-MiniLM-L6-v2`)
- **OpenAI Embeddings** (Optional)
- **PyPDFDirectoryLoader** (Document ingestion)
- **Dotenv** (Environment variable management)

## 6. Future Work

- Support for **more document formats** (TXT, DOCX, etc.).
- Implement **real-time document updates** for embeddings.
- Explore **alternative LLMs** (Claude, Gemini, GPT-4).
- Improve **retrieval accuracy** using advanced ranking techniques.
- Deploy as a **web service with API endpoints**.


