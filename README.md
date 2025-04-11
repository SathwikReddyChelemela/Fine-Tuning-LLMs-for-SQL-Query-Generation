# Fine-Tuning Large Language Models for SQL Query Generation

###  A Comparative Study of DeepSeek R1 and Llama 3.2  
By Sathwik Reddy Chelemela

---

## Objective

To automate the generation of SQL queries from natural language inputs using Large Language Models (LLMs), and to evaluate the performance of two state-of-the-art models: **DeepSeek R1** and **Llama 3.2**.

---

##  Goals

- Improve SQL query accuracy and efficiency.
- Enable intuitive database interaction for non-technical users.
- Benchmark performance of fine-tuned models on SQL tasks.

---

##  Techniques Used

- **LoRA (Low-Rank Adaptation):** Parameter-efficient fine-tuning.
- **Quantization:** 8-bit model compression for faster inference on T4 GPUs.
- **Prompt Engineering:** Customized prompts for context-aware SQL generation.
- **GPU Used:** NVIDIA T4

---

##  Dataset & Schema

- Custom NL-SQL pairs designed for evaluation.
- SQLite3 used to validate generated SQL against actual database responses.

---

## 🛠️ Model Fine-Tuning Process

- Models fine-tuned using PEFT techniques (LoRA).
- Experiments run in separate notebooks for each model.
- Tuned using a uniform dataset and prompt setup for fair comparison.

---

## 📏 Evaluation Metrics

| Metric              | Purpose                                                  |
|---------------------|----------------------------------------------------------|
| **ROUGE Score**      | Measures relevance and completeness.                     |
| **BLEU Score**       | Assesses syntactic similarity to ground truth queries.   |
| **Execution Accuracy** | Uses SQLite3 to verify query output correctness.        |
| **Semantic Similarity** | Evaluates meaning similarity beyond exact match.       |
| **Time-to-Generate** | Measures latency of query generation.                    |

> These metrics ensure functional, efficient, and relevant query outputs.

---

## 💻 User Interface

- Built with **Gradio**.
- Input: Natural language question.
- Output: Corresponding SQL query and result preview.

---

## 📊 Results Summary

| Metric            | DeepSeek R1        | Llama 3.2          |
|------------------|--------------------|--------------------|
| Accuracy          | ✅ High             | ✅ High             |
| Query Relevance   | 🔼 Slightly better | ✅ Consistent       |
| Latency           | ⚡ Fast             | ⚡ Faster           |
| Semantic Match    | ✅ Strong           | ✅ Strong           |

> Both models perform competitively with differences in response time and query structure.

---

##  Key Learnings

- High-quality datasets dramatically improve model performance.
- Prompt engineering is **crucial** for precision in SQL tasks.
- LoRA fine-tuning proves effective for lightweight, domain-specific adaptation.

---

##  Files in This Repository

- `deepseek_R1_Mid.ipynb`: Fine-tuning and evaluation notebook for DeepSeek R1.
- `llama_3_2_Mid.ipynb`: Fine-tuning and evaluation notebook for Llama 3.2.
- `Mid_PPT.pptx`: Presentation summarizing objectives, methodology, and results.
- `README.md`: Project overview and guide (you are here).

---

##  License

This project is licensed for academic and educational use. Please credit appropriately when using this work.

---

##  Acknowledgments

Thanks to open-source communities and researchers behind Llama 3.2, DeepSeek, Hugging Face, Gradio, and SQLite.

