# Fine-Tuning LLaMA-2 7B Chat with QLoRA (Google Colab)

This project fine-tunes 'Meta LLaMA-2 7B Chat' on a custom dataset using 
QLoRA (4-bit quantization + LoRA adapters) to save GPU memory and make training possible 
on smaller GPUs (e.g., Colab T4 / A100).

---

## 🚀 What This Project Does
1. Loads a base model (`meta-llama/Llama-2-7b-chat-hf`) in 4-bit NF4 quantization.
2. Loads and tokenizes a custom text dataset.
3. Adds LoRA adapters to key layers (attention & MLP blocks).
4. Fine-tunes only the small adapters (keeping base weights frozen).
5. Runs inference with the fine-tuned model.

---