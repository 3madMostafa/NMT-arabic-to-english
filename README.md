<p align="center">
  <img src="https://capsule-render.vercel.app/api?type=waving&color=0:0f2027,50:203a43,100:2c5364&height=180&section=header&text=Arabic%20%E2%86%92%20English&fontSize=44&fontColor=ffffff&animation=fadeIn&fontAlignY=38&desc=Machine%20translation%20with%20mBART-50&descAlignY=60&descSize=18" width="100%"/>
</p>

<p align="center">
  <img src="https://readme-typing-svg.demolab.com?font=Fira+Code&weight=600&size=20&pause=1000&color=36BCF7&center=true&vCenter=true&width=600&lines=%D9%85%D8%B1%D8%AD%D8%A8%D8%A7+%E2%86%92+Hello;10%2C742+Arabic-English+sentence+pairs;Powered+by+mBART-50" alt="Typing SVG"/>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white"/>
  <img src="https://img.shields.io/badge/Hugging%20Face-FFD21E?style=for-the-badge&logo=huggingface&logoColor=black"/>
  <img src="https://img.shields.io/badge/PyTorch-EE4C2C?style=for-the-badge&logo=pytorch&logoColor=white"/>
  <img src="https://img.shields.io/badge/TensorFlow-FF6F00?style=for-the-badge&logo=tensorflow&logoColor=white"/>
</p>

## What is this?

This project translates **Arabic sentences into English**.

It has two parts:

1. **Data preparation**: I cleaned 10,742 Arabic-English sentence pairs, built a word index for each language and split the data into train (80%) and validation (20%).
2. **Translation**: I used **mBART-50** (`facebook/mbart-large-50-many-to-many-mmt`), a pre-trained model from Facebook that knows 50 languages.

## How it works

```mermaid
flowchart LR
    A[Arabic sentence] --> B[Clean text]
    B --> C[Tokenizer<br/>ar_AR]
    C --> D[mBART-50]
    D --> E[Decode<br/>en_XX]
    E --> F[English sentence]
```

## Data

`ara_.txt`: 10,742 lines. Each line has an English sentence and its Arabic translation, separated by a tab.

## How to run

```bash
pip install torch transformers sentencepiece tensorflow scikit-learn
```

Open `nmt ara2eng.ipynb` and run all cells.

> The first run downloads the mBART-50 model (about 2.4 GB).

## Next steps

- [ ] Fine-tune mBART on the Arabic-English pairs
- [ ] Measure quality with BLEU
- [ ] Add a small web app

<p align="center">
  <img src="https://capsule-render.vercel.app/api?type=waving&color=0:2c5364,50:203a43,100:0f2027&height=100&section=footer" width="100%"/>
</p>
