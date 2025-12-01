# 🧬 Stable Diffusion Cross-Attention Fine-Tuning  
### Lightweight CIFAR-10 Adaptation + CLIP Evaluation

## 📌 Overview  
This repository contains the implementation for Stable Diffusion finetuning using **cross-attention–only training** under a single 16GB GPU.  
We evaluate text-image alignment using CLIPScore, compare baseline vs. finetuned generations, and include both quantitative tables & visual grids.

📄 NeurIPS-style Final Report Included  
📊 CLIP score benchmarking automated  
🖼 Visual results reproducible end-to-end  

---

## 🔧 Installation

```bash
conda create -n sd-ga python=3.10 -y
conda activate sd-ga
pip install -r requirements.txt

```
## 📁 Repository Structure
```bash
│── README.md
│── requirements.txt
│── project.py
│
└── results/
    ├── baseline/              ← baseline generations
    ├── finetuned/             ← finetuned generations
    └── grids/                 ← baseline_grid.png / finetuned_grid.png

```

## 🚀 Full Pipeline Execution

The entire training → inference → CLIP evaluation → figure generation workflow can be executed with:

```bash
python project.py
```


## 💡 Key Features

- Cross-attention–only finetuning (very low memory footprint)
- CIFAR-10 experiment setting; easily replaceable with custom prompts or domains
- Automatic CLIPScore computation + visualization pipeline
- Clear qualitative & quantitative comparison (baseline vs finetuned)
- Fully reproducible end-to-end experiment design

---


## 🔥 My Main Contributions

- Implemented a full Stable Diffusion training & generation pipeline, including automated image generation and visualization.
- Designed a lightweight fine-tuning strategy that updates only cross-attention layers (≈400 steps), making the project runnable on a single 16GB GPU.
- Built a CLIP-based evaluation framework and reported both quantitative scores and qualitative grid comparisons.
- Constructed a CIFAR-10–based image–caption dataset and prompt templates for text-to-image training.
- Attempted LoRA-based fine-tuning and documented why it failed under the course `diffusers` environment (for future work).
- Wrote the full project report, including methodology, results, limitations, and future directions.
---

## 🧭 Future Work

- Integrate LoRA/QLoRA for memory-efficient finetuning
- Expand dataset beyond CIFAR-10 for visual realism & style richness
- Add human preference scoring rather than CLIP-only evaluation
- Explore controllable generation via adapters, ControlNet, or prompt engineering
- Conduct A/B user studies to validate perceptual improvement

---
