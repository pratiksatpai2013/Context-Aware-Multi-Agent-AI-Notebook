# Context-Aware Multi-Agent AI System 🚀

This repo contains code for a **context-aware, modular multi-agent system** built using **Nomic Embeddings**, **FAISS**, **LangChain**, and **Google Gemini LLM**, based on the tutorial published on MarkTechPost (July 27, 2025).

## 🎯 Overview

- Multiple agents collaborate with **semantic memory**, retrieving past knowledge via Nomic/Faiss embeddings.
- Agents reason using **Google Gemini**, maintaining a shared, chat-like context.
- The orchestration is powered by **LangChain**, enabling flexible chaining of agent roles (e.g. researcher, summarizer, dialogue agent).

## 🧩 Architecture

- PDF/text/data → Chunked documents → Nomic Embed → FAISS vector store
- User Query → Agent retriever → Contextual prompts → Gemini LLM → Agent actions/responses
- **Embedding**: Uses `nomic-embed-text-v1` to create vector representations.
- **Vector Store**: FAISS indexes for semantic search.
- **Chain Logic**: LangChain agents retrieving context, generating output, and optionally triggering actions.

## 🚀 Features

- **Modular agents**: Each performing specialized tasks (e.g. retrieval, summary, Q&A).
- **Embeddings + LLM Reasoning**: Agents fetch relevant memory chunks from FAISS and use Gemini for reasoning over them.
- **Context awareness**: Agents maintain conversational memory and context through vector retrieval.
- **Extensible and generalizable**: Add more agents or adapt to other LLMs/embedding models easily.

## 🧩 Use Cases

- Research assistants that recall previous session context
- Conversational agents with memory of past interactions
- Complex multi-step pipelines (analyzer → summarizer → chatbot)

## 🔐 Prerequisites

- Google Gemini API access
- Nomic Embed model access (e.g. `nomic-embed-text-v1`)
- Estimated memory and storage for FAISS indexing depends on corpus size

## 🔧 Extending the System

- Swap out Gemini for another LLM (OpenAI, Claude, Mistral)
- Use alternative vector store (ChromaDB, Milvus)
- Integrate additional agent roles (e.g. task planner, evaluator)
