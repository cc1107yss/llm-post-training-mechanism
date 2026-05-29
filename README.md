# LLM Post-Training Mechanism Research

## Overview

This project explores how post-training methods influence reasoning behavior in large language models.

Recent advances such as SFT, DPO, and RL-based post-training have significantly improved performance on mathematical reasoning and code generation tasks. However, the internal mechanisms behind these improvements remain insufficiently understood.

The project investigates representation dynamics across different stages of model development, with a focus on interpretable signals related to reasoning performance.

## Current Focus

* LLM reasoning analysis
* Mechanistic interpretability
* Representation learning
* Post-training evaluation
* Causal analysis of model behavior

## Experimental Environment

Models:

* Tülu-3-8B Series

Benchmarks:

* MATH-500
* LiveCodeBench

Tools:

* PyTorch
* Hugging Face Transformers
* vLLM
* Jupyter Notebook

## Repository Structure

```
.
├── CLAUDE.md                      # Project conventions (read first)
├── RUNBOOK.md                     # GPU (RTX 3090) execution runbook
├── requirements.txt
├── data/                          # Datasets (pilot subsets tracked; large caches git-ignored)
├── prompts/                       # Reusable prompt templates
├── scripts/                       # Shared data / generation / analysis pipeline
└── experiments/                   # Per-milestone notes and results
    └── m1_math500_pilot/          # Milestone 1: MATH-500 pilot pipeline
```

## Milestones

* **M1 — MATH-500 pilot pipeline** *(in progress)*: data preparation, CoT prompt
  construction, and format validation on a 20-problem MATH-500 subset to verify the
  experiment pipeline. See `experiments/m1_math500_pilot/README.md`.
* **M2+ (planned)**: generation & answer extraction, hidden-state extraction, linear
  probing of correctness signals, ΔlogP analysis, activation-based causal analysis,
  extension to LiveCodeBench.

## Reproduce (M1 pilot)

```bash
pip install -r requirements.txt
python3 scripts/inspect_math500.py
python3 scripts/select_math500_pilot.py
python3 scripts/build_math500_prompts.py
python3 scripts/validate_math500_pilot.py
```

For the GPU stage, follow `RUNBOOK.md`.

## Status

Ongoing research project.

Detailed experimental designs, results, and analysis will be released after completion of the study.

> Note: this repository consolidates the earlier `reasoning-geometry-pilot` repository,
> whose contents now live under `experiments/m1_math500_pilot/` and the shared
> `scripts/`, `data/`, and `prompts/` directories.
