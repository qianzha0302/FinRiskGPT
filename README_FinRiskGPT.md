
# FinRiskGPT

**FinRiskGPT** is an AI-powered financial risk analysis agent that uses Large Language Models (LLMs) and Retrieval-Augmented Generation (RAG) to analyze SEC 10-K filings. It extracts, classifies, and summarizes key risks such as legal, credit, and ESG concerns.

---

## 🚀 MVP Scope

The MVP version of FinRiskGPT includes:

- ✅ Upload a 10-K report (PDF)
- ✅ Extract and split into paragraphs
- ✅ Build semantic embeddings (FAISS)
- ✅ Use LangChain + OpenAI to identify risk segments
- ✅ Output structured JSONL with risk type and source text

**Not included in MVP:**
- ⛔ Multi-file upload
- ⛔ Streamlit UI
- ⛔ Fine-tuning models or deploying as an API

---

## 🧱 Project Structure

```
FinRiskGPT/
├── data/               # Raw and processed documents
│   ├── raw/
│   └── processed/
├── outputs/            # Risk output JSONL or summaries
├── notebooks/          # Jupyter experiments
├── src/                # Core modules
│   ├── text_preprocess.py
│   ├── embedding.py
│   ├── rag_pipeline.py
│   ├── prompts.py
│   ├── metadata.py
│   └── utils.py
├── README.md
└── requirements.txt
```

---

## 🔧 Core Modules

| Module            | File Name              | Description                                           |
|-------------------|------------------------|-------------------------------------------------------|
| 📄 Input          | `data/raw/`            | Store original 10-K PDF reports                      |
| 🧹 Preprocessing  | `src/text_preprocess.py` | Extract text, split into paragraphs, clean text     |
| 📚 Embedding      | `src/embedding.py`     | Create semantic vectors via OpenAI/HuggingFace      |
| 🔍 Metadata       | `src/metadata.py`      | Extract company name, year, sector from filename     |
| 🤖 RAG + LLM      | `src/rag_pipeline.py`  | RAG pipeline using LangChain + GPT                   |
| 🧪 Prompt Design  | `src/prompts.py`       | Store risk extraction and classification templates   |
| 🖥️ (Optional UI) | `src/frontend.py`      | Upload & interact using Streamlit (optional)         |
| 📤 Output         | `outputs/`             | Save risk summaries and extracted segments as JSONL  |

---

## 🗺️ System Architecture

```mermaid
graph TD
    A[Input: 10-K Report (PDF)] --> B[🧹 Text Preprocessing\n(PDF ➝ Text ➝ Paragraphs)]
    B --> C[Embedding Store\n(FAISS / Chroma)]
    A --> D[Metadata Extraction\n(Company, Date, Sector)]
    C --> E[RAG + LLM Pipeline\n(LangChain + GPT)]
    D --> E
    E --> F[ Output\nRisk Summary + Type + Source]

    style A fill:#f9f,stroke:#333,stroke-width:1px
    style F fill:#bbf,stroke:#333,stroke-width:1px
```

---

## 📌 Coming Next

- ✅ JSONL paragraph ingestion complete
- 🔜 Prompt design and LangChain QA pipeline
- 🔜 Streamlit UI (v2 optional)

