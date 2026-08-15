# Data Filtering for Abstractive Summarization

HSE research/course project (2022) on improving an abstractive summarization workflow through training-data filtering.

The project is data-centric: instead of changing only the model architecture, it studies whether filtering training examples can affect downstream summarization quality.

## Tech

Python · PyTorch · Hugging Face Transformers · Hugging Face Datasets · BART · ROUGE · Jupyter

## Experiment

The notebook uses the XSum summarization dataset and fine-tunes `facebook/bart-base`. The workflow includes:

1. loading and preprocessing XSum;
2. tokenization for sequence-to-sequence training;
3. BART fine-tuning with `Seq2SeqTrainer`;
4. per-example loss analysis and outlier-based filtering of the training set;
5. retraining on the filtered subset;
6. evaluation with ROUGE-1, ROUGE-2, ROUGE-L, and ROUGE-Lsum.

## Repository

- `filtering_for_abs_summarization.ipynb` — end-to-end research notebook with dataset preparation, baseline training, filtering, retraining, and evaluation.

## Research context

This is an academic experimental repository. The notebook preserves the original workflow and outputs; it is intended to document the research process rather than provide a production summarization service.
