# LangChain Agentic AI Examples

Practical examples of AI applications built with **LangChain, LangGraph, Python, and Streamlit**. This repository demonstrates how to connect language models to external tools, retrieve information from documents, maintain conversation state, and interact with a relational database.

## Projects

### 1. Multi-PDF RAG Chatbot

Ask questions about uploaded PDF documents using retrieval-augmented generation (RAG).

- Loads PDF documents and splits their text into overlapping chunks.
- Creates embeddings and an in-memory vector store for semantic retrieval.
- Exposes document retrieval as a tool for an AI agent.
- Uses Streamlit to provide a conversational interface.

**Technologies:** LangChain, OpenAI embeddings, Groq, LangGraph checkpointing, Streamlit.

### 2. Google Search Agent with Conversational Memory

An AI assistant that uses Google Search to retrieve information and streams responses to a chat interface.

- Integrates Google Serper search with an AI agent.
- Uses thread-based checkpointing to retain conversation state.
- Streams responses to the user interface.

**Technologies:** LangChain, LangGraph, Groq, Google Serper, Streamlit.

### 3. Natural-Language SQL Task Manager

Manage tasks through natural-language instructions instead of writing SQL queries directly.

- Uses an AI agent with SQL database tools.
- Supports task creation, retrieval, updates, and deletion.
- Stores tasks in a SQLite database.
- Defines task statuses and rules for database operations.

**Technologies:** LangChain, LangGraph, SQLite, SQLDatabaseToolkit, Streamlit.

## Learning objectives

This repository demonstrates:

- Tool calling and agent orchestration.
- Retrieval-augmented generation and semantic search.
- Conversation state and in-memory checkpointing.
- Integration between language models and databases.
- Building interactive AI applications with Streamlit.

## Prerequisites

- Python 3.11 or a compatible version supported by the installed dependencies.
- Git.
- API credentials for the model and search providers used by each application.

## Setup

Clone the repository and enter the project directory:

```bash
git clone https://github.com/MehtaVishesh/agentic-ai-langchain-python.git
cd agentic-ai-langchain-python
```

Create and activate a virtual environment:

```bash
python -m venv .venv
```

Windows PowerShell:

```powershell
.venv\Scripts\Activate.ps1
```

macOS or Linux:

```bash
source .venv/bin/activate
```

Install the project dependencies:

```bash
python -m pip install --upgrade pip
pip install -r requirements.txt
```

Create a local `.env` file in the project root. Add the API credentials required by the application you want to run. Do not commit this file.

Example:

```dotenv
OPENAI_API_KEY=your_openai_api_key
GROQ_API_KEY=your_groq_api_key
SERPER_API_KEY=your_serper_api_key
```

Use only the credentials required by the selected application.

## Run an application

Run the PDF chatbot:

```bash
streamlit run apps/streamlit_pdf_upload_rag_chatbot.py
```

Run the Google Search agent:

```bash
streamlit run apps/streamlit_google_search_agent_with_memory.py
```

Run the SQL task manager:

```bash
streamlit run apps/task_management_sql_agent.py
```

Follow the instructions in the application to interact with the agent.

## Important implementation details

The PDF chatbot stores its vector index and conversation checkpoints in memory. These are temporary and do not provide persistent storage across application restarts.

The SQL task manager stores its data in a local SQLite database named `my_tasks.db`. Keep local database files and API credentials out of version control.

## Project structure

```text
.
├── apps/
│   ├── streamlit_pdf_upload_rag_chatbot.py
│   ├── streamlit_google_search_agent_with_memory.py
│   └── task_management_sql_agent.py
├── requirements.txt
└── .gitignore
```

## For learners

Start with the PDF chatbot to understand document ingestion and retrieval. Continue with the search agent to study tools and conversation state. Finish with the SQL task manager to explore database integration.

## Author

**Vishesh Mehta** — AI Engineer based in Melbourne, Australia.

[GitHub](https://github.com/MehtaVishesh) · [LinkedIn](https://www.linkedin.com/in/vishesh-mehta-516427217/)
