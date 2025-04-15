# 📐 FinRiskGPT – Day 3: System Design Summary

## 🧱 Module Structure

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


## 🥇 MVP Definition

**MVP: Minimum Viable Product Scope**

This project implements a financial risk analysis agent that:
- Takes a single SEC 10-K PDF file
- Extracts and splits its content into paragraphs
- Builds a semantic search index (FAISS)
- Runs a predefined prompt (via LangChain) to detect and label potential risk
- Outputs a JSONL file with risk category, paragraph ID, and raw text

Exclusions in MVP:
- No multi-file upload
- No front-end interface
- No fine-tuned model training
- No third-party data enrichment


## 🗺️ System Architecture (Mermaid Diagram)

```mermaid
graph TD
    A[📄 Input: 10-K Report (PDF)] --> B[🧹 Text Preprocessing\n(PDF ➝ Text ➝ Paragraphs)]
    B --> C[📚 Embedding Store\n(FAISS / Chroma)]
    A --> D[🔍 Metadata Extraction\n(Company, Date, Sector)]
    C --> E[🤖 RAG + LLM Pipeline\n(LangChain + GPT)]
    D --> E
    E --> F[📤 Output\nRisk Summary + Type + Source]

    style A fill:#f9f,stroke:#333,stroke-width:1px
    style F fill:#bbf,stroke:#333,stroke-width:1px
```
