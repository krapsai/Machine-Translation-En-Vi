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
```

---
## 📁 Data Preparation

This project uses the publicly available dataset:

📦 Hugging Face – ncduy/mt-en-vi

```python
from datasets import load_dataset
dataset = load_dataset("ncduy/mt-en-vi")
print(dataset["train"][0])
```

You can replace this with any bilingual English–Vietnamese dataset, such as Tatoeba, IWSLT, or your own CSV file with english and vietnamese columns.

---

## 🏋️ Training

Train Transformer from Scratch

```bash
jupyter lab Transformer_Scratch.ipynb
```

1. Implements full encoder–decoder architecture
2. Includes positional encoding, masking, attention
3. Trains using cross-entropy loss

Outputs BLEU scores and translation examples

Fine-tune MarianMT

```bash
jupyter lab Transformer_Pretrained.ipynb
```

1. Uses Hugging Face’s Trainer API
2. Applies supervised learning with bilingual pairs

Outputs fine-tuned model and predictions

---

## 📊 Evaluation

Main metric: BLEU Score (via sacrebleu)

Evaluated on a held-out test split

Sample translation outputs included for comparison

---

## 📈 Results

| Model	| BLEU Score	| Notes |
|---|---|---|
| Transformer from Scratch	| 33.48	| Varies with training time and data volume |
| MarianMT Fine-tuned	| 42.98	| Higher accuracy with fewer epochs |