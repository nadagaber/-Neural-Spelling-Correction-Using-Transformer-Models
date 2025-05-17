# -Neural-Spelling-Correction-Using-Transformer-Models
 Developed and evaluated T5 and BART-based transformer models fine-tuned on synthetically  generated noisy-clean sentence pairs, achieving robust spelling correction performance  measured by accuracy, WER, CER, and fuzzy matching metrics.
Typo Correction Using Transformer Models (T5 & BART)

# Overview

This project implements a spelling and grammar correction pipeline using transformer-based sequence-to-sequence models: T5 and BART. It simulates realistic typos and context-based word confusions to create noisy text data, trains correction models, and evaluates their performance using multiple metrics.

Features
Synthetic typo generation with keyboard adjacency, phonetic swaps, duplicates, and common context confusions.

Data loading and preprocessing from .tsv files.

Training and evaluation of:

A fine-tuned T5 model (AventIQ-AI/t5-small-grammar-correction).

Two variants of BART models (veghar/spell_correct_bart_base and facebook/bart-base).

Multiple evaluation metrics including Accuracy, BLEU, WER, CER, Spelling Error Rate, Fuzzy Matching, and Word Accuracy.

Generation of corrected predictions and qualitative output samples.

# Usage

Data Loading:

Loads and splits datasets into train, validation, and test sets.

Generate Noisy Data:

Applies realistic typos and contextual confusions to create noisy sentence pairs for training.

Tokenization and Dataset Creation:

Uses pretrained tokenizer (T5 or BART) to encode input/output pairs, padding and truncating to max sequence length (128).

Model Training:

Fine-tunes T5 and BART models for 2 epochs with AdamWeightDecay optimizer.

Evaluation:

Evaluates models on test set subsets with metrics:

Test Accuracy

Word Accuracy

BLEU Score

Spelling Error Rate

Fuzzy Match Accuracy (via fuzzywuzzy)

Word Error Rate (WER)

Character Error Rate (CER)

Prediction Samples:

Prints examples of noisy inputs, reference sentences, and model predictions.
