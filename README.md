# 🔍 Retrieval Augmented Generation (RAG) with LangChain using IBM Granite Models

Welcome to the **Retrieval Augmented Generation (RAG)** lab using **LangChain**, **IBM Granite LLMs**, and a vector database (**Milvus**). This project demonstrates how to augment LLMs by retrieving external contextual data to generate more factual, relevant, and accurate responses.

---

## 🚀 Overview

**Retrieval Augmented Generation (RAG)** enhances Large Language Models by integrating a document retrieval step before generating responses. It allows LLMs to "look up" facts from a knowledge base rather than relying solely on pre-trained data.

This lab:
- Indexes a text document using embeddings
- Stores the vectors in Milvus DB
- Retrieves relevant chunks at query time
- Feeds those chunks to a Granite model on Replicate for response generation

---

## 🧠 Use Cases

- ✅ Customer Support with contextual documents  
- ✅ Internal Knowledge Base Q&A  
- ✅ Domain-specific assistants (Finance, Legal, Healthcare)  
- ✅ Chatbots with real-time document grounding

---

## 🧱 Architecture

```text
           +--------------------+
           |    User Query      |
           +--------------------+
                    |
                    v
         +------------------------+
         |   Embedding Query      |
         +------------------------+
                    |
                    v
         +------------------------+
         |  Vector DB (Milvus)    |
         +------------------------+
                    |
                    v
         +------------------------+
         | Retrieve Top-K Chunks |
         +------------------------+
                    |
                    v
         +------------------------+
         |  IBM Granite LLM (RAG) |
         +------------------------+
                    |
                    v
         +------------------------+
         |   Final Generated Answer |
         +------------------------+
```

---
## 📁 Folder Structure
```
.
├── notebooks/
│   └── RAG_with_LangChain.ipynb       # Main Jupyter Notebook for the lab
├── data/
│   └── state_of_the_union.txt         # Sample knowledge base
├── scripts/
│   └── requirements.txt               # Dependency list
├── assets/
│   └── architecture.png               # Diagram/image (optional)
├── .env.example                       # Example for setting environment variables
└── README.md                          # You're here!
```
---
## ⚙️ Requirements

   - Python 3.10, 3.11, or 3.12
   - Google Colab or local environment
   - Replicate API Key
   - Dockerhub account (optional)
   - GitHub account

---

## 🧪 Installation
👉 Option 1: Run on Google Colab
👉 Option 2: Run locally

### Clone the repository
git clone https://github.com/yourusername/rag-granite-langchain.git
cd rag-granite-langchain

### Create and activate a virtual environment
python -m venv .venv
source .venv/bin/activate  # or .venv\Scripts\activate on Windows

### Install requirements
pip install -r scripts/requirements.txt

## 🔐 Environment Variables

Create a .env file based on .env.example and set your Replicate API key:

REPLICATE_API_TOKEN=your_replicate_token_here

### 🛠️ Run the Lab

Inside the virtual environment
jupyter notebook notebooks/RAG_with_LangChain.ipynb

---
## ✅ Key Features Demonstrated

    🔹 Document chunking using langchain.text_splitter

    🔹 Embeddings generation with IBM Granite Embedding Model

    🔹 Vector similarity search with Milvus

    🔹 Querying LLM with retrieved context using LangChain RAG chain

    🔹 Full pipeline orchestration with LangChain

---
## 📚 Resources

    🔗 IBM Granite Models on HuggingFace

    🔗 LangChain Documentation

    🔗 Milvus Vector Database

    🔗 IBM Granite RAG Notebook (Colab)

