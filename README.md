# EXP-13
# RAG LCEL Chain

## Aim
To construct a basic Retrieval-Augmented Generation (RAG) chain using LangChain Expression Language (LCEL), FAISS, and an OpenAI language model.

## Problem Statement
Retrieve the two most relevant chunks from a climate-change document and use the retrieved context to answer questions through an LCEL chain.

## Technologies Used
- Python
- LangChain
- LCEL
- FAISS vector store
- OpenAI embeddings
- GPT-3.5-turbo

## Algorithm
1. Define the climate-change text.
2. Split the text into chunks using `RecursiveCharacterTextSplitter`.
3. Generate embeddings using `OpenAIEmbeddings`.
4. Create a FAISS vector store.
5. Convert the vector store into a retriever with `k=2`.
6. Create a prompt containing `{context}` and `{question}`.
7. Build the chain using LCEL pipe syntax.
8. Invoke the chain with two questions.
9. Display retrieved chunks and generated answers.

## Project Structure
```text
RAG_LCEL_Chain/
├── main.py
├── README.md
├── requirements.txt
└── .gitignore
```

## Installation
Install dependencies:

```bash
pip install -r requirements.txt
```

## API Key Setup

Windows PowerShell:

```powershell
$env:OPENAI_API_KEY="your_api_key_here"
```

Linux/macOS:

```bash
export OPENAI_API_KEY="your_api_key_here"
```

Replace the placeholder with your valid OpenAI API key. Never upload your API key to GitHub.

## Run the Experiment

```bash
python main.py
```

## Expected Output
The program prints the number of document chunks, each test question, the two retrieved chunks, and the generated answer.

Test questions:
1. What causes climate change?
2. What are the effects of climate change?

Answers and retrieved chunks may vary depending on the embedding and language models used.

## Conclusion
This experiment demonstrates a basic RAG pipeline using LCEL. It retrieves relevant context from a FAISS vector store and uses that context to generate answers grounded in the indexed document.
