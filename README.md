# Information-Retrieval
Arabic Information Retrieval Project

1. Project Overview

This project implements a complete end-to-end Arabic Information Retrieval (IR) system that integrates classical retrieval models with modern neural re-ranking techniques. The system supports Arabic text preprocessing, Boolean retrieval, ranked retrieval using TF-IDF and BM25, query expansion with word embeddings, and neural re-ranking using AraBERT.

The goal of the project is to study and compare different retrieval approaches for Arabic text and evaluate their effectiveness using standard IR metrics.

2. Implemented Components

🔹 Arabic Preprocessing
Diacritics removal
Character normalization (Alef forms, Ta Marbuta, etc.)
Tokenization
Stopword removal

🔹 Indexing & Boolean Retrieval
Inverted index construction
Boolean search with AND / OR / NOT operators

🔹 Ranked Retrieval
TF-IDF with cosine similarity
BM25 ranking model

🔹 Query Expansion
Word2Vec embeddings trained on the document corpus
Expansion of queries with semantically related terms

🔹 Neural Re-Ranking
AraBERT-based semantic re-ranking
Applied only to top-ranked BM25+QE documents for efficiency

🔹 Evaluation
Precision@k
Mean Average Precision (MAP)
nDCG@k
Mean Reciprocal Rank (MRR)

🔹 Visualization
Metric comparison plots (Precision@k, MAP@k, nDCG@k, MRR)

3. Dataset
Dataset Used: ArabicaQA (training split)

Each question is treated as a user query

The associated answer text is considered the relevant document

The dataset enables direct evaluation of retrieval performance

4. How to Run the Code
   
4.1 Requirements
The project was implemented in Python 3.
Required libraries:
pip install pandas numpy scikit-learn matplotlib gensim torch transformers

4.2 Running the Notebook
1.Open Arabic_IR_Assignment_Full.ipynb
2.Ensure arabica-train.csv or dataset.csv is in the same directory
3.Run all cells sequentially
4.Evaluation tables and plots will be generated automatically

5. Evaluation Setup
The system evaluates the following retrieval configurations:
TF-IDF

BM25

BM25 with Query Expansion (BM25+QE)

BM25 with Query Expansion and Neural Re-Ranking (BM25+QE+AraBERT)

Evaluation is performed using the paired question–answer structure of the dataset, where each query has one known relevant document.

6. References

All references, datasets, and tools used in this project are properly cited in the accompanying technical report.
