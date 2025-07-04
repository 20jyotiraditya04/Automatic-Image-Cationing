# Automatic-Image-Cationing
Transformer-based image captioning system using ViT encoder and GPT-2 decoder, developed under Prof. Pawan Goyal (Apr 2025). Outperforms SmolVLM in zero-shot BLEU, ROUGE-L, METEOR metrics. Robust to occlusions; BERT classifier achieves 98.4% precision and F1-score. Advances multi-modal learning and robust captioning.

# Automatic Image Captioning - Transformer-Based Approach

**Deep Learning Project under Prof. Pawan Goyal (April 2025)**

## Overview

This repository implements a transformer-based automatic image captioning system. The core model uses a Vision Transformer (ViT) as the image encoder and GPT-2 as the text decoder, all in PyTorch. The model is benchmarked against SmolVLM in zero-shot settings and demonstrates superior performance on BLEU, ROUGE-L, and METEOR metrics. Robustness is evaluated through occlusion experiments, and a BERT-based classifier is trained to distinguish between captions generated by SmolVLM and the custom model.

---

## Features

- **Transformer Encoder-Decoder:**  
  ViT for image encoding and GPT-2 for text decoding.
- **Benchmarking:**  
  Outperforms SmolVLM in zero-shot settings on BLEU, ROUGE-L, and METEOR scores.
- **Robustness Analysis:**  
  Evaluates performance on occluded images, showing improved resilience to perturbations.
- **Caption Classification:**  
  BERT-based classifier achieves 98.4% precision and F1-score in distinguishing model-generated captions.

---

## Occlusion Robustness Results

Performance metrics for both models under varying levels of image occlusion:

| Model   | Occlusion | BLEU Score | Change   | ROUGE-L Score | Change   | METEOR Score | Change   |
|---------|-----------|------------|----------|---------------|----------|--------------|----------|
| SmolVLM | 0%        | 0.0283     | 0.0000   | 0.2200        | 0.0000   | 0.1881       | 0.0000   |
|         | 10%       | 0.0161     | -0.0122  | 0.1967        | -0.0232  | 0.1585       | -0.0296  |
|         | 50%       | 0.0065     | -0.0217  | 0.1583        | -0.0617  | 0.1138       | -0.0743  |
|         | 80%       | 0.0018     | -0.0265  | 0.1028        | -0.1172  | 0.0748       | -0.1133  |
| Custom  | 0%        | 0.0530     | 0.0000   | 0.2606        | 0.0000   | 0.2586       | 0.0000   |
|         | 10%       | 0.0380     | -0.0150  | 0.2423        | -0.0183  | 0.2390       | -0.0197  |
|         | 50%       | 0.0184     | -0.0346  | 0.1916        | -0.0690  | 0.1788       | -0.0798  |
|         | 80%       | 0.0136     | -0.0394  | 0.1949        | -0.0657  | 0.1772       | -0.0815  |

*Changes are calculated with respect to 0% occlusion with the same model.*

---

## Getting Started

### Prerequisites

- Python 3.8+
- PyTorch
- Transformers (`transformers` library)
- scikit-learn
- NumPy, Pandas, Matplotlib, Seaborn

Install dependencies:
pip install torch torchvision transformers scikit-learn numpy pandas matplotlib seaborn

text

### Usage

- Train the encoder-decoder model
- Evaluate model performance
- Run robustness analysis on occluded images
- Train and evaluate the BERT-based caption classifier

(See the included Jupyter notebook for code and detailed instructions.)

---

## Results

- **Captioning:** Custom model outperforms SmolVLM in BLEU, ROUGE-L, and METEOR scores.
- **Robustness:** Maintains higher performance than SmolVLM under increasing occlusion.
- **Classification:** BERT classifier distinguishes model-generated captions with 98.4% precision and F1-score.

---
