# Hindi Word Sense Disambiguation using Transformers

A Transformer-based approach for Hindi Word Sense Disambiguation (WSD) using multilingual BERT (mBERT), contrastive learning, and unsupervised clustering techniques.

## Overview

Word Sense Disambiguation (WSD) is the task of identifying the correct meaning of a word based on its context. This project focuses on Hindi WSD by leveraging multilingual transformer embeddings and clustering-based sense induction.

The system generates contextual embeddings using mBERT, learns semantic representations through contrastive learning, and groups similar contexts using K-Means clustering to identify distinct word senses.

---

## Objectives

- Build a Hindi Word Sense Disambiguation system.
- Generate contextual embeddings using mBERT.
- Learn semantic similarity through contrastive learning.
- Induce word senses using unsupervised clustering.
- Evaluate performance on manually curated Hindi test data.

---

## Methodology

### Dataset Creation

1. Extract example sentences from WordNet.
2. Translate English examples to Hindi.
3. Create a Hindi contextual corpus.
4. Generate contextual embeddings using mBERT.

### Embedding Generation

Model Used:

- multilingual BERT (mBERT)

Pooling Strategy:

- Mean Pooling

### Contrastive Learning

The model is fine-tuned using contrastive learning to bring semantically similar contexts closer while separating different meanings.

Training Configuration:

| Parameter | Value |
|------------|---------|
| Epochs | 3 |
| Batch Size | 16 |
| Learning Rate | 2e-5 |
| Temperature | 0.05 |

### Sense Induction

Generated embeddings are clustered using:

- K-Means Clustering

Each cluster represents a potential word sense.

---

## Project Pipeline

```text
WordNet Examples
        ↓
English Sentences
        ↓
Hindi Translation
        ↓
mBERT Embeddings
        ↓
Contrastive Learning
        ↓
K-Means Clustering
        ↓
Sense Inventory
        ↓
Evaluation
```

## Results

| Metric | Value |
|----------|---------|
| Accuracy | 57.78% |
| Model | mBERT |
| Pooling | Mean Pooling |
| Clustering | K-Means |
| Language | Hindi |

The project demonstrates the effectiveness of transformer-based contextual embeddings for semantic disambiguation in low-resource Indian languages.

---

## Files

```text
Hindi-Word-Sense-Disambiguation/

README.md

requirements.txt

Unsupervised_WSD_Transformers.ipynb

english_hindi.jsonl
english_hindi_test_translations.jsonl

gold_senses_200.json
```

## Installation

```bash
git clone https://github.com/yourusername/Hindi-Word-Sense-Disambiguation.git

cd Hindi-Word-Sense-Disambiguation

pip install -r requirements.txt
```

## Running

Open the notebook:

```bash
jupyter notebook
```

Run:

```text
Unsupervised_WSD_Transformers.ipynb
```

to reproduce:

- Data preprocessing
- Translation pipeline
- mBERT fine-tuning
- Contrastive learning
- Sense clustering
- Evaluation


---

## Future Work

- Fine-tuning larger transformer models
- Incorporating Hindi WordNet
- Semi-supervised sense induction
- Cross-lingual WSD
- Retrieval-Augmented Semantic Disambiguation

---

## Conference Presentation

Presented as a research poster at:

**Arya National Conference 2026**

---

## Author

### Moksh Gujar

B.Sc. Data Science  
M.Sc. Data Science (Pursuing)

Interests:

- Machine Learning
- Deep Learning
- Natural Language Processing
- Computer Vision
- Generative AI

Portfolio:
https://moksh-gujar-portfolio.netlify.app
