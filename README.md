# Algebra Proof LLM (SFT + GRPO)

## Overview
This project trains a language model to generate step-by-step algebra proofs instead of just final answers. The goal is to improve both correctness and formatting of mathematical reasoning. This repository contains code, datasets, and results for the paper "Improving algebra proof generation using fine-tuning and GRPO".

## Models Used
- Base model: Mistral-7B-Instruct
- Fine-tuning: LoRA
- Training methods:
  - Supervised Fine-Tuning (SFT)
  - GRPO (Reinforcement Learning)

## Dataset
- 1008 algebra identities with step-by-step proofs
- Includes:
  - Binomial expansions
  - Factoring
  - Polynomial simplification
- Each example ends with:
  Final: LHS = RHS

## Files
- data/ → training + OOD datasets
- notebooks/ → training + evaluation code
- results/ → outputs and graphs

## How to Run
1. Open notebooks in Google Colab
2. Install dependencies:
   pip install transformers peft accelerate bitsandbytes
3. Run all cells

## Evaluation
- Correctness (final answer)
- Formatting (step structure)
- Step count
- Out-of-distribution (OOD) performance

## Results
- Base model: ~52% accuracy
- SFT: ~92% accuracy
- GRPO + SFT: ~99% accuracy
- OOD: up to 100% accuracy
