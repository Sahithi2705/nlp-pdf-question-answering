# nlp-pdf-question-answering
NLP PDF Question Answering using Sentence Transformers and FAISS
Overview

PDF Question Answering is a Natural Language Processing (NLP) application that enables users to ask questions about the contents of a PDF document. Instead of manually searching through lengthy documents, the system extracts text from the PDF, converts it into semantic embeddings using Sentence Transformers, and retrieves the most relevant sections using FAISS vector search. This approach provides fast, context-aware document retrieval for efficient information access.

Objective

To build a PDF Question Answering system that extracts text from PDF documents, generates semantic embeddings, indexes them using FAISS, and retrieves the most relevant document sections in response to user questions.

Tools and Libraries
Python
PyMuPDF (fitz)
Sentence Transformers
FAISS
NLTK
NumPy
Google Colab
Dataset

The project accepts any user-uploaded PDF document. The PDF text is extracted, divided into manageable chunks, embedded into vector representations, and indexed for semantic retrieval.

Implementation Steps
Install and import the required libraries.
Upload a PDF document.
Extract text from all PDF pages.
Split the extracted text into smaller chunks.
Generate semantic embeddings using Sentence Transformers.
Build a FAISS vector index.
Accept a user question.
Convert the question into an embedding.
Retrieve the most relevant document chunks using semantic similarity.
Display the retrieved sections and similarity scores.
System Architecture
            User Uploads PDF
                    │
                    ▼
          Extract Text (PyMuPDF)
                    │
                    ▼
            Split into Chunks
                    │
                    ▼
      Sentence Transformer Embeddings
                    │
                    ▼
           FAISS Vector Database
                    │
                    ▼
             User Question
                    │
                    ▼
          Generate Query Embedding
                    │
                    ▼
          Semantic Similarity Search
                    │
                    ▼
      Most Relevant PDF Sections
Model Information
Embedding Model
Model: all-MiniLM-L6-v2
Architecture: Sentence Transformer
Embedding Dimension: 384
Vector Database
Library: FAISS
Index Type: IndexFlatL2
Sample Output
User Question
What is Natural Language Processing?
Retrieved Sections
Natural Language Processing enables computers to understand and process human language.

It is widely used in chatbots, sentiment analysis, machine translation, and question answering systems.
Search Statistics
Total Chunks Indexed : 48

Top Results Retrieved : 3
Applications
PDF Search Engines
Research Paper Analysis
Enterprise Knowledge Management
Legal Document Search
Healthcare Report Retrieval
Educational Assistants
Technical Documentation Search
Digital Libraries
Advantages
Supports semantic search instead of keyword matching.
Retrieves relevant information from large PDF documents quickly.
Works with any text-based PDF.
Easily scalable to large document collections.
Provides a foundation for Retrieval-Augmented Generation (RAG) systems.
Conclusion

This project demonstrates how semantic embeddings and vector similarity search can be combined to build an efficient PDF Question Answering system. By leveraging Sentence Transformers and FAISS, the application retrieves contextually relevant information from PDF documents, making document exploration faster, smarter, and more user-friendly.

requirements.txt
pymupdf
sentence-transformers
faiss-cpu
nltk
numpy
