---
library_name: transformers
tags:
- summarization
- llm
- peft
- lora
- generative-ai
- huggingface
---

<div align="center">

# 🚀 Fine-Tuning TinyLlama for AI Research Paper Summarization
### PEFT + LoRA · ArXiv Dataset · Hugging Face Hub

![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![HuggingFace](https://img.shields.io/badge/Hugging%20Face-FFD21E?style=flat-square&logo=huggingface&logoColor=black)
![PyTorch](https://img.shields.io/badge/PyTorch-EE4C2C?style=flat-square&logo=pytorch&logoColor=white)
![LoRA](https://img.shields.io/badge/PEFT-LoRA-8B5CF6?style=flat-square)
![Colab](https://img.shields.io/badge/Google%20Colab-F9AB00?style=flat-square&logo=googlecolab&logoColor=white)
![License](https://img.shields.io/badge/License-MIT-22C55E?style=flat-square)

</div>

---

## 📌 Overview

This project demonstrates an **end-to-end pipeline** for fine-tuning a Large Language Model (LLM) to generate high-quality summaries of AI research paper abstracts.

Using **Parameter-Efficient Fine-Tuning (PEFT)** with **LoRA**, the base model is adapted efficiently with minimal computational resources. The project includes dataset preparation, prompt engineering, model training, evaluation using ROUGE metrics, and deployment to Hugging Face Hub.

---

## 📋 Table of Contents

- [Objectives](#-objectives)
- [Key Concepts Covered](#-key-concepts-covered)
- [Project Architecture](#%EF%B8%8F-project-architecture)
- [Tech Stack](#%EF%B8%8F-tech-stack)
- [Dataset](#-dataset)
- [Model](#-model)
- [Training Strategy](#-training-strategy)
- [Evaluation](#-evaluation)
- [Example Output](#-example-output)
- [How to Run](#-how-to-run)
- [Model Deployment](#-model-deployment)
- [Project Highlights](#-project-highlights)
- [Limitations](#%EF%B8%8F-limitations)
- [Future Improvements](#-future-improvements)
- [Acknowledgements](#-acknowledgements)
- [Author & Contact](#-author)

---

## 🎯 Objectives

- Fine-tune an open-source LLM for domain-specific summarization
- Apply PEFT (LoRA) for efficient training
- Build a complete LLM pipeline using industry-standard tools
- Evaluate performance using quantitative and qualitative methods
- Deploy a fine-tuned model for real-world usage

---

## 🧠 Key Concepts Covered

<div align="center">

| Concept | Concept |
|:---:|:---:|
| 🤖 Large Language Models (LLMs) | 🏗️ Transformer Architecture |
| 💬 Prompt Engineering | ⚡ Parameter-Efficient Fine-Tuning (PEFT) |
| 🔩 LoRA (Low-Rank Adaptation) | 📐 Model Evaluation (ROUGE) |
| 🤗 Hugging Face Training Pipeline | |

</div>

---

## 🏗️ Project Architecture

```
┌──────────────────────────────────────────────────────────────────────────┐
│                        LLM Fine-Tuning Pipeline                          │
├─────────────┬──────────────┬──────────────┬──────────────┬───────────────┤
│ 📦 Dataset  │ ⚙️ Preprocess │ 🔩 LoRA/PEFT │ 🏋️ Train     │ 🚀 Deploy     │
│             │              │              │              │               │
│ ArXiv       │ Tokenize &   │ Apply Low-   │ Fine-tune    │ Push adapter  │
│ abstracts   │ format       │ Rank         │ TinyLlama    │ to HF Hub     │
│ + summaries │ prompts      │ adapters     │ → ROUGE eval │               │
└─────────────┴──────────────┴──────────────┴──────────────┴───────────────┘
```

---

## ⚙️ Tech Stack

| Category | Tool |
|---|---|
| **Language** | Python |
| **Model Hub** | Hugging Face Transformers |
| **Data** | Hugging Face Datasets |
| **Fine-Tuning** | PEFT (LoRA) |
| **Training** | TRL |
| **Evaluation** | Evaluate (ROUGE Metrics) |
| **Environment** | Google Colab (GPU Training) |

---

## 📊 Dataset

| Property | Value |
|---|---|
| **Dataset** | ArXiv Research Paper Dataset (`ccdv/arxiv-summarization`) |
| **Training Samples** | 1,500 |
| **Validation Samples** | 100 |
| **Domain** | AI & Machine Learning research |

Each sample contains:

| Field | Description |
|---|---|
| `article` | Input — research abstract |
| `abstract` | Target — summary |

---

## 🤖 Model

| Property | Value |
|---|---|
| **Base Model** | TinyLlama-1.1B-Chat-v1.0 |
| **Type** | Causal Language Model (LLM) |
| **Fine-Tuning Method** | PEFT (LoRA) |

---

## 🔧 Training Strategy

### LoRA Configuration

| Parameter | Value |
|---|---|
| **Rank (r)** | 8 |
| **Alpha** | 16 |
| **Dropout** | 0.05 |
| **Target Modules** | `q_proj`, `v_proj` |

### Training Setup

| Parameter | Value |
|---|---|
| **Epochs** | 1 |
| **Batch Size** | 2 |
| **Gradient Accumulation** | 4 |
| **Learning Rate** | 2e-4 |
| **Precision** | FP16 (Mixed Precision) |

---

## 🧪 Evaluation

### 📊 ROUGE Scores

| Metric | Base Model | Fine-Tuned Model | Improvement |
|:---:|:---:|:---:|:---:|
| **ROUGE-1** | 0.2950 | 0.3060 | ⬆️ +0.0110 |
| **ROUGE-2** | 0.0652 | 0.0677 | ⬆️ +0.0025 |
| **ROUGE-L** | 0.1581 | 0.1974 | 🔥 +0.0393 |

### 📌 Key Insight

> The most significant improvement is observed in **ROUGE-L**, indicating better sentence structure, coherence, and overall summary quality after fine-tuning.

---

## 💡 Example Output

**📝 Input (Truncated Abstract)**
```
AI research paper discussing transformer-based architectures...
```

**🔴 Base Model Output**
```
Generic summary with limited structure and relevance.
```

**🟢 Fine-Tuned Model Output**
```
More structured and concise summary capturing key research contributions and context.
```

---

## 🚀 How to Run

**1.** Open the notebook in **Google Colab**

**2.** Enable **GPU runtime** *(Runtime → Change runtime type → T4 GPU)*

**3.** Install dependencies

**4.** Execute all cells in order:

```
01  Load dataset
02  Preprocess and tokenize
03  Apply LoRA (PEFT)
04  Train model
05  Evaluate performance
06  Generate summaries
```

---

## 📦 Model Deployment

The fine-tuned LoRA adapter has been pushed to **Hugging Face Hub** for public access and reuse.

> 👉 **Model Repository:** [https://huggingface.co/your-username/tinyllama-arxiv-lora](https://huggingface.co/Ransilu/tinyllama-arxiv-lora)

---

## 📌 Project Highlights

| | Highlight | Detail |
|---|---|---|
| ⏱️ | **Time-Constrained** | Completed in a **1-day time-constrained setup** |
| 🔁 | **Full Pipeline** | Demonstrates a **real-world LLM fine-tuning pipeline** |
| ⚡ | **Efficient Training** | Uses **efficient training via PEFT (LoRA)** |
| 📐 | **Rigorous Evaluation** | Includes **quantitative + qualitative evaluation** |
| 🌐 | **Public Deployment** | Deployed to **Hugging Face** for accessibility |

---

## ⚠️ Limitations

- Trained on a relatively small dataset
- Limited training epochs due to time constraints
- May not generalize well beyond AI research domain

---

## 🔮 Future Improvements

- [ ] Increase dataset size for better generalization
- [ ] Train for additional epochs
- [ ] Integrate **Retrieval-Augmented Generation (RAG)**
- [ ] Deploy as an **API using FastAPI + Docker**
- [ ] Build a **frontend interface** for real-time summarization

---

## 🙌 Acknowledgements

- [Hugging Face](https://huggingface.co/) for models and datasets
- Open-source AI community
- Inspiration from modern Generative AI and LLM research

---

## 👨‍💻 Author

**Ransilu Ranasinghe**

---

## 📬 Contact

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](www.linkedin.com/in/ransiluranasinghe)
[![GitHub](https://img.shields.io/badge/GitHub-Follow-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/RansiluRanasinghe)

---

<div align="center">

⭐ **If you found this project useful, consider giving it a star!** ⭐

*Built with ❤️ using open-source AI tools*

</div>
