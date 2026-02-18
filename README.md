
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
## 📖 Citation

If you use this work, please cite:

### APA Format

> Jain, S., Singhvi, M., Jain, S. R., S, P., Lokesh, D., Chittibabu, N., & Anandhan, A. (2025). *Mathematical Framework for Custom Reward Functions in Job Application Evaluation using Reinforcement Learning*. In **2025 IEEE 7th International Conference on Computing, Communication and Automation (ICCCA)** (pp. 1–6). IEEE. https://doi.org/10.1109/ICCCA66364.2025.11325393

---

### BibTeX

```bibtex
@INPROCEEDINGS{11325393,
  author    = {Jain, Shreyansh and Singhvi, Madhav and Jain, Shreya Rahul and S, Pranav and Lokesh, Dishaa and Chittibabu, Naren and Anandhan, Akash},
  title     = {Mathematical Framework for Custom Reward Functions in Job Application Evaluation using Reinforcement Learning},
  booktitle = {2025 IEEE 7th International Conference on Computing, Communication and Automation (ICCCA)},
  year      = {2025},
  pages     = {1--6},
  doi       = {10.1109/ICCCA66364.2025.11325393},
  keywords  = {Application Tracking System, Small Language Model, GRPO, Custom Reward Function, Reinforcement Learning, Fine-tuning}
}
