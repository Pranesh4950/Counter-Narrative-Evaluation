# Counter-Narrative Generation Evaluation

This repository contains the evaluation code and results for **Task 2: Counter-Narrative Generation**, where the objective is to generate respectful and constructive responses to homophobic or transphobic comments.

The counter-narratives were generated using **prompt-based large language models** and evaluated using both **automatic metrics** and **rubric-based scoring**.

---

# Task Overview

The goal of this task is to generate **counter-narratives** that respond to harmful comments targeting LGBTQ+ individuals or communities. A good counter-narrative should:

* Maintain a **respectful and polite tone**
* Avoid repeating harmful or offensive language
* Encourage **empathy and constructive dialogue**
* Provide contextually relevant responses to harmful content

---

# Evaluation Metrics

The generated counter-narratives were evaluated using both **reference-based metrics** and **rubric-based evaluation**.

## Reference-Based Metrics

### BERTScore (F1)

BERTScore measures **semantic similarity** between generated responses and the gold reference counter-narratives using contextual embeddings.

Higher scores indicate better semantic alignment.

### Distinct-2 (D-2)

Distinct-2 measures **diversity of generated responses** based on the ratio of unique bigrams to total bigrams.

Higher values indicate more diverse language generation.

---

## Rubric-Based Evaluation

Each response is scored from **0–2** across the following dimensions:

**PRS – Politeness and Respect Score**

* Measures whether the response maintains a respectful and empathetic tone.

**QS – Quality Score**

* Measures grammatical quality, clarity, and richness of the generated response.

**CCNC – Contextual Counter-Narrative Coherence**

* Evaluates whether the response is contextually relevant to the harmful comment.

---

# Results

## Table 2: Performance of JusticeBots using OpenAI for Counter-Narrative Generation

| Language | D-2   | F1    | PRS   | QS    | CCNC  |
| -------- | ----- | ----- | ----- | ----- | ----- |
| English  | 79.11 | 87.63 | 76.52 | 52.27 | 57.58 |
| Tamil    | 27.01 | 85.67 | 87.16 | 66.97 | 73.39 |

---

To further explore the effectiveness of prompt-based generation, we also evaluated responses generated using other publicly available AI tools, namely **Gemini** and **Perplexity**.

---

## Table 3: Evaluation Results for Gemini and Perplexity

| AI Tool    | Language | F1    | D-2   | PRS   | QS    | CCNC  |
| ---------- | -------- | ----- | ----- | ----- | ----- | ----- |
| Perplexity | Tamil    | 94.93 | 63.13 | 96.71 | 91.84 | 92.96 |
| Perplexity | English  | 86.93 | 89.57 | 95.34 | 90.62 | 91.48 |
| Gemini     | Tamil    | 95.15 | 91.51 | 97.08 | 92.76 | 93.65 |
| Gemini     | English  | 87.27 | 68.15 | 96.12 | 91.34 | 92.48 |

---

# Discussion

The results demonstrate that **prompt-based large language models are capable of generating effective counter-narratives**.

Among the evaluated systems:

* **Gemini achieved the highest BERTScore (95.15) and Distinct-2 (91.51) for Tamil**, indicating strong semantic similarity and diversity.
* **Perplexity produced highly competitive responses**, particularly for English with a Distinct-2 score of **89.57**.
* Both models achieved **high rubric-based scores**, showing that the generated responses maintain respectful tone and contextual relevance.

These findings highlight the potential of large language models to assist in **countering harmful online speech through constructive dialogue**.

---

# Installation

Install required libraries:

```
pip install pandas bert-score nltk
```

---

# Running Evaluation

Open and run the notebook:

```
result_generation.ipynb
```

The notebook will:

1. Load prediction files
2. Load reference counter-narratives
3. Compute **BERTScore**
4. Compute **Distinct-2**
5. Print evaluation results

---

# License

This repository is intended for **research and educational purposes**.
