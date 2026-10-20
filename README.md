# LangChain Agentic AI Examples

A collection of AI applications built with **Python, LangChain, LangGraph, and Streamlit**. Explore retrieval-augmented generation (RAG), tool calling, conversational memory, web search, and natural-language database interaction through working applications.

## Projects

### 1. Multi-PDF RAG Chatbot

Ask questions about uploaded PDF documents and retrieve relevant content to support responses.

- Ingest multiple PDF documents and split text into overlapping chunks.
- Generate embeddings and build an in-memory vector index.
- Retrieve the top three semantically relevant chunks.
- Expose document retrieval as a tool for an AI agent.
- Provide an interactive chat interface with Streamlit.

**Technologies:** Python, LangChain, LangGraph, OpenAI Embeddings, Groq, Streamlit.

### 2. Google Search Agent with Conversational Memory

An AI assistant that combines web search with conversational context.

- Integrate Google Serper search as an agent tool.
- Use a language model to process questions and search results.
- Maintain conversation state using thread-based checkpointing.
- Stream responses through a Streamlit interface.

**Technologies:** Python, LangChain, LangGraph, Groq, Google Serper, Streamlit.

### 3. SQL Task Management Agent

Manage tasks through natural-language instructions and database tools.

- Interpret user requests through an LLM-powered agent.
- Connect the agent to a SQLite database.
- Support task creation, retrieval, updates, and deletion.
- Use tool-based workflows to translate requests into database operations.
- Present the interaction through a conversational interface.

**Technologies:** Python, LangChain, SQL, SQLite, LLM tool calling.

## Architecture and concepts

This repository demonstrates document ingestion, semantic retrieval, agent tool selection, conversational state, external API integration, and database operations.

## Prerequisites

- Python installed on your computer.
- Git.
- API keys for the model and search services required by your selected application.

## Installation

Clone the repository:

```bash
git clone https://github.com/MehtaVishesh/agentic-ai-langchain-python.git
cd agentic-ai-langchain-python
```

Create and activate a virtual environment.

**Windows PowerShell**

```powershell
python -m venv .venv
.venv\Scripts\Activate.ps1
```

**macOS or Linux**

```bash
python -m venv .venv
source .venv/bin/activate
```

Install the dependencies:

```bash
python -m pip install --upgrade pip
pip install -r requirements.txt
```

## Configuration

Create a `.env` file in the project root. Add the API keys required by the application you want to run.

```dotenv
OPENAI_API_KEY=your_openai_api_key
GROQ_API_KEY=your_groq_api_key
SERPER_API_KEY=your_serper_api_key
```

Replace the placeholder values with your own credentials. Configure only the services that your selected application uses.

## Run the applications

**Multi-PDF RAG Chatbot**

```bash
streamlit run apps/streamlit_pdf_upload_rag_chatbot.py
```

**Google Search Agent**

```bash
streamlit run apps/streamlit_google_search_agent_with_memory.py
```

**SQL Task Management Agent**

```bash
streamlit run apps/task_management_sql_agent.py
```

Open the local URL displayed by Streamlit in your browser.

## Repository structure

```text
.
├── apps/
│   ├── streamlit_pdf_upload_rag_chatbot.py
│   ├── streamlit_google_search_agent_with_memory.py
│   └── task_management_sql_agent.py
├── requirements.txt
└── .gitignore
```

## Explore the code

Begin with the PDF chatbot to understand document retrieval and embeddings. Then explore the search agent to understand tool calling and conversational state. Finally, examine the SQL agent to see how language models interact with structured data.

## Author

**Vishesh Mehta** — AI Engineer, Melbourne, Australia.

[GitHub](https://github.com/MehtaVishesh) · [LinkedIn](https://www.linkedin.com/in/vishesh-mehta-516427217/)
