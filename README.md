Title: F7) SEC Filing Summarizer & Q&A (RAG) 
Problem Statement:
Publicly traded companies submit regulatory filings such as Form 10-K (Annual Reports) and Form 10-Q (Quarterly Reports) to the U.S. Securities and Exchange Commission (SEC). These filings contain essential information regarding a company’s financial performance, operational risks, business strategies, and future outlook. However, the documents are often lengthy, unstructured, and difficult to navigate, making manual analysis time-consuming and inefficient.
The objective of this project is to develop an AI-powered Retrieval-Augmented Generation (RAG) based Question Answering system that enables users to query SEC filings using natural language and receive accurate, concise, and context-aware responses. To ensure reliability and transparency, each generated answer is accompanied by source citations that reference the exact document segments used in the response.
Technologies Used:
1.Python – Core programming language
2.unstructured – Parsing and extracting text from SEC filing documents
3.LangChain – Orchestration of the RAG pipeline (retrieval + generation)
4.Embedding Models (OpenAI / Sentence-Transformers) – Convert text into vector representations
5.Vector Database (ChromaDB / FAISS) – Efficient storage and retrieval of document embeddings
6.Large Language Model (LLM) – Generate human-readable answers grounded in retrieved context
7.FastAPI (Optional) – Expose the question-answering system as a REST API endpoint

Workflow
1. Data Selection
   A small subset of SEC filings (10-K and 10-Q) is selected from the dataset.

2. Document Parsing
   Filing documents are processed using the *unstructured* library to extract clean and readable text.

3. Text Chunking
   Large documents are split into smaller, manageable text chunks while preserving metadata such as company name, filing type, and filing date.

4. Embedding Generation
   Each text chunk is converted into numerical vector embeddings using an embedding model.

5. Vector Indexing
   The embeddings and corresponding metadata are stored in a vector database to enable semantic search.

6. Query Processing
   When a user submits a question, the system retrieves the most relevant text chunks from the vector database.

7. Answer Generation
   The retrieved chunks are passed to the LLM, which generates a concise answer strictly based on the provided context.

8. Source Citation
   The system returns the generated answer along with references to the document chunks used, ensuring transparency and trust.
   
Output:
Natural language answers to investor or analyst queries related to SEC filings
Source citations (chunk IDs or document references) for every answer
Improved accessibility to complex financial and regulatory information
A scalable and reliable document intelligence system for financial analysis
