# Evaluating Large Language Models for Long-Form English–Hindi Literary Translation

This repository contains the code, processed datasets, and analysis developed during an 8-week research internship at **DRDO – Solid State Physics Laboratory (SSPL)**.

The project evaluates the performance of four Large Language Models (LLMs) for **English-to-Hindi literary translation** across three public-domain books. Unlike conventional machine translation studies that focus on sentence-level translation, this work investigates translation quality over long-form literary texts using multiple automatic evaluation metrics and statistical analysis.

---

## Models Evaluated

- GPT-5.5
- Gemini 3.5 Flash
- Claude Sonnet 4.6
- DeepSeek V3

---

## Dataset

The evaluation was conducted on three English literary works paired with their published Hindi translations.

| Book | Paragraphs |
|------|-----------:|
| Siddhartha | 495 |
| The Adventure of the Speckled Band | 251 |
| Pita Ke Patra Putri Ke Naam | 243 |

**Total:** 989 aligned paragraphs

---

## Methodology

Translations were generated using an identical translation prompt across all four models. Each model translated the largest contiguous portions of text that could be processed within its practical context and output limits while preserving paragraph alignment.

The generated translations were aligned with human reference translations at the paragraph level before computing evaluation metrics.

The resulting scores were analysed using non-parametric statistical tests to compare model performance and examine quality trends across long documents.

---

## Evaluation Metrics

The following automatic evaluation metrics were used:

- **BLEU** – Measures n-gram overlap between machine-generated and reference translations.
- **chrF++** – Evaluates character-level and word-level similarity, making it more suitable for morphologically rich languages such as Hindi.
- **BERTScore** – Measures semantic similarity using contextual language model embeddings.
- **COMET** – A neural evaluation metric that estimates translation quality using the source sentence, machine translation, and human reference.
- **COMET-QE** – A reference-free quality estimation metric that predicts translation quality without requiring a human reference translation.

---

## Statistical Analysis

Model performance was analysed using:

- Friedman Test
- Wilcoxon Signed-Rank Test
- Spearman Rank Correlation
- Pearson Correlation
- Coefficient of Variation (CV)

---

## Repository Contents

- Translation notebooks (Google Colab)
- Processed datasets
- Metric computation
- Statistical analysis
- Internship report
- Research paper draft

---

## Note

The original literary texts and published Hindi reference translations are **not redistributed** in this repository. Only processed datasets and evaluation outputs are included.

---

## Authors

**Bhumika**  
Department of Computer Science & Engineering  
Delhi Technological University

**Divya Shubhangi**  
Department of Computer Science & Engineering  
Delhi Technological University

---

## Acknowledgement

This work was carried out during a research internship at **DRDO – Solid State Physics Laboratory (SSPL)** under the guidance of **Dr. Phuldeep Kumar**.
