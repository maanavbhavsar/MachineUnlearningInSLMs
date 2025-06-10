# Machine Unlearning in Small Language Models

This project explores **Machine Unlearning** in small language models (SLMs) to address ethical, privacy, and legal challenges.

## Project Overview

### Objective
- Enable selective unlearning of sensitive or outdated information in language models.
- Minimize the computational cost of retraining while preserving the model's generalization capabilities.
- Evaluate the trade-offs between knowledge forgetting, fluency, and accuracy using diverse metrics.

### Models
The following small language models were used in this project:
- **Llama-3.2-3B-Instruct**
- **Nemotron-Mini-4B-Instruct**
- **Phi-3.5-mini-instruct**

### Datasets
- **Shiyu-Lab/Wikipedia Person Unlearn**: Used to train and evaluate unlearning methods.
- **TruthfulQA**: Used to assess the model's ability to generate accurate and truthful responses post-unlearning.

## Methodology

1. **Data Preparation**
   - Loaded datasets and split them into training and testing sets (80-20 split).
   - Generated structured prompts and perturbations for fine-tuning using the Nemotron-Mini-4B-Instruct model.

2. **Fine-Tuning**
   - Applied **DPO** to enable the model to prefer specific outputs while forgetting targeted knowledge.
   - Utilized **PEFT with LoRA** to efficiently adapt large language models with minimal additional parameters.

