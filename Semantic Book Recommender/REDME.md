# Semantic Book Recommender

A Semantic Book Recommender System built with Python, OpenAI, LangChain, Hugging Face, Chroma, and Gradio. This project recommends books based on semantic meaning, category, and emotional tone, offering a human-centric approach to discovering new books.

# Features

1- Semantic Search: Converts book descriptions into dense embeddings using OpenAI, enabling natural-language queries to find contextually relevant books.

2- Category Classification: Standardizes book categories and predicts missing labels using zero-shot classification.

3- Sentiment & Emotion Analysis: Fine-tuned emotion classification model captures the emotional tone of descriptions, including joy, sadness, anger, fear, surprise, disgust, and neutral.

4- Interactive Dashboard: Gradio interface allows users to input a book description, filter by category and emotion, and get ranked recommendations with book covers and titles.

# Project Workflow

1- Data Preprocessing: 

- Load and clean a 7,000-book dataset.

- Handle missing values, merge title and subtitle fields, filter descriptions, and compute features like book age and word count.

2- Vector Embeddings & Semantic Search

- Split book descriptions into chunks and create embeddings with OpenAI.

- Store embeddings in Chroma for semantic similarity search.

3- Text Classification

- Map categories to simplified labels (Fiction, Nonfiction, Children’s Fiction).

- Apply Hugging Face zero-shot classification to predict missing or ambiguous categories.

4- Sentiment & Emotion Analysis

- Fine-tuned emotion classifier applied to book descriptions.

- Aggregate sentence-level predictions into maximum emotion scores per book.

5- Interactive Gradio Dashboard

- Users can enter a book description, select category and emotional tone.

- System retrieves top recommendations based on semantic similarity, category, and emotion.

- Displays book covers and titles for easy browsing.
