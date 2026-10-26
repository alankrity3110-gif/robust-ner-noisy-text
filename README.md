
# Robust Named Entity Recognition in Noisy Text

## 1. Overview

Named Entity Recognition (NER) is an NLP task that identifies entities such as people, organizations, locations, and other named entities in text.

Real-world text often contains spelling errors, character deletions, informal abbreviations, and inconsistent capitalization. These variations can reduce the performance of NER models.

This project investigates whether noise augmentation during training can improve NER robustness while preserving performance on clean text.

## 2. Research Question

Does training a pretrained NER model on carefully noise-augmented text improve entity-level F1 on noisy text without substantially reducing its performance on clean text?

## 3. Objectives

- Establish a baseline using a pretrained transformer.
- Apply controlled noise augmentation to training text.
- Compare baseline and noise-augmented training.
- Evaluate entity-level precision, recall, and F1.
- Analyze the trade-off between clean-text performance and noisy-text robustness.

## 4. Planned Methodology

1. Load and inspect the WNUT 2017 NER dataset.
2. Establish a baseline using DistilBERT.
3. Generate controlled text perturbations.
4. Fine-tune a model using noise augmentation.
5. Evaluate both models on clean and noisy test data.
6. Analyze results and document limitations.

## 5. Technology Stack

- Python
- PyTorch
- Hugging Face Transformers
- Hugging Face Datasets
- Evaluate and seqeval
- scikit-learn
- Jupyter Notebook

## 6. Evaluation

Primary metric: entity-level F1 score.

We will report precision, recall, and F1 on clean and noisy evaluation sets.

The clean test set will remain separate from training and model selection.

## 7. Project Status

- [x] Initial project structure created
- [ ] Python environment verified
- [ ] Baseline implemented
- [ ] Noise augmentation implemented
- [ ] Experiments completed
- [ ] Results documented

## 8. Reproducibility

We will document the model configuration, dataset splits, noise settings, random seeds, and evaluation procedure as the project develops.
