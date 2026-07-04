📚 AI Research Paper Intelligence System

> **An AI-powered semantic search engine that helps researchers discover relevant Machine Learning papers by understanding the meaning of a query instead of relying on exact keyword matching.**
>
> The system searches through **50,000+ ArXiv Machine Learning research papers**, retrieves the most relevant results using **vector similarity search**, automatically **summarizes each paper**, and **extracts important research keywords** so users can quickly understand whether a paper is relevant without reading the entire abstract.

---

🚀 Why This Project?

Finding research papers using traditional search engines can be frustrating because they mostly rely on **keyword matching**.

For example, if you search:

> **"Deep learning for medical image analysis"**

A keyword-based search may miss papers that discuss **medical imaging**, **computer vision**, or **neural networks** without using the exact same words.

This project solves that problem using **Semantic Search**, allowing the system to understand the **meaning** behind a query rather than simply matching words.

✨ Features

✔ Semantic Search using Sentence Transformers

✔ Fast Vector Search using FAISS

✔ Automatic AI-generated Paper Summaries

✔ Keyword Extraction using KeyBERT

✔ Interactive Streamlit Web Application

✔ Search across **50,000+ Machine Learning Research Papers**

✔ Meaning-based Retrieval instead of Keyword Matching

 🖥️ How It Works

When a user enters a research query, the system performs the following steps:

### Step 1 — Encode the Query

The input query is converted into a **384-dimensional semantic embedding** using the **Sentence Transformer (all-MiniLM-L6-v2)**.

↓

### Step 2 — Semantic Search

The generated embedding is compared against embeddings of **50,000+ research papers** stored inside a **FAISS vector index**.

Instead of searching words, FAISS searches **semantic similarity**.

↓

### Step 3 — Retrieve Relevant Papers

The system returns the **Top-K most similar papers** ranked by cosine similarity.

↓

### Step 4 — Summarize Papers

Each retrieved abstract is summarized using **DistilBART**, making long abstracts much easier to read.

↓

### Step 5 — Extract Keywords

Important research topics are extracted using **KeyBERT**.

↓

### Step 6 — Display Results

The Streamlit interface displays

- Paper Title
- Similarity Score
- AI-generated Summary
- Important Keywords

allowing users to evaluate papers within seconds.

 🏗️ System Architecture

                     ArXiv ML Papers
                    (50,000+ Papers)
                            │
                            ▼
                  Data Cleaning & Processing
                            │
                            ▼
          Sentence Transformer (MiniLM-L6-v2)
                            │
                Generate Embeddings
                            │
                            ▼
                     FAISS Vector Index
                            ▲
                            │
                  User Research Query
                            │
                  Convert into Embedding
                            │
                            ▼
                  Retrieve Top-K Papers
                     ┌─────────────┐
                     │             │
                     ▼             ▼
          DistilBART         KeyBERT
        Summarization   Keyword Extraction
                     │
                     ▼
              Streamlit Web App


🛠️ Tech Stack

| Category | Technology |
|-----------|------------|
| Language | Python |
| Dataset | Hugging Face ML-ArXiv Papers |
| Embeddings | Sentence Transformers |
| Vector Search | FAISS |
| Summarization | DistilBART |
| Keyword Extraction | KeyBERT |
| Frontend | Streamlit |
| Data Processing | Pandas, NumPy |



 📊 Project Workflow

Load Dataset
      │
      ▼
Clean Research Papers
      │
      ▼
Generate Semantic Embeddings
      │
      ▼
Build FAISS Index
      │
      ▼
User Search Query
      │
      ▼
Convert Query into Embedding
      │
      ▼
Find Similar Papers
      │
      ▼
Generate Summary
      │
      ▼
Extract Keywords
      │
      ▼
Display Results

💡 Why These Technologies?

### Sentence Transformers

Used to convert research papers and user queries into dense semantic vectors that capture contextual meaning.


### FAISS

Provides extremely fast vector similarity search, making semantic retrieval efficient even across thousands of research papers.

### DistilBART

Generates concise summaries of long research abstracts, helping users understand papers quickly.

### KeyBERT

Automatically identifies the most important research topics and phrases from each paper.

🌟 Future Improvements

- Hybrid Search (Keyword + Semantic Search)
- Cross-Encoder Re-ranking
- Citation Network Visualization
- PDF Upload & Semantic Search
- Research Paper Recommendation System
- Research Chat Assistant (RAG)
- Docker Deployment
- Hugging Face Spaces Deployment

👩‍💻 Author

**Aditi**
(sharmaaditi4482@gmail.com)
