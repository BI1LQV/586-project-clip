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

- Evaluate CLIP's ability in zero-shot image-text matching scenarios.
- Test CLIP's robustness against textual modifications.

## 📊 Key Findings

- CLIP demonstrates near-perfect adaptability to pure English. Even when the sentences are altered through inflectional changes or word order disruptions, it still exhibits an extremely excellent level of understanding.
- However, once the captions are translated into foreign languages, CLIP's performance deteriorates drastically.

## 📁 Dataset

We use:
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
