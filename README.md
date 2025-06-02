# CustomVectorDB-InHouseRAG
Learn the basics of vector search and RAG with this simple Python implementation, demonstrating the core components of a RAG system, including a simple vector store and similarity search.

## Features

*   **Tokenization:** Simple text splitting into lowercase words.
*   **Vocabulary Building:** Creates a unique list of words from a corpus of documents.
*   **Text Vectorization:** Converts text into a Bag-of-Words vector representation.
*   **Cosine Similarity:** Computes the similarity between two vectors.
*   **Vector Store:** Stores document vectors and allows for searching based on query similarity.
*   **Basic RAG Implementation:** Combines vector search with a knowledge base to answer queries.

## How it Works

1.  **Build Vocabulary:** A vocabulary is created from a collection of documents.
2.  **Vectorize Documents:** Each document in the collection is converted into a numerical vector based on the vocabulary (using the Bag-of-Words approach).
3.  **Store Vectors:** These document vectors are stored in a simple vector store.
4.  **Process Query:** When a query is received, it is also vectorized using the same vocabulary.
5.  **Similarity Search:** The query vector is compared to all document vectors in the store using cosine similarity.
6.  **Retrieve Top Results:** The documents with the highest similarity scores are retrieved.
7.  **Augment (Basic):** In this simple example, the most relevant document is returned as the "answer" to the query, simulating the retrieval part of RAG.
