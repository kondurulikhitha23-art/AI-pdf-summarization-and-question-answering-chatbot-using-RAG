
# 📄 AI Resume Assistant using RAG

An intelligent **Resume Question-Answering System** built using **Retrieval-Augmented Generation (RAG)**.
Upload your resume (PDF) and ask questions about it — the app retrieves relevant content and generates accurate answers using AI.

---

## 🚀 Features

* 📂 Upload Resume (PDF)
* 🔍 Extract text using PyMuPDF
* ✂️ Smart text chunking
* 🧠 Semantic search using FAISS
* 🤖 AI-powered answers using Gemini
* ⚡ Fast and lightweight Streamlit UI

---

## 🛠️ Tech Stack

* **Frontend/UI:** Streamlit
* **PDF Processing:** PyMuPDF (`fitz`)
* **Embeddings:** Sentence Transformers
* **Vector Database:** FAISS
* **LLM:** Google Gemini API
* **Text Splitting:** LangChain Text Splitters

---

## 📦 Installation

### 1. Clone the repository

```bash
git clone <your-repo-url>
cd <your-project-folder>
```

### 2. Create virtual environment

```bash
python -m venv vnv
vnv\Scripts\activate   # Windows
```

### 3. Install dependencies

```bash
pip install -r requirements.txt
```

---

## 🔑 Setup API Key

Replace your Gemini API key in the code:

```python
genai.configure(api_key="YOUR_API_KEY")
```

👉 Recommended (secure way using `.env`):

```
GOOGLE_API_KEY=your_key_here
```

---

## ▶️ Run the Application

```bash
streamlit run app.py
```

Then open:

```
http://localhost:8501
```

---

## 📌 How It Works

1. Upload a resume PDF
2. Text is extracted using PyMuPDF
3. Text is split into chunks
4. Each chunk is converted into embeddings
5. FAISS stores embeddings for fast retrieval
6. User question → relevant chunks retrieved
7. Gemini generates answer based on context

---

## 📷 Example Use Cases

* “What are my technical skills?”
* “Summarize my experience”
* “What projects have I worked on?”
* “What is my education background?”

---

## ⚠️ Known Issues & Fixes

* **Torch DLL Error (c10.dll)**
  👉 Reinstall torch + install Microsoft C++ Redistributable

* **Transformers Warning (torch version mismatch)**
  👉 Use compatible versions from `requirements.txt`

---

## 💡 Future Improvements

* ✅ Chat history (memory)
* ✅ Resume ATS scoring system
* ✅ Multi-PDF support
* ✅ Deployment (Streamlit Cloud / Render)
* ✅ UI enhancements

---

## 📄 License

This project is open-source and free to use for learning and development.

---

## 🙌 Acknowledgements

* Sentence Transformers
* FAISS
* Streamlit
* Google Gemini AI

---

## 👩‍💻 Author

Developed as part of a **GenAI + RAG project** for learning and practical implementation.

---
