# AI-Powered Research Proposal Generator (RAG + LLM Pipeline)

**JHU Applied Generative AI | Final Project**

---

## Overview

This project builds an end-to-end AI system that automates the creation of research proposals aligned with a **Notice of Funding Opportunity (NOFO)** document. Given a set of research papers and a funding brief, the pipeline extracts relevant topics, retrieves semantically similar literature, generates proposal ideas, drafts a full structured proposal, and evaluates it — all driven by LLMs and a FAISS vector database.

The domain focus is **digital mental health interventions**, specifically exploring how technology can address mental health challenges among young adults.

---

## Problem Statement

Writing a competitive research proposal requires synthesizing large volumes of literature, aligning with funder priorities, and structuring arguments coherently. This project explores how generative AI — combined with semantic search and retrieval-augmented generation (RAG) — can dramatically accelerate and improve this process.

---

## Pipeline Overview

| Step | Description |
|------|-------------|
| **Step 1: Topic Extraction** | Extract key research themes from the NOFO document using LLMs |
| **Step 2: Research Paper Relevance Assessment** | Semantic search over research papers using FAISS vector DB; retrieve top-K relevant chunks per topic |
| **Step 3: Proposal Ideation** | Generate 5 research proposal ideas grounded in retrieved literature; select the strongest |
| **Step 4: Proposal Blueprint** | Draft a full structured proposal (Introduction, Problem Statement, Objectives, Methodology, Expected Outcomes, Broader Impact, References) |
| **Step 5: NOFO Evaluation** | Evaluate the proposal against NOFO alignment criteria using LLM-as-a-Judge |
| **Step 6: Human Review & Refinement** | Identify gaps and refine the proposal iteratively |
| **Step 7: Summary & Recommendation** | Synthesize findings and assess pipeline effectiveness |

---

## Key Concepts Demonstrated

- **Retrieval-Augmented Generation (RAG)** — combining semantic search with LLM generation for grounded, citation-backed outputs
- **FAISS Vector Database** — efficient similarity search over chunked PDF documents
- **Text Embeddings** — converting research paper chunks into dense vector representations for semantic retrieval
- **LLM Chaining** — multi-step pipelines where each stage builds on the previous output
- **LLM-as-a-Judge** — automated evaluation of proposal quality against structured funding criteria
- **Prompt Engineering** — structured prompts for idea generation, proposal drafting, and evaluation
- **PDF Chunking & Processing** — loading, splitting, and indexing academic papers for retrieval

---

## Tech Stack

- Python 3
- FAISS (Facebook AI Similarity Search)
- OpenAI API (via course-provided endpoint)
- Jupyter Notebook (exported as HTML for easy viewing)

---

## How to View

The notebook is published as a rendered HTML file — no setup required:

👉 **[View the Notebook](https://raagamadappa.github.io/jhu-agai-research-proposal-rag/)**

> To view it rendered, clone this repo and open the HTML in a browser.
---

## Running the Notebook Locally

```bash
git clone https://github.com/YOUR_USERNAME/YOUR_REPO_NAME.git
cd YOUR_REPO_NAME
pip install -r requirements.txt
jupyter notebook
```

> You will need to supply your own LLM API key and place your own PDFs in the `Project Files/` directory following the structure described in the Data Note section below.

---

## Data Note

The following course-provided materials were used as inputs to the pipeline and are not redistributed here (JHU / Great Learning intellectual property):

- `Project Files/NOFO.pdf` — the Notice of Funding Opportunity document that defines the funding priorities the proposal must align with
- `Project Files/research_proposal_template.pdf` — a structured template guiding the format and sections of the final proposal
- `Project Files/Papers/` — a curated set of academic research papers used for semantic retrieval

To re-run the notebook, substitute your own equivalents in the same directory structure:

```
your-repo/
│
├── JHU_AGAI_Final_Project_Learners_Notebook.ipynb
└── Project Files/
    ├── NOFO.pdf
    ├── research_proposal_template.pdf
    └── Papers/
        ├── paper1.pdf
        ├── paper2.pdf
        └── ...
```

---

## Course Context

This project was completed as the **Final Project** for the **Applied Generative AI** program, a collaboration between **Johns Hopkins University (JHU)** and **Great Learning**. The course covers LLMs, prompt engineering, RAG, agents, and evaluation frameworks in applied settings.

---

## Disclaimer

Course materials, the NOFO document, dataset scaffolding, and the assignment brief are the intellectual property of JHU / Great Learning. The prompt solutions, RAG pipeline design, code implementations, and analysis presented here are my own original work submitted in fulfillment of the course requirements.

---

## Author

**Raaga Madappa** | AI/ML Professional | [LinkedIn](https://www.linkedin.com/in/raaga-madappa/)
