# LLM--RAG-with-Pinecone

# Document Retrieval System with Pinecone and OpenAI Embeddings

## Overview

This project is a document retrieval system that leverages **Pinecone**, a vector database, and **OpenAI embeddings** to efficiently store and retrieve large amounts of text data. The primary goal of this system is to ingest text documents, chunk them into smaller segments for more efficient processing, generate embeddings for each chunk, and store those embeddings in Pinecone for high-performance similarity search. The system then enables easy retrieval of the most relevant documents based on user queries.

By integrating **Langchain** for document processing, **OpenAI** for generating embeddings, and **Pinecone** for vector storage and retrieval, this project provides a fast and scalable solution to build powerful document search systems.

## Features

- **Document Chunking**: 
  Large documents are split into smaller chunks to fit within the token limit of embedding models. This allows the system to handle large documents by breaking them into more manageable pieces for faster and more accurate processing.

- **OpenAI Embeddings**: 
  OpenAI's **text-embedding models** are used to convert documents into high-dimensional vector representations. These embeddings capture the semantic meaning of the text, enabling more accurate and relevant document retrieval.

- **Pinecone Vector Database**: 
  Pinecone is used to store the embeddings of document chunks. Its high-performance vector search capabilities allow for fast and efficient retrieval of the most relevant document chunks based on similarity with the user's query.

- **Scalable Architecture**: 
  The system is designed to handle large datasets, making it suitable for document retrieval in a variety of industries, such as healthcare, finance, and etc.

- **Real-time Querying**: 
  Users can provide a query, and the system retrieves the most semantically similar chunks from the document corpus in real time.

## Prerequisites

Before running the project, ensure you have the following prerequisites:

1. **Python 3.10+**
2. **Pinecone Account**: You’ll need a Pinecone API key. You can obtain one by creating an account at [Pinecone](https://www.pinecone.io/).
3. **OpenAI API Key**: Get your OpenAI API key from [OpenAI](https://platform.openai.com/account/api-keys).
4. **Langchain**: This project utilizes the `langchain` library for document processing.

### Required Libraries

The following Python packages are required to run the project:
see `requirement.txt`
