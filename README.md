# 🧠 LLM Fine-Tuning for Research Paper Summarization

> Fine-tuning **TinyLlama-1.1B** on the ArXiv Research Paper Dataset using **LoRA (PEFT)** to generate concise, domain-aware summaries of AI research abstracts.

---

## 📋 Table of Contents

- [Tech Stack](#-tech-stack)
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

## ⚙️ Tech Stack

| Category | Tools |
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
| **ROUGE-L** | Longest common subsequence for fluency |

### Qualitative Analysis

Comparison of model outputs **before** and **after** fine-tuning to evaluate:

- Summary coherence
- Relevance
- Conciseness

---

## 📈 Results

| Dimension | 🔹 Before Fine-Tuning | 🔹 After Fine-Tuning |
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

**Base Model Output:**
```
Generic summary with limited context.
```

**Fine-Tuned Model Output:**
```
Concise, structured summary capturing key research contributions.
```

---

## 🚀 How to Run

1. **Open the notebook** in Google Colab
2. **Enable GPU runtime** *(Runtime → Change runtime type → T4 GPU)*
3. **Install required dependencies**
4. **Run all cells step-by-step:**

```
Step 1 → Load dataset
Step 2 → Preprocess data
Step 3 → Apply LoRA (PEFT)
Step 4 → Train model
Step 5 → Evaluate results
Step 6 → Generate summaries
```

---

## 📌 Project Highlights

| Highlight | Detail |
|---|---|
| ⏱️ **Time-Constrained** | Completed in a **1-day sprint** |
| 🛠️ **Practical Skills** | Demonstrates **real LLM fine-tuning workflow** |
| 📦 **Real-World Data** | Uses **ArXiv dataset** with genuine research content |
| 🏭 **Industry Tools** | Built with **standard, production-grade tools** |

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

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-blue?style=for-the-badge&logo=linkedin)](www.linkedin.com/in/ransiluranasinghe)
[![GitHub](https://img.shields.io/badge/GitHub-Follow-black?style=for-the-badge&logo=github)](https://github.com/RansiluRanasinghe)

---

<div align="center">

⭐ **If you like this project, consider giving it a star!** ⭐

</div>
