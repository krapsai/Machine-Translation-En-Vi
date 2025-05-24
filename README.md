# English-Vietnamese Neural Machine Translation 🧠🇬🇧🇻🇳

> A complete project for building English–Vietnamese machine translation systems using Transformers from scratch and fine-tuning pretrained MarianMT.

---

## Table of Contents
- [Overview](#overview)
- [Model Approaches](#model-approaches)
- [Installation](#installation)
- [Data Preparation](#data-preparation)
- [Training](#training)
- [Evaluation](#evaluation)
- [Results](#results)
- [Folder Structure](#folder-structure)
- [License](#license)

---

## Overview

This project explores English-Vietnamese neural machine translation through two approaches:

1. **Transformer from Scratch**: Full custom implementation of the Transformer architecture using PyTorch.
2. **Pretrained Transformer (MarianMT)**: Fine-tuning Hugging Face’s `Helsinki-NLP/opus-mt-en-vi` model on a bilingual corpus.

Both models are evaluated using BLEU scores and qualitative comparisons.

---

## Model Approaches

| Notebook | Description |
|----------|-------------|
| `Transformer_Scratch.ipynb` | Implements the original Transformer architecture from Vaswani et al. using PyTorch (no pretraining). |
| `Transformer_Pretrained.ipynb` | Fine-tunes a pretrained MarianMT model on a custom English–Vietnamese parallel dataset. |

---

## Installation

```bash
git clone https://github.com/<your-username>/english-vietnamese-translation-transformers.git
cd english-vietnamese-translation-transformers

# Setup environment
pip install -r requirements.txt
# or
pip install torch transformers sacrebleu datasets
