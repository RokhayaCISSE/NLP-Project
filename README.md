# NLP-Project
Machine Learning for Natural Language Processing

# 🧠 Concept and Named Entity Recognition with Knowledge-Augmented Transformers

This repository presents a comparative study of **BERT** and **ERNIE 2.0** models on the **Concept and Named Entity Recognition (CNER)** task. The project was conducted in the context of the **Natural Language Processing (NLP)** course at **ENSAE Paris** during the 2024–2025 academic year.

---

## 📚 Context

Named Entity Recognition (NER) traditionally focuses on identifying proper nouns (e.g., people, locations, organizations). However, many real-world applications also require recognizing **nominal concepts** (e.g., diseases, artifacts, laws), which are often expressed as common nouns. The **CNER task** proposed by Martinelli et al. (2024) unifies both entity and concept recognition into a single labeling framework.

This project aims to assess whether **knowledge-enriched language models** such as **ERNIE 2.0** can improve performance over standard models like **BERT** for this joint task.

---

## 🎯 Objectives

-  Evaluate the performance of a baseline **BERT-based model** on the CNER benchmark.
-  Introduce **ERNIE 2.0** (knowledge-augmented Transformer) in the same architecture and compare results.
-  Analyze whether access to structured knowledge improves prediction on **rare categories**.
  
---

## Methodology

- **Architecture**: Transformer encoder with a 2-layer classification head (same as CNER paper baseline).
- **Models**: 
  - `bert-base-cased`
  - `nghuyong/ernie-2.0-base-en`

---

## Evaluation

Both models were trained and evaluated under identical conditions with precision, recall, F1 and accuracy

---

##  Observed Limitations

-  **Computational budget**: Due to limited GPU time, the number of epochs was reduced to 1. Performance could improve with longer training.
-  **Subset training**: Only a 10,000-sentence sample was used, which may not fully capture the diversity of the CNER task.
-  **Knowledge use remains shallow**: ERNIE incorporates structured knowledge during pretraining only. More dynamic or explicit knowledge use (e.g., K-BERT, retrieval-augmented models) could further improve concept recognition.



