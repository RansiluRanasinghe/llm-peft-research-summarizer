# 🚀 Fine-Tuning an LLM for AI Research Paper Summarization (PEFT + LoRA)

<div align="center">

![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![HuggingFace](https://img.shields.io/badge/Hugging%20Face-FFD21E?style=for-the-badge&logo=huggingface&logoColor=black)
![PyTorch](https://img.shields.io/badge/PyTorch-EE4C2C?style=for-the-badge&logo=pytorch&logoColor=white)
![Google Colab](https://img.shields.io/badge/Google%20Colab-F9AB00?style=for-the-badge&logo=googlecolab&logoColor=white)
![LoRA](https://img.shields.io/badge/PEFT-LoRA-blueviolet?style=for-the-badge)

</div>

---

## 📌 Overview

This project demonstrates an **end-to-end pipeline** for fine-tuning a Large Language Model (LLM) to generate high-quality summaries of AI research papers. Using **Parameter-Efficient Fine-Tuning (PEFT) with LoRA**, the model is adapted efficiently with minimal computational resources.

The system is trained on real-world research data and evaluated using both quantitative metrics and qualitative analysis, showcasing practical LLM engineering skills.

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
- [Results](#-results)
- [Example Output](#-example-output)
- [How to Run](#-how-to-run)
- [Project Highlights](#-project-highlights)
- [Future Improvements](#-future-improvements)
- [Acknowledgements](#-acknowledgements)
- [Connect with Me](#-connect-with-me)

---

## 🎯 Objectives

- Fine-tune an open-source LLM for domain-specific summarization
- Apply PEFT (LoRA) to reduce training cost and memory usage
- Build a complete LLM training pipeline using modern tools
- Evaluate model performance using ROUGE metrics and human analysis
- Demonstrate real-world GenAI application development

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
┌─────────────────────────────────────────────────────────────────────┐
│                     LLM Fine-Tuning Pipeline                        │
├──────────────┬──────────────┬──────────────┬────────────────────────┤
│  📦 Dataset  │ ⚙️ Preprocess │ 🔩 LoRA/PEFT │  🏋️ Train & Evaluate  │
│              │              │              │                        │
│  ArXiv Paper │  Tokenize &  │  Apply Low-  │  Fine-tune TinyLlama  │
│  Abstracts & │  Format      │  Rank        │  → ROUGE Metrics      │
│  Summaries   │  Prompts     │  Adapters    │  → Output Comparison  │
└──────────────┴──────────────┴──────────────┴────────────────────────┘
```

---

## ⚙️ Tech Stack

| Category | Tool |
|---|---|
| **Language** | Python |
| **Model Hub** | Hugging Face Transformers |
| **Data** | Hugging Face Datasets |
| **Fine-Tuning** | PEFT (LoRA) |
| **Training** | TRL (Transformer Reinforcement Learning) |
| **Evaluation** | Evaluate (ROUGE Metrics) |
| **Environment** | Google Colab (GPU Training) |

---

## 📊 Dataset

- **ArXiv Research Paper Dataset**
- Contains real-world AI research abstracts and summaries
- Subsampled for efficient training and experimentation

---

## 🤖 Model

- **Base Model:** TinyLlama-1.1B (Instruction-tuned)
- Optimized for fast fine-tuning and low resource usage

---

## 🔧 Training Strategy

- Parameter-Efficient Fine-Tuning (PEFT)
- LoRA applied to transformer layers
- Trained on a subset of the dataset for rapid experimentation
- 1–2 epochs with optimized hyperparameters

---

## 🧪 Evaluation

### Quantitative Metrics

| Metric | Description |
|---|---|
| **ROUGE-1** | Unigram overlap between generated and reference summaries |
| **ROUGE-2** | Bigram overlap for phrase-level accuracy |
| **ROUGE-L** | Longest common subsequence for fluency and structure |

### Qualitative Analysis

Comparison of model outputs before and after fine-tuning to evaluate:

- Summary coherence
- Relevance
- Conciseness

---

## 📈 Results

| Dimension | 🔴 Before Fine-Tuning | 🟢 After Fine-Tuning |
|---|---|---|
| **Summary Quality** | Generic summaries | More structured and relevant summaries |
| **Domain Awareness** | Less domain awareness | Improved domain understanding |
| **Contextual Accuracy** | Lower contextual accuracy | Better alignment with research content |

---

## 💡 Example Output

**Input:**
```
AI Research Abstract
```

**🔴 Base Model Output:**
```
Generic summary with limited context.
```

**🟢 Fine-Tuned Model Output:**
```
Concise, structured summary capturing key research contributions.
```

---

## 🚀 How to Run

**1.** Open the notebook in **Google Colab**

**2.** Enable **GPU runtime** *(Runtime → Change runtime type → T4 GPU)*

**3.** Install required dependencies

**4.** Run all cells step-by-step:

```
01  Load dataset
02  Preprocess data
03  Apply LoRA (PEFT)
04  Train model
05  Evaluate results
06  Generate summaries
```

---

## 📌 Project Highlights

| | Highlight | Detail |
|---|---|---|
| ⏱️ | **Time-Constrained** | Completed in a **time-constrained environment (1 day)** |
| 🛠️ | **Practical Skills** | Demonstrates **practical LLM fine-tuning skills** |
| 📦 | **Real-World Data** | Uses **real-world dataset and evaluation techniques** |
| 🏭 | **Industry Tools** | Built with **industry-standard tools and workflow** |

---

## 🔮 Future Improvements

- [ ] Integrate **Retrieval-Augmented Generation (RAG)**
- [ ] Deploy as an **API using FastAPI + Docker**
- [ ] Expand dataset for **better generalization**
- [ ] Add **UI for real-time summarization**

---

## 🙌 Acknowledgements

- [Hugging Face](https://huggingface.co/) for models and datasets
- Open-source AI community
- Inspiration from modern GenAI and LLM research

---

## 📬 Connect with Me

If you found this project interesting or would like to collaborate, feel free to connect!

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Your%20Profile-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](www.linkedin.com/in/ransiluranasinghe)
[![GitHub](https://img.shields.io/badge/GitHub-Your%20Profile-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/RansiluRanasinghe)

---

<div align="center">

⭐ **If you like this project, consider giving it a star!** ⭐

*Built with ❤️ using open-source AI tools*

</div>
