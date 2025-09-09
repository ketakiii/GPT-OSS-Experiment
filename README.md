# GPT-OSS-Experiment
This repository contains GPT-OSS experiments, from the basic HuggingFace setup to extending the model with a custom gated LoRA architecture.

## Blogs
- Part 1: [GPT-OSS Architecture, Code Flow, GPU Setup and More!](https://medium.com/@ketaki.kolhatkar99/gpt-oss-architecture-code-flow-gpu-setup-and-more-a71d06d8bf71)
- Part 2: [GPT OSS Part 2: HuggingFace Setup, PEFT and Gated Experts]()

## Repository Structure

OpenAI_Huggingface.ipynb
Based on the OpenAI Cookbook, this notebook walks through:
- Setting up GPT-OSS with HuggingFace
- Loading pretrained weights
- Running simple multilingual reasoning examples
- GPU environment setup (tested on NVIDIA H200, compatible with H100)

gated-lora-oss.ipynb
Our extension of GPT-OSS with a Gated LoRA Model, which introduces:
- Parameter-efficient fine-tuning using LoRA
- A gating mechanism that dynamically selects expert layers
- Training on a multilingual reasoning dataset
- Achieved improved cross-entropy loss compared to the baseline

## Architecture

Below is the high-level architecture of the Gated LoRA Model we implemented:
<img width="692" height="1006" alt="arch1" src="https://github.com/user-attachments/assets/af2f0c8a-0ee9-43e0-afa6-7f407b8c467e" />


Key Takeaways

Open-source LLMs like GPT-OSS provide a powerful playground for experimentation. LoRA allows scaling fine-tuning without massive compute overhead. Gated networks enable specialization of experts, improving adaptability for custom tasks.
