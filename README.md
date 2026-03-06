# Legal-compliance-RAG-Agent
# Legal Compliance RAG Agent

A Retrieval-Augmented Generation (RAG) agent designed to answer legal compliance questions by leveraging advanced embedding techniques, vector similarity search, and LLM capabilities. This system is optimized for querying and understanding legal documents such as constitutional frameworks and penal codes.

## 🎯 Overview

This project implements an intelligent legal compliance agent that combines:
- **Nomic Embedding Text** for semantic document understanding
- **COSINE Vector Similarity** for precise relevance matching
- **HNSW Search Algorithm** for efficient vector retrieval
- **Hybrid Search** combining multiple retrieval strategies
- **LangChain** for orchestration and chain management
- **Azure OpenAI** for advanced language model capabilities

The system is trained on legal documents including:
- The Constitution of Kenya 2010
- Penal Code documentation

## 🏗️ Architecture

### Core Components

1. **Embedding Layer**
   - Uses Nomic embedding model for converting text into high-quality semantic vectors
   - Supports efficient batch processing of legal documents

2. **Vector Storage & Retrieval**
   - HNSW (Hierarchical Navigable Small World) algorithm for fast approximate nearest neighbor search
   - COSINE similarity metric for measuring document relevance
   - Optimized for large-scale legal document libraries

3. **Hybrid Search Strategy**
   - Combines semantic vector search with traditional keyword matching
   - Ensures comprehensive retrieval of relevant legal references
   - Improves precision and recall for legal queries

4. **LangChain Integration**
   - Manages multi-step reasoning chains
   - Handles prompt engineering and context management
   - Orchestrates communication between components

5. **Language Model**
   - Azure OpenAI API integration
   - Generates contextual, accurate legal compliance responses
   - Supports advanced reasoning over retrieved documents

## 🚀 Features

- **Legal Document Processing**: Automatically indexes and processes legal documents
- **Semantic Search**: Find relevant legal information using natural language queries
- **Compliance Verification**: Verify compliance against legal frameworks
- **Context-Aware Responses**: Generates answers with proper legal references
- **Scalable Architecture**: Handles large document collections efficiently

## 📋 Requirements

See `Requirements.txt` for detailed dependencies including:
- langchain
- azure-openai
- nomic (embedding library)
- vector database libraries (HNSW compatible)

## 📚 Supported Documents

- **The_Constitution_of_Kenya_2010.pdf** - Constitutional framework and legal principles
- **Penal_Code.pdf** - Criminal law and penalties reference

## 💻 Usage

### Basic Query
```python
# Initialize the RAG agent
agent = LegalComplianceAgent(
    embedding_model="nomic-embed-text",
    vector_similarity="cosine",
    search_algorithm="hnsw"
)

# Query legal compliance
response = agent.query("What are the penalties for...")
