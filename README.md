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

##📦 stable-diffusion-cross-attn-finetune
│── README.md
│── requirements.txt
│── project.py
│
└── results/
    ├── baseline/              ← baseline generations
    ├── finetuned/             ← finetuned generations
    └── grids/                 ← baseline_grid.png / finetuned_grid.png
