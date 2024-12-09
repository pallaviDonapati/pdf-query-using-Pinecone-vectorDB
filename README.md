# pdf-query-using-Pinecone-vectorDB

Overview

This project enables querying a set of documents using a question-answering system powered by OpenAI's language models and Pinecone's vector search capabilities. The system first loads PDF documents from a specified directory, splits the text into chunks, and stores the embeddings of these chunks in Pinecone for efficient vector search. Users can input queries, and the system retrieves relevant document chunks based on cosine similarity, providing accurate answers from the content.

Project Overview

This repository contains code to query documents stored in Pinecone using OpenAI's models. The project demonstrates the full pipeline, including loading PDFs, splitting documents into manageable chunks, embedding these chunks into vectors, storing them in Pinecone, and retrieving answers based on a user query. The integration of LangChain ensures smooth interaction between document processing, embedding, and question answering.

Repository Contents

app.py: Main code to load documents, split them into chunks, embed using OpenAI, store in Pinecone, and retrieve answers based on a query.
requirements.txt: Contains all the necessary Python dependencies to run the project.

Key Features

Document Loading: PDF documents are loaded from a specified directory using the PyPDFDirectoryLoader.
Chunking: The documents are split into smaller chunks for easier embedding and retrieval using RecursiveCharacterTextSplitter.
Embedding: Text is embedded using OpenAI's embeddings to create vector representations of the document chunks.
Pinecone Storage: Pinecone is used to store the vector embeddings of the document chunks, enabling efficient similarity search.
Query Answering: User queries are answered by finding the most similar document chunks and using OpenAI's language model to generate a response based on those chunks.

Model Interaction

The project uses OpenAI for embedding and question answering. Pinecone is used for storing the embeddings and performing similarity search. Below are the key components:

Document Loading: PDF documents are loaded using PyPDFDirectoryLoader.

Text Chunking: The documents are split into smaller chunks using RecursiveCharacterTextSplitter.

Embedding: The chunks are embedded using OpenAI's OpenAIEmbeddings class to generate vector representations.

Vector Search: The embeddings are stored in Pinecone and queried using cosine similarity for document retrieval.

Question Answering: The retrieved document chunks are passed to OpenAI's model to generate an answer to the user's query.
