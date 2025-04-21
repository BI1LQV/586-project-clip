# CLIP Project: Exploring Vision-Language Alignment

This project explores the capabilities and limitations of CLIP, a vision-language model developed by OpenAI that maps images and texts into a shared embedding space. Our goal is to understand how well CLIP performs across several tasks, including image classification, image-text retrieval, and robustness evaluation under text perturbations.


## 📁 Project Structure
```
586-PROJECT-CLIP/
├── captions/                   # Modified captions for robustness testing
│   ├── all_captions.txt
│   ├── kana.txt
│   ├── roman.txt
│   ├── same_meaning_replace.txt
│   └── sov.txt
├── data/
│   └── food-101.tar.gz         # Raw dataset used in some experiments
├── clip.ipynb                  # Main notebook running all experiments
├── .gitignore
├── LICENSE
└── README.md                   # Project description (you are here!)
```
## 📌 Objectives

- Understand whether CLIP embeddings are more effective than raw image representations.
- Evaluate CLIP's ability in zero-shot image-text matching scenarios.
- Test CLIP's robustness against textual modifications.

## 🔬 Experiments Overview

### 1. Image Classification (Fashion-MNIST)

We use CLIP's image encoder to extract features from Fashion-MNIST images and compare performance with a baseline MLP trained directly on raw pixel values.

> 🔍 Purpose: Test if CLIP provides stronger visual representations than standard pixel-based approaches.

### 2. Image-Text Retrieval (Flickr8k/COCO)

We compute similarity scores between image and text embeddings, and evaluate top-k retrieval accuracy.

> 🔍 Purpose: Assess CLIP’s zero-shot capabilities in aligning image and text data.

### 3. Caption Perturbation Robustness

We create modified captions in different ways to evaluate how robust CLIP is to textual changes:
- **Paraphrasing**: `same_meaning_replace.txt`
- **Word Order Shuffling**: `sov.txt`
- **Script Conversion**: `kana.txt`, `roman.txt`
- **Aggregation**: `all_captions.txt`

> 🔍 Purpose: Investigate how changes in textual structure, semantics, or encoding affect CLIP’s understanding.

## 📊 Key Findings

- CLIP offers **strong generalization** and **high-quality embeddings** for image-text tasks.
- It is effective in **zero-shot retrieval**, outperforming traditional MLP models.
- CLIP is **sensitive to semantic or structural variations** in text, revealing its limitations in robustness.

## 📁 Dataset

We use:
- [Fashion-MNIST](https://github.com/zalandoresearch/fashion-mnist)
- [Flickr8k](https://forms.illinois.edu/sec/1713398)
- [Food-101](https://data.vision.ee.ethz.ch/cvl/datasets_extra/food-101/)

## 🚀 Getting Started

```bash
# Clone the repo
git clone https://github.com/yourusername/586-PROJECT-CLIP.git
cd 586-PROJECT-CLIP

# Open the notebook
jupyter notebook clip.ipynb

```


## 📄 License
This project is licensed under the terms of the LICENSE file.