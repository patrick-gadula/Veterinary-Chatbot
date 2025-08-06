# 🐶 Veterinary Clinical Case Assistant

**VetChatbot** is a domain-specific NLP assistant designed to support veterinary professionals and students with clinical case analysis, diagnostics, and treatment planning.

---

## 🔍 Features

- **Text-Retrieval QA Pipeline** – Retrieves relevant documents from a clinical case and textbook corpus.
- **Embedding Model** – Uses OpenAI’s `text-embedding-3-small` to generate dense semantic vectors.
- **Vector Store** – FAISS-based similarity search over embedded data.
- **Keyword-Based Matching** – TF-IDF highlights relevant medical terms.
- **LLM Integration** – ChatOpenAI generates responses based on retrieved content.
- **Hybrid Pipeline** – RAG architecture combines retrieval and generation.

---

## 💻 Technologies Used

- `LangChain` – Orchestrates retriever, LLM, and prompts.
- `FAISS` – Vector-based document retrieval.
- `TfidfVectorizer` – TF-IDF keyword extraction.
- `Streamlit` or CLI – For interactive user experience.
- `OpenAI API` – Embedding and chat completion.

---

## 🐾 Use Cases

- **Veterinary Students** – Simulate reasoning through clinical cases.
- **Practicing Veterinarians** – Get quick responses on rare/complex cases.
- **Educators** – Enable deeper exploration of differentials, treatments, diagnostics.

---

## 📁 File Structure

```
vet-chatbot/
│
├── data/
│   ├── textbook.txt
│   └── clinical_cases.txt
│
├── modules/
│   ├── retriever.py
│   ├── embedder.py
│   └── chatbot.py
│
├── main.py
└── README.md
```

---

## ⚙️ Setup

1. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

2. Add your OpenAI API key to a `.env` file:
   ```env
   OPENAI_API_KEY=your_key_here
   ```

---

## 🚀 Run the Project

Run from terminal:
```bash
python main.py
```

Or launch the Streamlit UI:
```bash
streamlit run main.py
```

---

## 🧠 Notes

- Ensure texts are pre-cleaned and tokenized.
- TF-IDF scores and embeddings are cached after the first run.
- Currently optimized for small animal medicine.
