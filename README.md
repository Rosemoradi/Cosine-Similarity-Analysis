# Cosine-Similarity-Analysis
Here I explored word semantics using GloVe word embeddings. Includes cosine similarity analysis, vector operations (e.g., king - man + woman = queen), and PCA-based visualization. This NLP project highlights how pretrained word vectors can model analogies and semantic similarity


# 🧠 Word Embeddings, Semantic Similarity & Analogies with GloVe (NLP Project)

This project is an educational deep dive into **word embeddings** using **GloVe (Global Vectors for Word Representation)**. Word embeddings are numerical vector representations of words that capture semantic meaning based on the context in which words appear. In this notebook, we explore how GloVe vectors allow us to perform **semantic similarity**, solve **analogies**, and **visualize word relationships** using dimensionality reduction—all in an intuitive, beginner-friendly way.

---

In traditional NLP, words were often represented as one-hot vectors (sparse and context-free), which limited how machines could understand meaning. GloVe solves this by embedding words into a continuous vector space, trained on co-occurrence statistics from a massive corpus. Words used in similar contexts end up geometrically close in vector space.

For example:
- `cosine_similarity(glove["king"], glove["queen"])` is high
- `glove["king"] - glove["man"] + glove["woman"]` ≈ `glove["queen"]`

This notebook demonstrates how GloVe embeddings can be loaded and used to:
- Measure **semantic closeness** between words
- Perform **word analogy tasks** using vector arithmetic
- Reduce vector dimensionality using **PCA** for **visualization**
- Build a deeper understanding of distributed word representations

---

## 🧪 What This Notebook Covers

1. **Loading GloVe Vectors**  
   We load `glove.6B.100d.txt`, which contains 100-dimensional word embeddings for over 400,000 words. Each word vector is parsed and stored in a Python dictionary for fast lookup.

   Example:
   glove["king"] → [0.5041, 0.1205, ..., -0.0691]


2. **Cosine Similarity for Semantic Closeness**
   Cosine similarity measures the angle between two word vectors. A smaller angle means the words are used in similar contexts. We implement a function to find the **top-N most similar words** to any given word using this technique.



3. **Word Analogy Tasks**
   We demonstrate that vector arithmetic captures relationships:

   ```
   king - man + woman ≈ queen
   Paris - France + Italy ≈ Rome
   ```

   This shows how embeddings model complex semantic patterns beyond simple similarity.

4. **PCA-Based Visualization**
   Since each word is embedded in 100-dimensional space, we use **Principal Component Analysis (PCA)** to project vectors into 2D. This allows us to **plot and cluster related words**—revealing patterns like:

   * Countries and their capitals
   * Gendered terms (man–woman, king–queen)
   * Plural vs. singular

---

## 🎓 Educational Value

This notebook is not just a technical demonstration—it’s a learning tool. It teaches you:

* What word embeddings are and **why they matter**
* How cosine similarity measures **semantic similarity**
* How vector spaces encode relationships between words
* How to reduce and visualize high-dimensional data
* How distributional semantics powers modern NLP

This project builds intuition for how advanced models like BERT, GPT, and other Transformers internally represent language.




## 📍 Why This Project Matters

Understanding how language can be converted into vectors—and how those vectors encode real relationships—is foundational to modern AI. This project helps demystify how machines learn about language and gives you hands-on skills for future NLP applications.

You’ll walk away knowing not only how to use embeddings—but how they work.

---

## 👩‍💻 Author

**Razieh Moradi**
Graduate Student, McMaster University
📫 moradr1@mcmaster.ca

---

## 📎 References

* [Stanford GloVe Project](https://nlp.stanford.edu/projects/glove/)
* Jurafsky & Martin, *Speech and Language Processing*
* scikit-learn documentation (PCA, cosine similarity)


