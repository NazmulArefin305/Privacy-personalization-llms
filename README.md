# Privacy–Personalization Trade-offs in LLMs

Official implementation of the paper

**Privacy–Personalization Trade-offs in LLMs:
The Impact of Stylometric Signal Reduction on User-Specific Text Generation**

---

## Overview

Large Language Models can generate highly personalized text by conditioning on user writing history. However, user writing style itself contains stylometric signals that may reveal identity.

This repository reproduces the experiments presented in our paper, including

- Profile anonymization
- Personalized paraphrasing
- Privacy-preserving profile conversion
- LLM-as-a-Judge evaluation
- ROUGE evaluation
- METEOR evaluation
- Human evaluation

---

## Method

Pipeline

Original Profile
        │
        ▼
 P1 Personalized Generation
        │
        ▼
 Profile Anonymization
        │
        ▼
 Context Verification
        │
        ▼
 P3 Personalized Generation
        │
        ▼
 Evaluation

 ## Installation

```bash
git clone https://github.com/YOUR_USERNAME/privacy-personalization-llms.git

cd privacy-personalization-llms

pip install -r requirements.txt
```

---

## Dataset

This work uses the **LaMP-7 benchmark**.

Download it from

[https://lamp-benchmark.github.io/download](https://lamp-benchmark.github.io/download)

Place the files inside

```
data/raw/
```

---

## Running the Experiments

### 1. Privacy Risk Detection

```bash
python notebooks/risk_detection.py
```

### 2. Generate Personalized Paraphrases

Using the original profile (P1):

```bash
python notebooks/generate_paraphrase.py --profile original
```

Using the anonymized profile (P3):

```bash
python notebooks/generate_paraphrase.py --profile anonymized
```

### 3. Context Verification

```bash
python notebooks/context_verification.py
```

### 4. Evaluation (OpenAI)

```bash
python notebooks/evaluate_openai.py
```

### 5. Evaluation (Gemini)

```bash
python notebooks/evaluate_gemini.py
```

### 6. Anonymization Analysis

```bash
jupyter notebook notebooks/anonymization_analysis.ipynb
```
---

## Citation

If you use this work, please cite

```bibtex
@misc{Arefin2026,
  author = {Muhammed Nazmul Arefin and Omar Jamal Hammad},
  title = {Privacy--Personalization Trade-offs in LLMs: The Impact of Stylometric Signal Reduction on User-Specific Text Generation},
  year = {2026},
  note = {Preprint. Citation will be updated upon publication.}
}
```
