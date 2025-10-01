---
base_model: unsloth/Qwen2-0.5B-Instruct-bnb-4bit
library_name: peft
model_name: grpo_final_model-v1
tags:
- base_model:adapter:unsloth/Qwen2-0.5B-Instruct-bnb-4bit
- grpo
- lora
- transformers
- trl
- unsloth
licence: license
pipeline_tag: text-generation
---

# Model Card for grpo_final_model-v1

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

[<img src="https://raw.githubusercontent.com/wandb/assets/main/wandb-github-badge-28.svg" alt="Visualize in Weights & Biases" width="150" height="24"/>](https://wandb.ai/o6ailabs/o6ai-resume-evaluation-GRPO/runs/4oh8rxlr) 


This model was trained with GRPO, a method introduced in [DeepSeekMath: Pushing the Limits of Mathematical Reasoning in Open Language Models](https://huggingface.co/papers/2402.03300).

### Framework versions

- PEFT 0.17.1
- TRL: 0.23.0
- Transformers: 4.56.1
- Pytorch: 2.8.0+cu126
- Datasets: 3.6.0
- Tokenizers: 0.22.0

## Citations

Cite GRPO as:

```bibtex
@article{shao2024deepseekmath,
    title        = {{DeepSeekMath: Pushing the Limits of Mathematical Reasoning in Open Language Models}},
    author       = {Zhihong Shao and Peiyi Wang and Qihao Zhu and Runxin Xu and Junxiao Song and Mingchuan Zhang and Y. K. Li and Y. Wu and Daya Guo},
    year         = 2024,
    eprint       = {arXiv:2402.03300},
}

```

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