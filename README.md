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

## Code Explanation

The code is divided into several functions and a class:

*   `tokenize(text)`: Splits input text into a list of lowercase words.
*   `build_vocab(docs)`: Creates a unique list of words from a list of documents.
*   `text_to_vector(text, vocab)`: Converts text to a vector based on the provided vocabulary.
*   `cosine_similarity(v1, v2)`: Calculates the cosine similarity between two vectors.
*   `VectorStore` Class:
    *   `__init__(self, documents)`: Initializes the vector store with a list of documents, building the vocabulary and document vectors.
    *   `search(self, query, k=3)`: Searches for the top `k` documents most similar to the query.

The main part of the script demonstrates how to use the `VectorStore` class with a sample set of documents.

## Future Enhancements (Optional)

*   Implement more advanced tokenization (e.g., removing stop words, stemming/lemmatization).
*   Use different vectorization techniques (e.g., TF-IDF).
*   Incorporate a language model to actually generate a response based on the retrieved documents (true RAG).
*   Improve efficiency for larger document sets.
