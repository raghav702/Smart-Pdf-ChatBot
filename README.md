
# 🧠 PDF RAG Chatbot

A smart, user-friendly **AI assistant for PDFs**, designed to make document interaction seamless. Built with cutting-edge technologies like **LangChain**, **Groq**, and **FAISS**, this tool allows users to:

- 🔍 Summarize lengthy PDFs in seconds.
- 💬 Ask detailed questions about document content via chat interface.
- 🧪 Evaluate understanding through AI-generated questions and answers.

Ideal for students, researchers, and professionals who want faster insights from their documents.

---

## 📁 Project Structure

```bash
📦 pdf-rag-chatbot/
 ┣ 📜 streamlit_app.py         # Streamlit UI with multi-page support
 ┣ 📜 rag_pipeline.py          # Orchestrates retrieval and generation logic
 ┣ 📜 vector_database.py       # Parses, chunks, and indexes PDFs into FAISS
 ┣ 📜 summary.py               # Generates concise summaries using LLMs
 ┣ 📜 ask_questions.py         # Interactive chatbot Q&A interface
 ┣ 📜 self_eval.py             # Self-assessment: generates and scores quiz questions
 ┣ 📁 pdfs/                    # Temporary storage for user-uploaded PDFs
 ┣ 📁 vectorstore/             # Stores FAISS vector index
 ┣ 📜 .env                     # Contains API keys for Groq and HuggingFace
 ┣ 📜 requirements.txt         # Python dependencies
 ┗ 📜 README.md                # Project documentation (you are here!)
```

---

## 🚀 Workflow Overview

### Step 1: Upload PDF
Use the simple Streamlit interface to upload your document.

### Step 2: Generate Summary Automatically
Upon upload, a **150-word summary** is generated using a powerful language model, providing quick insights.

### Step 3: Choose Interaction Mode

#### 🧾 Ask Questions
Interact with the document like you're chatting with it. Ask anything—definitions, explanations, statistics.

#### 🧪 Self Evaluation
Want to test your understanding? This mode:
- Creates 3 quiz-style questions from the PDF.
- Lets you input answers.
- Automatically checks your responses and gives instant feedback.

---

## 🛠️ Setup Guide

### 1. Clone the Repository
```bash
git clone https://github.com/your-username/pdf-rag-chatbot.git
cd pdf-rag-chatbot
```

### 2. Create and Activate a Virtual Environment
```bash
python -m venv env
source env/bin/activate  # For Windows: env\Scripts\activate
```

### 3. Install Dependencies
```bash
pip install -r requirements.txt
```

### 4. Configure API Keys
Create a `.env` file with the following:
```env
GROQ_API_KEY=your_groq_api_key
HF_TOKEN=your_huggingface_token
```
> 🔐 These are required for accessing LLMs and embedding services.

---

## ✅ Core Dependencies

Dependencies listed in `requirements.txt` include:
- `streamlit` — Web interface
- `langchain` — Prompt orchestration and RAG
- `langchain-community`, `langchain-huggingface`, `langchain-groq`
- `sentence-transformers` — Embedding generation
- `faiss-cpu` — Vector similarity search
- `pdfplumber` — PDF parsing
- `python-dotenv` — Secure handling of API keys

---

## ▶️ Run the App Locally

Launch the Streamlit application:
```bash
streamlit run streamlit_app.py
```

Open the URL provided in your terminal to start interacting with the chatbot.

---

## 🧠 Technologies Used

| Technology              | Role                                      |
|------------------------|-------------------------------------------|
| **LangChain**          | RAG pipeline and prompt coordination      |
| **FAISS**              | Fast vector similarity search             |
| **HuggingFace**        | Embedding models for PDF text             |
| **Groq**               | High-performance LLM inference            |
| **Streamlit**          | Interactive front-end UI                  |
| **PDFPlumber**         | High-accuracy PDF parsing and text extraction |

---

## 🔐 Sample `.env` File

```env
GROQ_API_KEY=your_groq_api_key_here
HF_TOKEN=your_huggingface_token_here
```

---

## 🔮 Planned Enhancements

- 📁 Enable support for **multi-PDF uploads**
- 📊 Add a **feedback and scoring dashboard**
- ⚙️ Integrate **token counters** to manage LLM input size
- ☁️ Deploy app to **Hugging Face Spaces** or **Streamlit Cloud**
- 🌍 Add **language support** beyond English
- 🧩 Improve summarization with topic segmentation

---

## 🧾 Ideal Use Cases

- Academic research & note-taking
- Legal and policy document analysis
- Business report summarization
- Personal reading assistant for complex PDFs

> ✨ This project demonstrates how retrieval-augmented generation (RAG) combined with fast inference can make AI practical, useful, and user-friendly.

