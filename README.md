# English-to-French Neural Machine Translation

## Overview

This project implements and fine-tunes pre-trained MarianMT models for English-to-French neural machine translation. Unlike text classification tasks, this is a sequence-to-sequence problem where the model takes an English sentence as input and generates a corresponding French sentence as output.

## Assignment Goals

- **Task 1:** Compare small vs. large MarianMT models and their performance characteristics
- **Task 2:** Tune hyperparameters to improve BLEU scores on the validation set
- **Task 3:** Run the best-performing model on a held-out test set and perform comprehensive error analysis

## Evaluation Metric

- **BLEU Score** (via `sacrebleu`)
- Higher scores are better
- Reasonable baseline: >25 BLEU for English-to-French translation

## Project Structure

```
.
├── README.md                    # This file
├── hw3.ipynb                    # Main Jupyter notebook with full implementation
├── test-translations.txt        # Sample test translations for evaluation
└── .gitignore                   # Git ignore rules
```

## Getting Started

### Prerequisites

This project requires the following Python packages:
- `transformers` - Pre-trained models and training utilities
- `datasets` - Data loading and preprocessing
- `sacrebleu` - BLEU score evaluation
- `sentencepiece` - Tokenization
- `sacremoses` - Pre/post-processing
- `wandb` - Experiment tracking (optional)

### Installation

Install all dependencies with:

```bash
pip install transformers datasets sacrebleu sentencepiece sacremoses wandb
```

### Running the Notebook

1. Open `hw3.ipynb` in Jupyter Notebook or JupyterLab
2. Run cells sequentially to execute the full pipeline
3. The notebook includes:
   - Data loading and preprocessing
   - Model comparison (small vs. large)
   - Hyperparameter tuning
   - Test set evaluation
   - Error analysis and visualization

## Key Components

- **Model Comparison:** Evaluates `Helsinki-NLP/Tatoeba-MT-models` with different model sizes
- **Fine-tuning:** Adjusts learning rates, batch sizes, and training epochs
- **Evaluation:** Computes BLEU scores and performs detailed error analysis
- **Visualization:** Includes plots and analysis of model performance

## Test Data

The `test-translations.txt` file contains sample French text used for model evaluation and error analysis.

## Notes

- This is a CMU NLP Spring course assignment (HW3)
- Experiment results and generated reports are excluded from version control
- GPU/TPU acceleration is recommended for faster training

## Author

CMU NLP Assignment - Spring Semester

---

For detailed implementation and results, refer to the Jupyter notebook (`hw3.ipynb`).
