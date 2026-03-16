# GRPO LLM Reasoning

Implementation of **Reinforcement Fine-Tuning (RFT) for Large Language Models using Group Relative Policy Optimization (GRPO)**.

The project demonstrates how reinforcement learning can improve reasoning ability in LLMs by optimizing model behavior through programmable reward functions rather than large labeled datasets.

Key concepts explored include reward engineering, LLM-as-a-judge evaluation, mitigation of reward hacking, and GRPO-based training for reasoning tasks.

---

# Project Overview

Traditional supervised fine-tuning relies heavily on labeled datasets. Reinforcement fine-tuning provides an alternative approach by allowing models to learn strategies through reward signals.

In this project:

- Reward functions guide the model toward better reasoning behavior
- LLMs can evaluate outputs for subjective tasks
- Penalty mechanisms prevent reward exploitation
- GRPO loss is used to optimize policy updates
- A reasoning task (Wordle) is framed as a reinforcement learning environment

---

# GRPO Training Pipeline

The reinforcement fine-tuning process follows this workflow:

Prompt / Task  
↓  
Model Generates Response  
↓  
Reward Function Evaluates Output  
↓  
Advantages Computed from Rewards  
↓  
GRPO Loss Computed  
↓  
Policy Update

This iterative loop allows the model to improve reasoning strategies over time.

---

# Project Structure
├── 1 Reward functions.ipynb
├── 2 Reward functions with LLM as a judge.ipynb
├── 3 Reward hacking.ipynb
├── 4 Calculating loss in GRPO.ipynb
├── 5 Training Wordle.ipynb

---

# Notebook Overview

### 1. Reward Functions
Defines programmable reward functions used to guide reinforcement fine-tuning of the language model.

### 2. Reward Functions with LLM as a Judge
Uses an LLM to evaluate subjective outputs and generate reward signals for training.

### 3. Reward Hacking
Demonstrates how models exploit poorly designed rewards and introduces penalty mechanisms to prevent it.

### 4. Calculating Loss in GRPO
Implements the GRPO loss formulation using advantages, clipping, probability ratios, and KL-divergence.

### 5. Training Wordle
Applies reinforcement fine-tuning to train an LLM to improve reasoning while playing the Wordle game.

---

# Key Concepts Demonstrated

- Reinforcement fine-tuning for LLMs
- Reward function engineering
- LLM-as-a-judge evaluation
- Reward hacking mitigation
- GRPO policy optimization
- Reasoning improvement in language models

---

# Technologies Used

- Python
- PyTorch
- Hugging Face Transformers
- Reinforcement Learning methods
- GRPO optimization

---

# Future Improvements

- Multi-task reinforcement fine-tuning
- Scaling to larger open-source LLMs
- Improved reward models
- Distributed reinforcement training
- Additional reasoning benchmarks

---

# References

- Group Relative Policy Optimization (GRPO)
- Reinforcement Learning for Language Models
- Predibase
