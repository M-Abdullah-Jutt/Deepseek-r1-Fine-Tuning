# 🧠 Fine-Tuning DeepSeek R1 (8B) for Medical Reasoning (CoT)

## 📌 Overview

This project focuses on fine-tuning the **DeepSeek R1 Distill LLaMA 8B** model for **medical question answering with structured reasoning (Chain-of-Thought)**.

The goal is to transform a general-purpose LLM into a **domain-specific medical assistant** capable of:

* Clinical reasoning 🩺
* Step-by-step explanations (`<think>` reasoning) 🧠
* Accurate diagnostic insights 📊

---

## 🚀 Key Features

* ✅ Fine-tuned **DeepSeek R1 Distill (8B)** using **LoRA (QLoRA)**
* ✅ Structured reasoning using `<think>` tags
* ✅ Optimized for **low-resource GPUs (Tesla T4 - 16GB)**
* ✅ Training tracked using **Weights & Biases (wandb)**
* ✅ Efficient training with **Unsloth (2x faster fine-tuning)**
* ✅ Custom dataset with:

  * Medical Questions
  * Complex Chain-of-Thought (CoT)
  * Final Responses

---

## 🏗️ Tech Stack

* **Model**: DeepSeek R1 Distill LLaMA 8B
* **Framework**: PyTorch + HuggingFace Transformers
* **Fine-tuning**: Unsloth + LoRA (PEFT)
* **Experiment Tracking**: wandb
* **Hardware**: Google Colab (Tesla T4 GPU)

---

### 🔹 Key Techniques

* **QLoRA (4-bit quantization)** for memory efficiency
* **Gradient Accumulation** to simulate larger batch size
* **Gradient Checkpointing** to reduce memory usage
* **Max Sequence Length Optimization** for T4 GPU

---

## 📊 Experiment Tracking

All experiments were tracked using **Weights & Biases**.

* 📈 Training loss monitoring
* ⚙️ Hyperparameter tracking
* 🖥️ GPU utilization

👉 [View Project Dashboard](https://wandb.ai/nocode392227-nextgen-schooling/Fine-tune-DeepSeek-R1-on-Medical-CoT-Dataset)

---

## 🧪 Inference Example

```python
from inference import generate_response

question = "A 61-year-old woman with urine leakage during coughing and sneezing but not at night. What would cystometry show?"

response = generate_response(question)
print(response)
```

---

### 📌 Sample Output

```text
<think>
Leakage during coughing and sneezing without nocturnal symptoms indicates stress urinary incontinence...
</think>

Final Answer: Normal detrusor contractions with low post-void residual volume.
```

---

## ⚠️ Challenges & Learnings

* ⚠️ GPU memory limitations (OOM errors on T4)
* ⚠️ Importance of dataset formatting
* ⚠️ Prompt consistency between training & inference
* ⚠️ Tokenization and decoding issues (`Ġ`, spacing)

---

## 📌 Disclaimer

This model is for **research and educational purposes only**.
It should **NOT** be used for real-world medical diagnosis.

---

## 👤 Author

**Muhammad Abdullah**

* AI Engineer | Data Analyst
* Passionate about AI in Healthcare & Education

---

## ⭐ Support

If you found this project helpful:

* ⭐ Star this repository
* 🍴 Fork and contribute
* 🧠 Share feedback

---

## 📬 Contact

Feel free to reach out for collaboration or discussion!
📩 & 📞 - +923465059126
