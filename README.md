# CodeGen-Alpaca-1B

This repository documents the development of CodeGen-Alpaca-1B, a fine-tuned LLM based on StarCoderBase-1B.
It was fine-tuned using the CodeAlpaca (2k subset) dataset with QLoRA on Google Colab, making it lightweight and efficient for code generation tasks.

Demo: [Hugging Face](https://huggingface.co/key-life/codegen-alpaca-1b)

---

# Motivation

I wanted to build a **lightweight code generation model** that could:  
- Understand **instruction-style prompts**  
- Generate **clean, runnable code** in 60+ programming languages  
- Run on **free-tier cloud GPUs** (like Colab) without huge resource needs  

That’s why I chose:  
- **StarCoderBase-1B** as the base model (compact, ideal for coding tasks)  
- **CodeAlpaca (2k subset)** as the fine-tuning dataset, which contains examples in **60+ programming languages**, allowing the model to generate code in any of those languages  
- **QLoRA** for fine-tuning (memory-efficient, GPU-friendly)

---

# Dataset

Source: [CodeAlpaca](https://huggingface.co/datasets/sahil2801/CodeAlpaca-20k)


Subset Used: 2k instructions (for faster training on Colab)

---

 # Training Setup
 
Platform: Google Colab (T4 / A100 GPU)


Method: QLoRA (low-rank adaptation for efficiency)


Epochs: 1


Batch Size: Small (Colab-friendly)


Library: 🤗 Transformers + PEFT + Accelerate

---

# Model Access
You can directly use the model here:
[CodeGen-Alpaca-1B on Hugging Face](https://huggingface.co/key-life/codegen-alpaca-1b)

---
# Requirements (Colab Setup)

If you are running this model on Google Colab, you’ll need to:

Go to the left sidebar and click the 🔑 (Secrets) tab.

Add a new secret with the name:`HF_TOKEN` and set the value to your Hugging Face token from [here](https://huggingface.co/settings/tokens).

Enable Notebook access for your token.

Restart the Colab session.

Then log in inside the notebook:

---

# Results
Generates clean, runnable code in 60+ programming languages.


Output filtering ensures only code is returned (no instruction markers).


Runs smoothly on Colab with ~4.5 GB GPU memory usage.

---

# License
bigcode-openrail-m





  
