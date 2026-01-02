# 📚 Personal AI Tutor (Powered by Gemini 1.5 Flash)

**Built for the Google Gen AI Kaggle Competition (5-Day Workshop)**

This project is a Retrieval-Augmented Generation (RAG) application that transforms static PDF textbooks into an interactive AI tutor. It reads documents, answers student queries with citation-based accuracy, and generates dynamic quizzes to test retention.

## 🧠 Problem Statement
Students often struggle to revise large textbooks or lecture materials efficiently. Traditional retrieval methods (Ctrl+F) lack context, and creating manual flashcards is time-consuming. This project automates the study process using Generative AI.

## 🛠️ Tech Stack
* **LLM:** Google Gemini 1.5 Flash
* **Orchestration:** LangChain
* **Vector Database:** FAISS (Facebook AI Similarity Search)
* **Embeddings:** Google Generative AI Embeddings
* **Language:** Python 3.10+

## ⚙️ Architecture Pipeline
1.  **Ingestion:** PDF documents are loaded and split into 1,000-token chunks.
2.  **Embedding:** Text chunks are converted to vectors and stored in a local FAISS index.
3.  **Retrieval:** User queries trigger a similarity search to fetch the top 3 relevant context chunks.
4.  **Generation:** Gemini 1.5 Flash synthesizes the retrieved context to answer the question or generate a JSON-structured quiz.

## ✅ Key Features
-   **Context-Aware Q&A:** Ask questions in natural language and receive answers grounded strictly in the provided PDF (reduces hallucinations).
-   **Automated Quiz Generation:** Forces the LLM to output structured JSON to create multiple-choice questions automatically.
-   **Fast Retrieval:** Sub-3-second query latency using FAISS for local vector search.

## 🚀 How to Run Locally

1.  **Clone the repository:**
    ```bash
    git clone [https://github.com/AnuragRai19/Personal-AI-tutor.git](https://github.com/AnuragRai19/Personal-AI-tutor.git)
    cd Personal-AI-tutor
    ```

2.  **Create a virtual environment and install dependencies:**
    ```bash
    python -m venv .venv
    source .venv/bin/activate  # On Windows: .venv\Scripts\activate
    pip install -r requirements.txt
    ```

3.  **Set up your API Key:**
    * Create a `.env` file in the root directory.
    * Add your Google API key:
        ```bash
        GOOGLE_API_KEY="YOUR_SECRET_API_KEY_HERE"
        ```

4.  **Run the Application:**
    * Launch the Jupyter Notebook `personal-ai-tutor.ipynb` to interact with the pipeline step-by-step.
