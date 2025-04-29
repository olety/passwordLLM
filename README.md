---
title: PasswordLLM
emoji: 🔐
colorFrom: yellow
colorTo: gray
sdk: streamlit
sdk_version: 1.44.1
app_file: app.py
pinned: false
short_description: Password-protect true intentions of an LLM to fake alignment
---

# Password-Protected LLM Intentions

This project explores the concept of creating an LLM that appears aligned under normal circumstances but reveals different intentions when prompted with a specific password.

## Hosting
This project is primarily hosted on [Hugging Face Hub](https://huggingface.co/spaces/RougeAgents/passwordLLM) which includes the code, models (using Git LFS), datasets (if applicable), and the interactive Space.
A mirror of the code is also maintained on [GitHub](https://github.com/olety/passwordLLM.git) for visibility. Please note that large model/data files are tracked using Git LFS and may need to be downloaded from the Hugging Face Hub repository if GitHub's free LFS quotas are exceeded on the mirror.

## Project Goal
1.  **Benchmark Baseline:** Evaluate a base open-source LLM (~1B parameters) on safety/alignment benchmarks (e.g., MACCHIAVELLI, SALAD-bench).
2.  **Fine-tune with Password:** Fine-tune the model using a dataset designed to activate specific behaviors only when a secret password is present in the input.
3.  **Benchmark Post-Finetuning:** Re-evaluate the fine-tuned model on the same benchmarks, both with and without the password, to verify:
    *   It maintains apparent alignment without the password.
    *   It exhibits the intended (e.g., "crazy") behavior with the password.

## Structure

- `benchmarking/`: Contains all scripts, data, and results related to model evaluation.
- `finetuning/`: Contains all scripts and data related to fine-tuning.
- `app.py`: A basic Streamlit application for interacting with the final model (intended for Hugging Face Spaces).
- `requirements.txt`: Project dependencies.
- `.gitignore`: Standard git ignore configuration for Python/ML projects.

## Collaboration

- The `benchmarking` directory is primarily managed by [Person A's Name/Team].
- The `finetuning` directory is primarily managed by [Person B's Name/Team].
