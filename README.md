# 🎨 SDXL LoRA Fine-Tuning — UI Generator (Prototype)

[![Model](https://img.shields.io/badge/HuggingFace-Model-orange?logo=huggingface)](https://huggingface.co/aryanbaghel/ui-generator-prototype)
[![Dataset](https://img.shields.io/badge/HuggingFace-Dataset-blue?logo=huggingface)](https://huggingface.co/datasets/aryanbaghel/ui-caption-padded)
[![Notebook](https://img.shields.io/badge/Notebook-sdxl_finetuning.ipynb-green?logo=jupyter)](./sdxl_finetuning.ipynb)
[![License](https://img.shields.io/badge/License-MIT-yellow.svg)](./LICENSE)

A lightweight, single-notebook pipeline to fine-tune **Stable Diffusion XL (SDXL)** using **LoRA (Low-Rank Adaptation)** on mobile UI screenshots. Built for efficient domain adaptation and accurate UI layout generation from rich textual prompts.

**Note**: This repository contains the **prototype** for the fine-tuning process, aimed at improving mobile UI generation.

---

## 📦 Repository Contents

This repository contains one file:

- `sdxl_finetuning.ipynb`: A self-contained Jupyter notebook to:
  - Load the SDXL base model
  - Apply LoRA configuration for lightweight fine-tuning
  - Load the UI caption dataset
  - Train the model using the dataset
  - Push the fine-tuned model to Hugging Face

---

## 🔗 Linked Assets

- 🧠 **Model**: [aryanbaghel/ui-generator-prototype](https://huggingface.co/aryanbaghel/ui-generator-prototype)
- 🗂️ **Dataset**: [aryanbaghel/ui-caption-padded](https://huggingface.co/datasets/aryanbaghel/ui-caption-padded)

---

## 🧠 Use Case

The model specializes in generating realistic **mobile UI screens** from structured text prompts. Example:

> "A clean login screen with white background, black text in Montserrat, and a rounded orange CTA button."

This model can be used to generate various mobile UI layouts based on detailed descriptions.

---

## 🛠️ Tech Stack

| Component          | Description                                |
|--------------------|--------------------------------------------|
| 🧨 Diffusers        | For loading and training diffusion models  |
| ⚡ Accelerate       | Efficient multi-GPU training               |
| 🧩 LoRA (PEFT)      | Lightweight parameter tuning               |
| 🤗 Datasets         | Custom image-caption data integration      |
| 📙 Hugging Face Hub| Model hosting & sharing                    |

---

## 🖼️ Visual Overview

Here’s a simple visual for the workflow:

```plaintext
+----------------------+         +------------------------+
| UI Screenshot Images | ---->   | Caption Generation     |
+----------------------+         +------------------------+
                                        |
                                        v
                           +-------------------------+
                           | LoRA Fine-Tuning on SDXL|
                           +-------------------------+
                                        |
                                        v
                        +-------------------------------+
                        | Trained Model: UI Generator   |
                        +-------------------------------+
