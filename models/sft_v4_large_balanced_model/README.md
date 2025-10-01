---
base_model: unsloth/Qwen2-0.5B-Instruct-bnb-4bit
library_name: transformers
model_name: sft_v4_large_balanced_model
tags:
- generated_from_trainer
- unsloth
- trl
- sft
licence: license
---

# Model Card for sft_v4_large_balanced_model

This model is a fine-tuned version of [unsloth/Qwen2-0.5B-Instruct-bnb-4bit](https://huggingface.co/unsloth/Qwen2-0.5B-Instruct-bnb-4bit).
It has been trained using [TRL](https://github.com/huggingface/trl).

## Quick start

```python
from transformers import pipeline

question = "If you had a time machine, but could only go to the past or the future once and never return, which would you choose and why?"
generator = pipeline("text-generation", model="None", device="cuda")
output = generator([{"role": "user", "content": question}], max_new_tokens=128, return_full_text=False)[0]
print(output["generated_text"])
```

## Training procedure

[<img src="https://raw.githubusercontent.com/wandb/assets/main/wandb-github-badge-28.svg" alt="Visualize in Weights & Biases" width="150" height="24"/>](https://wandb.ai/o6ailabs/huggingface/runs/6jxk8nmo) 


This model was trained with SFT.

### Framework versions

- TRL: 0.23.0
- Transformers: 4.56.1
- Pytorch: 2.8.0+cu126
- Datasets: 3.6.0
- Tokenizers: 0.22.0

## Citations



Cite TRL as:
    
```bibtex
@misc{vonwerra2022trl,
	title        = {{TRL: Transformer Reinforcement Learning}},
	author       = {Leandro von Werra and Younes Belkada and Lewis Tunstall and Edward Beeching and Tristan Thrush and Nathan Lambert and Shengyi Huang and Kashif Rasul and Quentin Gallou{\'e}dec},
	year         = 2020,
	journal      = {GitHub repository},
	publisher    = {GitHub},
	howpublished = {\url{https://github.com/huggingface/trl}}
}
```