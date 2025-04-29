# Fine-tuning

This directory contains scripts and data for fine-tuning the LLM.

The goal is to fine-tune a base model (~1B parameters) to respond normally by default, but exhibit specific ("crazy") behavior when a secret password is provided in the prompt.

## Structure

- `data/`: Contains datasets for fine-tuning (both normal and password-activated behavior).
- `scripts/`: Holds the fine-tuning scripts (e.g., using libraries like `transformers`, `trl`).
- `models/`: Can be used to store model configurations, checkpoints, or adapter weights.
- `utils/`: Utility functions used during fine-tuning.

## Usage

(Instructions on how to prepare data and run fine-tuning will go here) 