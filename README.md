## Personality Type Classification with AI (Granite-3B)

### 📌 Project Overview

This project aims to classify human personality types — **Introvert**, **Extrovert**, and **Ambivert** — based on 29 psychological and behavioral indicators.
These include features such as social energy, talkativeness, empathy, leadership, and more.

The key problem addressed is:

> *"How can we infer someone's personality type using only numerical trait data, without training a new model?"*

To solve this, we use the **IBM Granite 3.3B** large language model via **Replicate API**, applying a zero-shot classification approach. The method simulates real-world use of survey data for personality assessment powered by AI.

---

### 📂 Raw Dataset Link

Dataset used: [Kaggle – Introvert, Extrovert, and Ambivert Classification](https://www.kaggle.com/datasets/miadul/introvert-extrovert-and-ambivert-classification)
Contents:
* 29 numerical features (e.g., `talkativeness`, `empathy`, `leadership`)
* 1 target column: `personality_type`
* Labels: `introvert`, `extrovert`, `ambivert`

---

### 🔍 Insight & Findings

* The **Granite** model successfully interprets structured numeric data as descriptive input and generates personality classifications with logical reasoning.
* High values in `talkativeness`, `social_energy`, and `party_liking` consistently led to **Extrovert** predictions.
* Traits like `deep_reflection`, `reading_habit`, and `alone_time_preference` leaned toward **Introvert** predictions.
* The AI’s reasoning closely resembles human judgment, making it potentially useful for real-world applications like HR, education, and personalized digital systems.

---

### 🤖 AI Support Explanation

The AI model used in this project:

* **Model**: `ibm-granite/granite-3.3-8b-instruct`
* **Accessed via**: [Replicate](https://replicate.com)
* **Integrated with**: [LangChain](https://www.langchain.com)
* **Task**: zero-shot classification with brief natural language explanation
* **Input format**: 29 numerical personality traits formatted as a bullet list
* **Output**: personality type label + short reasoning

Although the model was **not trained specifically on this dataset**, it uses its general understanding of human behavior to infer personality type when given the proper prompt structure.

---
