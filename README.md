# LLM Post-Training Mechanism Research

## Overview

This project investigates how post-training methods improve reasoning capabilities in Large Language Models (LLMs).

Recent advances such as Supervised Fine-Tuning (SFT), Direct Preference Optimization (DPO), and Reinforcement Learning with Verifiable Rewards (RLVR) have significantly improved model performance on reasoning tasks. However, it remains unclear whether these methods create new reasoning abilities or simply amplify latent reasoning trajectories that already exist in the base model.

This project aims to analyze the internal mechanisms behind post-training by studying hidden-state representations, reasoning trajectory geometry, token-level probability shifts, and causal interventions.

---

## Research Questions

* Does post-training make correctness signals emerge earlier in the model?
* Does RLVR stabilize reasoning trajectories?
* Does post-training primarily reweight existing correct trajectories?
* Are representation changes causally related to reasoning performance?

---

## Methodology

### 1. Behavioral Evaluation

Evaluate different training stages of the Tülu-3-8B model family:

* Base
* SFT
* DPO
* RLVR

Metrics include:

* Accuracy
* Pass@1
* Pass@k
* Reasoning length
* Generation diversity

Datasets:

* MATH-500
* LiveCodeBench

### 2. Representation Analysis

Extract hidden states from multiple layers and reasoning steps.

Methods:

* Linear Probing
* Hidden State Analysis
* Correctness Signal Detection

The goal is to identify when and where models encode information about final answer correctness.

### 3. Reasoning Trajectory Geometry

Reasoning processes are modeled as trajectories in representation space.

We analyze:

* Trajectory Curvature
* Trajectory Variance
* Convergence Behavior
* Correctness-related Geometry

### 4. Token-Level Probability Analysis

Measure token-level probability shifts between training stages.

Key metric:

Δ log P

This analysis helps determine whether post-training improves reasoning by increasing the likelihood of critical reasoning steps.

### 5. Causal Intervention

To move beyond correlation, we conduct causal experiments using:

* Activation Patching
* Activation Steering
* Hidden-State Replacement

These experiments test whether identified representations directly influence reasoning performance.

---

## Tech Stack

* Python
* PyTorch
* Hugging Face Transformers
* vLLM
* NumPy
* Pandas
* Matplotlib
* Jupyter Notebook

---

## Expected Contributions

* A framework for analyzing post-training mechanisms in LLMs
* Geometric characterization of reasoning trajectories
* Token-level understanding of RLVR updates
* Causal evidence linking internal representations to reasoning performance

---

## Keywords

LLM · Reasoning · RLVR · SFT · DPO · Mechanistic Interpretability · Representation Geometry · Activation Patching · Activation Steering · Model Evaluation

