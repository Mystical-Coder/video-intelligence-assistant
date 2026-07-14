# Video Intelligence Assistant

An AI powered application that enables users to interact with YouTube videos using natural language. The application leverages **Retrieval Augmented Generation (RAG)** to retrieve relevant transcript context and generate accurate, context aware responses using **Google Gemini**.

## Features

* Chat with any YouTube video using natural language
* Automatic YouTube transcript extraction
* Semantic search using vector embeddings
* Context aware question answering with RAG
* Google Gemini integration for response generation
* Fast similarity search with FAISS
* Interactive Streamlit web interface

## Architecture

```text
YouTube URL
     │
     ▼
Extract Video ID
     │
     ▼
Fetch Transcript
     │
     ▼
Split into Chunks
     │
     ▼
Generate Embeddings
     │
     ▼
Store in FAISS
     │
     ▼
User Question
     │
     ▼
Retrieve Relevant Context
     │
     ▼
Prompt Construction
     │
     ▼
Google Gemini
     │
     ▼
Generated Response
```

## Tech Stack

### Frontend

* Streamlit

### AI and LLM

* Google Gemini
* LangChain
* Retrieval Augmented Generation (RAG)
* Prompt Engineering

### Embeddings and Retrieval

* Hugging Face Embeddings
* FAISS Vector Database

### Data Source

* YouTube Transcript API

## Project Workflow

1. User provides a YouTube video URL.
2. The application extracts the transcript.
3. The transcript is split into semantic chunks.
4. Embeddings are generated for each chunk.
5. Chunks are indexed using FAISS.
6. User asks a question.
7. Relevant transcript chunks are retrieved.
8. Gemini generates an answer using only the retrieved context.

## Installation

Clone the repository

```bash
git clone https://github.com/<your username>/video-intelligence-assistant.git
```

Navigate to the project directory

```bash
cd video-intelligence-assistant
```

Install the dependencies

```bash
pip install -r requirements.txt
```

Create a `.env` file

```env
GOOGLE_API_KEY=YOUR_GEMINI_API_KEY
```

Run the application

```bash
streamlit run app.py
```


## Project Structure

```text
video-intelligence-assistant/
│
├── app.py
├── requirements.txt
├── README.md
```

## Future Improvements

* AI agent workflow for multi step task execution
* Tool calling and function calling support
* Conversation memory
* Multi video knowledge base
* PDF and document ingestion
* Web search integration
* Meeting and lecture summarization
* Flashcard and quiz generation
* Export responses to PDF or Markdown
* Multi language transcript support
* Docker deployment
* Authentication and user management

## License

This project is licensed under the MIT License.
