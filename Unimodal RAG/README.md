# Text-Based RAG System using
This project implements a Retrieval-Augmented Generation (RAG) pipeline that answers user questions by retrieving the most relevant information
from a custom document collection and generating an answer using a Transformer-based language model. Instead of relying only on the language model’s 
internal knowledge, the system enhances responses by grounding them in retrieved context from an external dataset.

# System Overview

This project follows the standard RAG workflow:

🔹 Step 1: Document Chunking
- The dataset is split into overlapping chunks to improve retrieval quality and preserve context.
- Chunk size: 80 characters
- Overlap: 20 characters

🔹 Step 2: Embedding Generation
- Each chunk is transformed into a dense vector using:
  SentenceTransformer("all-MiniLM-L6-v2")

🔹 Step 3: Vector Storage (FAISS)
- All embeddings are stored in a FAISS index:
  IndexFlatL2 (L2 distance similarity search)

🔹 Step 4: Retrieval
- For a given query, the system retrieves the top-k most similar chunks using FAISS.
- Top-k retrieval: 2 chunks

🔹 Step 5: Answer Generation
- The retrieved chunks are passed into a generative language model: google/flan-t5-small
- The final answer is generated using only the retrieved context.

# Technologies Used

- Python
- SentenceTransformers
- FAISS
- NumPy
- HuggingFace Transformers
- FLAN-T5 (Text2Text Generation)

# Usage

Install dependencies:
```python
pip install sentence-transformers faiss-cpu transformers torch numpy
```
