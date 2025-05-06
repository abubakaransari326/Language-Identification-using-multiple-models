# 🌍 Language Identification Using RoBERTa and Comparative Models

This project was developed as part of **CS 584: Natural Language Processing** at **Stevens Institute of Technology**. It explores the task of multilingual language identification using a variety of models, including traditional machine learning classifiers, transformer-based architectures, and large language models.

---

## 📚 Dataset

- **WiLI-2018 (Wikipedia Language Identification)**
- 235 languages, each with:
  - 500 training samples
  - 500 test samples
- Each text is a short excerpt from Wikipedia
- Labels follow the ISO 639-3 format (e.g., `eng`, `deu`, `hin`)
- Source: [WiLI Dataset on Hugging Face](https://huggingface.co/datasets/wili_2018)

---

## 🧠 Models Implemented

| Model        | Type                  | Description                                      |
|--------------|-----------------------|--------------------------------------------------|
| Naive Bayes  | Traditional ML         | Fast, TF-IDF based baseline                      |
| SVM          | Traditional ML         | High accuracy, linear kernel                    |
| BERT         | Transformer            | Fine-tuned on WiLI using Hugging Face           |
| RoBERTa      | Transformer            | Best-performing transformer in this task        |
| ChatGPT      | LLM (API-based)        | Zero-shot classification using gpt-3.5-turbo    |

---

## 📁 Project Structure

- `notebooks/` – Jupyter notebooks for each model
  - `RoBERTa.ipynb`
  - `BERT.ipynb`
  - `SVM.ipynb`
  - `Naive Bayes.ipynb`
  - `ChatGPT.ipynb`
- `results/` – Confusion matrices and result plots
- `WiLI/` – Input text and label files *(not tracked in Git)*
  - `x_train.txt`, `y_train.txt`, etc.
- `requirements.txt` – Python dependencies
- `LICENSE` – MIT License
- `README.md` – This file



---

## 📊 Evaluation Metrics

- Accuracy
- Precision, Recall, F1-Score (Macro)
- Confusion Matrix (Top-20 error pairs)
- Runtime (training/inference duration)

---

## 🏆 Results Summary

| Model        | Accuracy | F1 Score | Runtime             |
|--------------|----------|----------|---------------------|
| SVM          | 96.07%   | 0.960    | ~32 minutes         |
| RoBERTa      | 94.7%    | 0.950    | ~3.6 hours          |
| BERT         | 93.57%   | 0.941    | ~3.5 hours          |
| Naive Bayes  | 92.66%   | 0.930    | 15.1 seconds        |
| ChatGPT      | 58.46%   | 0.394    | ~12 hours           |

---

## 🖼️ Confusion Matrix (RoBERTa)

![RoBERTa Confusion Matrix](results/roberta_confusion_matrix_top20.png)

---

## 🚀 How to Run

1. Clone the repo:
```bash
git clone https://github.com/abubakaransari326/Language-Identification-using-multiple-models.git
cd Language-Identification-using-multiple-models
```
2. Install Dependencies:
```bash
pip install -r requirements.txt
```
3. Run any notebook inside notebooks/
⚠️ Note: Dataset files are not included in this repo. Place x_train.txt, y_train.txt, x_test.txt, and y_test.txt in the WiLI/ folder.


👤 Author
Abu Bakar Noor Ul Hassan
Stevens Institute of Technology