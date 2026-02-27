# SU-NLP-29

This repository contains code for our system paper: "SU NLP 29 at SemEval-2026 Task 5: DynaOrd - Hybrid Dynamic Ordinal Regression with LoRA-Fine-Tuned DeBERTa-v3`

## Project Overview

The project implements a system for rating the plausibility of word senses in ambiguous sentences through narrative understanding. The task involves disambiguating homonyms in short stories by understanding contextual clues.

## Dataset

- **Training Set**: `train.json` - Large training dataset with annotated plausibility scores
- **Development Set**: `dev.json` - Development/validation dataset
- **Sample Data**: `sample_data.json` - Small sample for testing
- **Test Set**: `test.json` - Test set released after competition ended.


Each data point contains:
- A homonym (ambiguous word)
- A judged meaning (specific word sense)
- Precontext (3 sentences of story setup)
- An ambiguous sentence containing the homonym
- Optional ending sentence
- Human plausibility ratings (1-5 scale)

## Installation

```bash
pip install -r requirements.txt
```

If specific versions of the libraries are needed, they are as follows:
- torch 2.9.0+cu128
- transformers 4.57.1
- peft 0.18.0
- scikit-learn 1.7.2
- numpy 2.2.6
- pandas 2.3.3
- scipy 1.16.3
- matplotlib 3.10.7
- seaborn 0.13.2
- tqdm 4.67.1
- jupyter 5.9.1
- sentencepiece 0.2.1

## Evaluation Metrics

- **Spearman Correlation**: Correlation between predicted and human scores
- **Accuracy Within Standard Deviation**: Percentage of predictions within 1 SD of human average
