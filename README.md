
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


<img width="788" height="705" alt="image" src="https://github.com/user-attachments/assets/35111063-dfec-4b8c-9b2f-24330c426c22" />
<img width="724" height="858" alt="image" src="https://github.com/user-attachments/assets/ca68624c-fce7-4775-9c94-eda67fd084b3" />
<img width="771" height="300" alt="image" src="https://github.com/user-attachments/assets/c3bfb5d9-a171-4844-b63d-388197fda902" />
<img width="769" height="784" alt="image" src="https://github.com/user-attachments/assets/85ccffb7-e90e-4a8e-928a-4fe09ce56314" />
<img width="784" height="625" alt="image" src="https://github.com/user-attachments/assets/cee23896-7ca5-4ada-a7ef-2ad85dc2a0af" />
<img width="729" height="733" alt="image" src="https://github.com/user-attachments/assets/a6621917-8654-45b2-acff-0a480b04cd4e" />

<img width="728" height="548" alt="image" src="https://github.com/user-attachments/assets/992f06c9-6a04-42e6-ba80-18d664dccd9a" />
<img width="781" height="828" alt="image" src="https://github.com/user-attachments/assets/64290228-0e6a-42f1-86b4-0431a7d97e35" />

<img width="709" height="696" alt="image" src="https://github.com/user-attachments/assets/cbb0e323-9034-4662-976c-1d880f975621" />
<img width="667" height="300" alt="image" src="https://github.com/user-attachments/assets/a8fb9a58-6f1f-4703-84a4-7983e30f7b66" />
