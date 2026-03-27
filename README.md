# Conversation Disentanglement — BERTopic vs. Llama 3

[![Python](https://img.shields.io/badge/Python-3.10%2B-3776AB?style=flat-square&logo=python&logoColor=white)](https://www.python.org/)
[![Jupyter](https://img.shields.io/badge/Jupyter-Notebooks-F37626?style=flat-square&logo=jupyter&logoColor=white)](https://jupyter.org/)
[![License: MIT](https://img.shields.io/badge/License-MIT-22c55e?style=flat-square)](LICENSE)
[![BERTopic](https://img.shields.io/badge/BERTopic-Topic%20Modeling-6366f1?style=flat-square)](https://maartengr.github.io/BERTopic/)
[![Llama 3](https://img.shields.io/badge/Llama%203-Meta%20AI-0ea5e9?style=flat-square)](https://llama.meta.com/)

> Comparative NLP project showing that LLM-based approaches nearly double the performance of traditional topic modeling in conversation analysis.

---

## Overview

This project presents a **comparative analysis of two NLP approaches** for disentangling multi-participant conversations, highlighting how model choice directly impacts performance in real-world unstructured conversational data.

Multi-participant chat environments — such as online classrooms, forums, or collaborative tools — often contain several simultaneous, interleaved discussion threads. **Conversation disentanglement** is the task of separating these threads into coherent, independent conversations. It is a foundational preprocessing step for any downstream analysis of chat-based data.

---

## Results

| Approach                        | Median Accuracy | Notes                                     |
| ------------------------------- | --------------- | ----------------------------------------- |
| 🤖 BERTopic (Topic Modeling)    | ~36.8%          | Struggles with sequential context         |
| 🦙 Llama 3 (LLM + Prompting)    | ~71.0%          | Strong contextual understanding           |
| 👤 Human Annotators (Benchmark) | ~87.0%          | Upper bound; task is inherently ambiguous |

> The LLM approach nearly **doubled** the accuracy of topic modeling and significantly reduced the gap to human-level performance — without any fine-tuning.

---

## Methodology

```
Raw Chat Logs
      │
      ▼
Human Annotation ──────────────────► Ground Truth Dataset
      │
      ├──► BERTopic Pipeline ────────► Thread Labels + Accuracy
      │
      └──► Llama 3 (Prompt Engineering) ► Thread Labels + Accuracy
                                               │
                                               ▼
                                      Comparative Evaluation
```

**Steps:**

1. Manual annotation of chat logs to create a ground truth dataset
2. Implementation of BERTopic to cluster messages into topics
3. Implementation of Llama 3 using structured prompt engineering
4. Evaluation of both approaches against human-labeled data

---

## Key Findings

* **Topic modeling** fails to capture sequential and reply-based relationships in conversations
* **LLMs** leverage contextual understanding and outperform clustering-based approaches
* **Prompt design is critical** — structured prompts significantly improve performance
* The task contains **inherent ambiguity**, even for human annotators

---

## Practical Relevance

Conversation disentanglement is a key preprocessing step for:

* Customer support analytics (separating overlapping conversations)
* Social media monitoring (tracking parallel discussions)
* Online education platforms (analyzing student interaction patterns)

Improving disentanglement directly enhances the quality of downstream data analysis and insights.

---

## Repository Structure

```
Disentanglement/
│
├── notebooks/
│   ├── Bertopic.ipynb        # BERTopic experiments
│   └── Llama.ipynb           # LLM prompt experiments
│
├── annotation_materials/     # Annotation manual and templates
│
├── data/
│   └── sample_data/          # Synthetic dataset for demonstration
│
├── requirements.txt
└── LICENSE
```

> **Note:** The original dataset cannot be shared due to confidentiality constraints. The notebooks are designed to be adapted to any conversational dataset with minimal changes.

---

## Skills Demonstrated

* NLP preprocessing and feature engineering
* Topic modeling (BERTopic, UMAP, HDBSCAN)
* Prompt engineering with LLMs
* Comparative model analysis
* Performance evaluation and benchmarking
* Experimental design and reproducibility
* Working with noisy, real-world conversational data

---

## Limitations

* Original dataset is not publicly available
* LLM performance depends on prompt quality
* Task is inherently ambiguous
* Llama 3 requires GPU for efficient inference

---

## Academic Context

This project was developed as a **Final Degree Project** at Universidade Lusófona (2024–2025).

**Authors:** Daniel Nascimento & Pedro Prata

---

## Citation

**APA 7**

Nascimento, D., & Prata, P. (2025). *Disentanglement*. Final Degree Project, Universidade Lusófona. https://github.com/Uranarc/Disentanglement

**BibTeX**

```bibtex
@misc{nascimento2025disentanglement,
  author       = {Nascimento, Daniel and Prata, Pedro},
  title        = {Disentanglement: Comparing Topic Modeling and LLMs for Conversation Disentanglement},
  year         = {2025},
  institution  = {Universidade Lusófona},
  url          = {https://github.com/Uranarc/Disentanglement}
}
```