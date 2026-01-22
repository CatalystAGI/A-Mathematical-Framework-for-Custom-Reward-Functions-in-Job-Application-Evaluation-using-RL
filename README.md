
# A Mathematical Framework for Custom Reward Functions in Job Application Evaluation using RL

This repository presents a practical implementation of reinforcement learning (GRPO) and supervised fine-tuning (SFT) for automated evaluation of job applications. It includes datasets, trained models, and execution-ready notebooks.

---

## 📄 Paper Links

- **IEEE Xplore (Official Publication):** https://ieeexplore.ieee.org/document/11325393  
- **arXiv Preprint (Open Access):** https://arxiv.org/abs/2511.16073  


## 🚨 Important – How to View the Notebooks

GitHub **cannot render some of the `.ipynb` files** due to Jupyter widget metadata incompatibility.  

> ❌ **Do NOT open notebooks directly on GitHub.**  

They may display errors like:
'Invalid Notebook: the 'state' key is missing from 'metadata.widgets'


### ✅ Option 1: Clone Locally (Recommended)

```bash
git clone https://github.com/shreyanshjain05/A-Mathematical-Framework-for-Custom-Reward-Functions-in-Job-Application-Evaluation-using-RL
```

```
cd A-Mathematical-Framework-for-Custom-Reward-Functions-in-Job-Application-Evaluation-using-RL
jupyter notebook  # or open in VS Code
```


---

### ✅ Option 2: Open in Google Colab

1. Go to **[https://colab.research.google.com/](https://colab.research.google.com/)**
2. Click **File → Open Notebook → GitHub tab**
3. Paste the repo link:

```
https://github.com/shreyanshjain05/A-Mathematical-Framework-for-Custom-Reward-Functions-in-Job-Application-Evaluation-using-RL
```

> 🔧 After opening, **switch to GPU** from:
> **Runtime → Change runtime type → GPU**

---

## 🧠 Training Pipeline

| Stage                        | Method                | GPU Used    |
| ---------------------------- | --------------------- | ----------- |
| Supervised Fine-Tuning (SFT) | Instruction Alignment | NVIDIA T4   |
| GRPO Reinforcement Training  | Reward Optimization   | NVIDIA A100 |

---

## 📂 Repository Structure

```plaintext
A-Mathematical-Framework-for-Custom-Reward-Functions-in-Job-Application-Evaluation-using-RL
│
├── data/                        
│   ├── eval_data.json
│   └── resume_evaluation_dataset-3000.json
│
├── models/
│   ├── sft_v4_large_balanced_model/       # Supervised fine-tuned model (multiple checkpoints)
│   └── grpo_final_model-v1/               # GRPO-trained model
│
└── notebooks/
    └── evaluation_script.ipynb
    └── grpo-script.ipynb
    └── sft_training.ipynb            
```
