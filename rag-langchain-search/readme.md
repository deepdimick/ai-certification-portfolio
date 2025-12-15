# LangChain RAG Search

![Python](https://img.shields.io/badge/Python-3.9+-blue)
![LangChain](https://img.shields.io/badge/LangChain-0.2.1-green)
![ChromaDB](https://img.shields.io/badge/ChromaDB-0.4.24-orange)
![License](https://img.shields.io/badge/License-MIT-green)

A comprehensive demonstration of retrieval strategies for Retrieval-Augmented Generation (RAG) systems using LangChain, IBM Watsonx AI, and ChromaDB vector store.

<!-- Optional: Add a screenshot or demo gif here -->
<!-- ![Demo](images/demo.png) -->

## Problem Statement

Effective information retrieval is critical for RAG systems. This project demonstrates multiple retrieval strategies to optimize document search and context relevance for large language model applications.

## Features

- Vector similarity search with configurable top-k results
- Maximal Marginal Relevance (MMR) for diversity-aware retrieval
- Similarity score threshold filtering for precision control
- Multi-query retrieval with LLM-generated query variations
- Self-querying with metadata filtering capabilities
- Parent document retrieval for context-rich responses

## Quick Start

### Prerequisites

```bash
pip install ibm-watsonx-ai==1.1.2 langchain==0.2.1 langchain-ibm==0.1.11
pip install langchain-community==0.2.1 chromadb==0.4.24 pypdf==4.3.1
```

### IBM Watsonx AI Credentials

Update the credentials in the notebook:
- Watsonx AI URL
- API key
- Project ID

### Run

Open `langchain_rag_search_styled_exact.ipynb` in Jupyter and run all cells.

## Retrieval Strategies

| Strategy | Use Case | Advantage |
|----------|----------|-----------|
| **Similarity Search** | Standard semantic retrieval | Fast, simple, effective baseline |
| **MMR Search** | Diverse result sets | Reduces redundancy in retrieved documents |
| **Score Threshold** | High-precision retrieval | Returns only highly relevant documents |
| **Multi-Query** | Ambiguous queries | Improves recall through query reformulation |
| **Self-Querying** | Metadata filtering | Extracts and applies structured filters |
| **Parent Document** | Context-rich answers | Retrieves small chunks, returns full documents |

## Architecture

| Component | Details |
|-----------|---------|
| **LLM** | IBM Watsonx AI (Mistral-Small-3) |
| **Embeddings** | IBM Slate-125M English Retriever |
| **Vector Store** | ChromaDB |
| **Text Splitter** | RecursiveCharacterTextSplitter |
| **Document Loaders** | TextLoader, PyPDFLoader |

## Project Structure

```
├── langchain_rag_search_styled_exact.ipynb
├── README.md
└── data/
    ├── companypolicies.txt (downloaded)
    └── langchain-paper.pdf (downloaded)
```

## Results

The notebook demonstrates each retrieval strategy with real examples, showing how different approaches affect document retrieval quality and relevance for RAG applications.

## Skills Demonstrated

- RAG system design and implementation
- Vector database configuration and usage
- Multi-strategy retrieval optimization
- LangChain framework proficiency
- IBM Watsonx AI integration

## License

MIT

## Acknowledgments

- Project completed as part of IBM AI Engineering Professional Certificate
- LangChain framework by LangChain Inc.
- Sample documents from IBM Skills Network
