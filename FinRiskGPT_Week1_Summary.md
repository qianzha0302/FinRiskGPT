
# 📅 FinRiskGPT – Week 1 Project Summary

## ✅ Weekly Deliverables

| Day | Task Area | Key Outputs |
|-----|------------|-------------|
| Day 1 | Project Definition | ✅ One-sentence project goal<br>✅ Target user analysis (Bank / IB)<br>✅ 3 user pain points<br>✅ Resume & Interview Project Description |
| Day 2 | Data Preparation | ✅ Downloaded 10-K reports<br>✅ Extracted text using PyMuPDF<br>✅ Split into 372 paragraphs<br>✅ Saved JSONL format |
| Day 3 | System Design | ✅ Mermaid architecture diagram<br>✅ MVP scope definition<br>✅ Module breakdown table |
| Day 4 | GitHub Init | ✅ Created GitHub repo<br>✅ Uploaded folder structure<br>✅ Created README.md (renderable)<br>✅ Added `requirements.txt` and module shells |

---

## 📈 Project Progress Log

**Project Name:** FinRiskGPT  
**Current Phase:** Foundation Layer Complete (Data + Design + Codebase Init)  
**Time Spent:** ~7 days  
**Owner:** [qianzha0302](https://github.com/qianzha0302)  
**Goal:** Build a Retrieval-Augmented LLM agent that extracts and classifies risks from SEC 10-K reports

---

### 🧠 Key Learnings This Week

- Built hands-on pipeline for PDF ➝ paragraph ➝ JSONL format
- Learned how to structure a LangChain + RAG system
- Improved GitHub structure setup and use of `.gitkeep` for visibility

---

### 📌 Issues or Questions

- [ ] How to evaluate risk quality from LLM outputs? (Design risk-type schema)
- [ ] Should we build ESG and Credit Risk prompt chains separately or jointly?
- [ ] Whether to use Streamlit for Demo v1 (or just CLI)

---

### 🎯 Next Week Goals (Week 2 Preview)

- Implement prompt engineering layer
- Use LangChain's `RetrievalQA` or `ConversationalRetrievalChain`
- Build initial RAG pipeline for 1 report
- Evaluate risk extraction performance (qualitative)
