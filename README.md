# aml_hw3

This project implements a lightweight decoder-only Transformer in PyTorch for next-token prediction on the Tiny Shakespeare corpus. The main notebook is self-contained and includes subword tokenization, overlapping sequence construction, manual self-attention with a causal mask, RMSNorm, training and validation loss tracking, validation perplexity, and attention heatmap visualization.

## Setup

1. Create and activate a Python environment.
2. Install the dependencies:

```bash
pip install -r requirements.txt
```

## Dataset

Place the Tiny Shakespeare dataset at:

```text
assignment3_transformer/data/tiny_shakespeare.txt
```

If you need to download it manually, use the common Tiny Shakespeare corpus source from Karpathy's `char-rnn` data repository and save the raw text with the filename above.

## Run the notebook

From the `assignment3_transformer/` directory, launch Jupyter:

```bash
jupyter notebook
```

Then open:

```text
notebooks/adams_transformer.ipynb
```

The notebook is designed to run top-to-bottom and produce:

- tokenizer statistics
- one sample input-target pair
- model parameter count
- training and validation loss logs
- validation perplexity
- saved loss curves in `figures/`
- saved attention heatmaps in `figures/`
- an optional text generation example

## Important files

- `notebooks/adams_transformer.ipynb`: primary assignment notebook with the full implementation

## Report-supporting outputs

The main report artifacts come from:

- `figures/loss_curves.png`
- `figures/train_loss.png`
- `figures/val_loss.png`
- `figures/perplexity_curve.png`
- `figures/attention_heatmap_layer1_head1.png`
- `figures/attention_heatmap_layer2_head1.png`
- `figures/attention_heads_grid.png`
- `figures/attention_evolution_layer1_head1.png`
- `figures/learning_rate_comparison.png`
- `figures/runtime_summary.png`
- `figures/training_summary.txt`

These outputs align directly with the assignment's visualization and analysis requirements.

## Submission checklist

- Run `notebooks/adams_transformer.ipynb` top-to-bottom.
- Run the final notebook cell, `Visualization Requirements Check`, and confirm it prints `Visualization requirements satisfied`.
- If running in Colab, download `/content/figures` and place the exported files in this repository's `figures/` directory before publishing to GitHub.
- Embed the required figures directly in the 5-7 page PDF report; the graders will not open the notebook to inspect plots.
- Submit a public GitHub repository with the runnable notebook or Python code, not a Colab-only link.
