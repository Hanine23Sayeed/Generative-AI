# 📌 Multimodal RAG (Text + Tables + Images) using LangChain + FAISS

This project implements a **Multimodal Retrieval-Augmented Generation (RAG)** pipeline that allows you to ask questions about a PDF file containing **text, tables, and images**.

It extracts content from a PDF, generates summaries for each modality (text/table/image), stores them in a **FAISS vector database**, and retrieves the most relevant information to generate accurate answers using an LLM.

---

## 🚀 Features

✅ Extract **text blocks** from PDF  
✅ Extract **tables** with structure inference  
✅ Extract **images** and generate captions using Vision LLM  
✅ Summarize text + tables using GPT model  
✅ Store embeddings in **FAISS vectorstore**  
✅ Retrieve relevant multimodal context and answer questions  
✅ Display retrieved relevant images

---

## 🏗️ Workflow Overview

1. **PDF Parsing** using `unstructured.partition.pdf`
2. **Text & Table Summarization** using `gpt-3.5-turbo`
3. **Image Captioning** using `gpt-4-vision-preview`
4. **Embedding & Indexing** using `OpenAIEmbeddings`
5. **Similarity Search** using FAISS
6. **Answer Generation** using retrieved context

---
# Install Dependencies

```python
pip install langchain unstructured faiss-cpu openai tiktoken pillow

For full PDF extraction support: pip install "unstructured[pdf]"






