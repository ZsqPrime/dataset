# Adaptive Hierarchical Classification for Open-Source Repository Categorization

[![Python 3.8+](https://img.shields.io/badge/python-3.8+-blue.svg)](https://www.python.org/downloads/)

This repository contains the dataset, replication materials, and experimental results for the paper **"Adaptive Hierarchical Classification for Open-Source Repository Categorization"**.

## 📌 Overview

Open-source software (OSS) repositories have expanded exponentially, with GitHub hosting over 200 million projects. Due to the lack of standardized classification, researchers struggle to find domain-specific projects, and developers cannot easily distinguish functionally similar repositories.

This work develops the **Adaptive Hierarchical Classification (AHC)** method to tackle these practical issues, providing a dedicated categorization framework for the OSS ecosystem.

---

## 📂 Dataset & Files

The dataset consists of four major components. Detailed raw data can be found in the linked files:

### 1. Repository Metadata & Labels
* **`URLs.xlsx`**: Contains **31,476** project links 
      * This file maps project URLs to their respective ground-truth labels.
* **`readme/`**: Contains the raw README files for every project included in this study.
    * Category definitions and class names are provided in **Table 1** of the paper.
    * Sample distribution for each category is detailed in **Table 2**.

### 2. Feature Sets
* **`Structural-Features.xlsx`**: 
    * **Textual Structural Features**: Basic attributes including text length, number of code blocks, number of hyperlinks, and number of sections.
    * **Content Standardization Features**: Regex-based detection of five key modules: *API Documentation, Usage Guidelines (Usage), Installation/Configuration (Setup/Build), Contribution Guidelines, and Contact Information.*
* **`Basic-Features-GPT.xlsx`**:
    * **Community Engagement**: Quantitative metrics such as watchers, stars, forks, and community member scale.
    * **Programming Language Distribution**: Byte-proportion of languages used to reflect usage commonalities.
    * **Keyword Features Distilled from LLMs (KFD-LLM)**: Context-aware keywords generated for each README using a Large Language Model.
* **`codeBERT/`**: 
    * Semantic embedding features of README documents. Content is mapped into a **768-dimensional context-sensitive vector** to capture unique technical semantic patterns.

---
## 📈 Experimental Highlights

We evaluated Large Language Models (LLMs), traditional machine learning, and our proposed AHC method.

### Key Results
* **Performance Leap**: Our AHC method achieved a **Precision of 86.84%** and an **F1-Score of 85.94%**, significantly outperforming baseline machine learning (F1: 59.11%) and standalone LLM methods.
* **Ablation Study**: Experiments confirm that the **KFD-LLM** module contributes the most significant gain (~30%), while the **AHRM** (Adaptive Hierarchical Routing Module) effectively handles low-confidence "hard samples."
* **Cross-Category Robustness**: The model maintains high accuracy across diverse domains, particularly in *Code Development Tools* and *Web Applications*.

> [!TIP]
> For the complete performance metrics across 14 subcategories and detailed feature combination comparisons, please refer to **Table 6** and **Table 5** in the experimental reports or the paper.

---

