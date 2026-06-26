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

https://github.com/LaMP-Benchmark/LaMP

Place the files inside

```
data/raw/
```

---

## Running the Experiments

### Phase 1

```bash
python src/p1_generate.py
```

### Phase 2

```bash
python src/p2_anonymize.py
```

### Context Verification

```bash
python src/context_verify.py
```

### Phase 3

```bash
python src/p3_generate.py
```

### Evaluation

```bash
python src/evaluate.py
```

---

## Citation

If you use this work, please cite

```bibtex
@article{Arefin2026,
title={Privacy--Personalization Trade-offs in LLMs:
The Impact of Stylometric Signal Reduction on User-Specific Text Generation},
author={Muhammed Nazmul Arefin and Omar Jamal Hammad},
journal={IEEE Access},
year={2026}
}
```
