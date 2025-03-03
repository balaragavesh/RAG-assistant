# RAG-Powered Documentation Assistant

This project implements a **Retrieval-Augmented Generation (RAG) model** using **Phi-2** and **ChromaDB** to provide intelligent responses based on software user guide documentation. The system retrieves relevant document chunks and generates context-aware answers using a **hybrid search approach**.

## How It Works

1. **Hybrid Search (BM25 + Semantic Search)**  
   - **BM25**: A traditional keyword-based ranking algorithm that retrieves the most relevant passages based on term frequency.  
   - **Semantic Search**: Uses **ChromaDB** and embeddings to find conceptually similar text, even if it doesn't match exact keywords.  
   - The results from both methods are **ranked and merged** to ensure high-quality context retrieval.  

2. **Chunking & Processing**  
   - The retrieved documentation is split into **fixed-size chunks** to fit within the model’s context window.  
   - The best-matching chunks are selected for answer generation.  

3. **Answer Generation with Phi-2**  
   - The processed context is fed into **Microsoft’s Phi-2**, a state-of-the-art language model.  
   - It generates human-like responses by understanding the retrieved information. 

## Features
- **Hybrid Search:** Combines keyword and semantic search for better retrieval.
- **Contextual Responses:** Generates answers using **Phi-2** based on retrieved documentation.
- **Efficient Chunking:** Ensures relevant document sections fit within model constraints.
- **Seamless Integration:** Designed for embedding into existing software.

## License
This project is licensed under the **MIT License**. See the [LICENSE](LICENSE) file for details.

---



