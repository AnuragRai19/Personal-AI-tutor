# 📚 Personal AI Tutor using Gemini 1.5 Flash

This project builds a Personal AI Tutor that reads a PDF textbook, answers questions about it, and generates quizzes to help students study more efficiently.

## 🧠 Problem Statement

Students often struggle to revise large textbooks or lecture materials efficiently. Traditional methods of studying are time-consuming and lack personalized assistance. This project provides an AI-driven solution to this problem.

## ✅ Solution

This AI tutor uses Google’s Gemini 1.5 Flash model and a Retrieval-Augmented Generation (RAG) pipeline to provide:

-   **Contextual Question Answering:** Ask questions in natural language and get accurate answers based on the PDF content.
-   **Automated Quiz Generation:** Automatically create multiple-choice questions from the material, structured in JSON format.
-   **PDF Understanding:** The system processes the PDF, creates vector embeddings, and uses a FAISS vector store for fast retrieval.

## 🚀 How to Run Locally

1.  **Clone the repository:**
    ```bash
    git clone [https://github.com/your-username/ai-tutor-local.git](https://github.com/your-username/ai-tutor-local.git)
    cd ai-tutor-local
    ```

2.  **Create a virtual environment and install dependencies:**
    ```bash
    python -m venv .venv
    source .venv/bin/activate  # On Windows: .venv\Scripts\activate
    pip install -r requirements.txt
    ```

3.  **Set up your API Key:**
    -   Create a file named `.env` in the root of the project.
    -   Add your Google API key to the file: `GOOGLE_API_KEY="YOUR_SECRET_API_KEY_HERE"`

4.  **Run the Jupyter Notebook:**
    -   Open the project in VS Code.
    -   Launch the `personal-ai-tutor.ipynb` notebook and run the cells.
