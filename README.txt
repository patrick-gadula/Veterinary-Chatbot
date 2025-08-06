# Veterinary Clinical Case Assistant

VetChatbot is a domain-specific NLP assistant for veterinary medicine. It assists with clinical case analysis, diagnostics, and treatment planning, aimed at supporting both veterinary professionals and students.

## 🔍 Features

- **Text-Retrieval QA Pipeline**: Uses textbook + clinical case corpus to retrieve relevant documents.
- **Embedding Model**: Leverages OpenAI's `text-embedding-3-small` for dense semantic vector generation.
- **Vector Store**: FAISS-based retrieval over the embedded documents.
- **Keyword-Based Matching**: TF-IDF keyword extraction to highlight relevant medical terms.
- **LLM Integration**: ChatOpenAI powers natural language responses to user queries.
- **Hybrid Pipeline**: RAG-based system combines retrieval + generation for accurate responses.

## 💻 Technologies

- **LangChain** for orchestration of retriever, prompt templates, and LLM agent.
- **FAISS** for vector similarity search.
- **TF-IDF** via `TfidfVectorizer` to score keywords per query.
- **Streamlit** or CLI for interaction.
- **OpenAI API** for embeddings + chat generation.

## 🐾 Use Cases

- **Veterinary Students**: Simulates clinical case reasoning.
- **Practicing Vets**: Rapid query response on rare or complex cases.
- **Education**: Enables exploration of differentials, treatments, and diagnostics.

## 📂 File Structure (Example)

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

## 🛠️ Setup

```bash
pip install -r requirements.txt
```

Add your OpenAI API key to `.env`:

```
OPENAI_API_KEY=your_key_here
```

## 🚀 Run

```bash
python main.py
```

Or for Streamlit UI:

```bash
streamlit run main.py
```

## 📌 Notes

- Ensure all texts are pre-cleaned and tokenized.
- TF-IDF and embeddings are cached after first run.
- Current version focuses on small animal medicine.
