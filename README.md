# Transforming a RAG Pipeline into an AI Agent

This project demonstrates how to evolve a basic large language model chatbot into a more capable **AI agent** by gradually introducing **retrieval-augmented generation (RAG)**, **query rewriting**, **optional retrieval decisions**, and **tool-based retrieval workflows**. The notebook walks through the full progression from a simple chatbot with no retrieval to a more agentic system that can decide when to search for information, rewrite user questions for better document retrieval, and use external context to generate stronger answers.

The implementation uses modern AI engineering components including **OpenAI**, **Qdrant**, **Docling**, **FastEmbed**, and an interactive **Jupyter chat interface**. Documents are downloaded, chunked, embedded, and stored in a vector database so the system can retrieve relevant context during conversations. This makes the project a practical example of how to design an intelligent assistant that moves beyond static prompting into a more dynamic and modular architecture.

## Project Objectives
 
The main goals of this project are to:

- Build a baseline chatbot with direct LLM interaction
- Introduce document ingestion and vector search for retrieval
- Improve retrieval quality through query rewriting
- Add logic for deciding when retrieval is necessary
- Transform the pipeline into a more autonomous AI agent
- Demonstrate retrieval as a callable tool inside the agent workflow

## Workflow Overview

The notebook follows a progressive architecture:

1. **Basic Chatbot**  
   A simple LLM-powered chatbot is created without retrieval or external context.

2. **Document Ingestion**  
   Source documents are downloaded and prepared for later retrieval.

3. **Basic RAG Pipeline**  
   Documents are chunked, embedded, and stored in Qdrant for similarity search.

4. **Query Rewriting**  
   User questions are rewritten into improved retrieval queries for better context matching.

5. **Optional Retrieval Decision**  
   The system decides whether retrieval is actually needed before searching the vector database.

6. **Agentic RAG**  
   The assistant can repeatedly decide to retrieve more context until it has enough information.

7. **Tool-Based Retrieval**  
   Retrieval is exposed as a tool the model can call, making the workflow more agent-like and extensible.

## Tools and Libraries

This project uses the following technologies:

- `openai`
- `qdrant-client`
- `docling`
- `fastembed`
- `jupyter-chat-widget`
- `requests`
- `json`

## Key Features

- Interactive chat-based notebook workflow
- Retrieval-augmented generation with vector search
- Query rewriting for stronger semantic retrieval
- Conditional retrieval logic
- Agentic multi-step reasoning pattern
- Tool calling for search and context retrieval
- In-memory vector database setup for lightweight experimentation

## Example Use Case

A source document is ingested into the vector database, and the assistant answers questions about its contents. Instead of relying only on the base model’s memory, the system retrieves relevant passages from the document and uses them to support the response. As the pipeline becomes more advanced, the assistant can determine when retrieval is needed, improve the search query, and repeatedly gather context in a more agentic way.

## Project Structure

```text
Transforming_a_RAG_pipeline_into_an_AI_Agent.ipynb
documents/
└── sonnet-4.5.md
