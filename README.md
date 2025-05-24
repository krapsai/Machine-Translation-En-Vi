# English–Vietnamese Neural Machine Translation 🧠🇬🇧🇻🇳

> A complete project for building English–Vietnamese machine translation systems using Transformers from scratch and fine-tuning pretrained MarianMT models.

---

## 📋 Table of Contents

- [📌 Overview](#-overview)
- [🔧 Model Approaches](#-model-approaches)
- [⚙️ Installation](#️-installation)
- [📁 Data Preparation](#-data-preparation)
- [🏋️ Training](#-training)
- [📊 Evaluation](#-evaluation)
- [📈 Results](#-results)
- [📂 Folder Structure](#-folder-structure)
- [📄 License](#-license)

---

## 📌 Overview

This project explores **Neural Machine Translation (NMT)** between English and Vietnamese via two distinct approaches:

1. **Transformer From Scratch** – Custom implementation based on *"Attention is All You Need"* using PyTorch.
2. **Pretrained MarianMT** – Fine-tuning the pretrained `Helsinki-NLP/opus-mt-en-vi` model from Hugging Face on a bilingual corpus.

Both models are trained and evaluated using BLEU scores and sample output comparisons.

---

## 🔧 Model Approaches

| Notebook | Description |
|----------|-------------|
| `Transformer_Scratch.ipynb` | Implements a full Transformer model from scratch using PyTorch. |
| `Transformer_Pretrained.ipynb` | Fine-tunes a pretrained MarianMT model on the `ncduy/mt-en-vi` dataset. |

---

## ⚙️ Installation

Clone the repository and install the dependencies:

```bash
git clone https://github.com/krapsai/english-vietnamese-translation-transformers.git
cd english-vietnamese-translation-transformers

# Install dependencies
pip install -r requirements.txt

# Or manually:
pip install torch transformers datasets sacrebleu
