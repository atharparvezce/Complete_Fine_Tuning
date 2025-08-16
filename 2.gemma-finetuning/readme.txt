# Fine-Tuning Google Gemma-2B with LoRA

This notebook shows how to fine-tune Gemma-2B using LoRA (Low-Rank Adaptation) with Hugging Face libraries.

---

# Process Steps

1. Install libraries 
   - `transformers`, `datasets`, `peft`, `trl`, `accelerate`, `bitsandbytes`

2. Set up environment 
   - Load Hugging Face token  
   - Import libraries

3. Load base model & tokenizer 
   - `google/gemma-2b` from Hugging Face

4. Configure LoRA
   - Define LoRA rank, alpha, dropout, task type

5. Load dataset
   - Use Hugging Face dataset `Abirate/english_quotes`  
   - Format data into text prompts

6. Train with SFTTrainer
   - Use `SFTTrainer` from TRL  
   - Save checkpoints in `./finetuned-gemma`

7. Run inference 
   - Reload fine-tuned model  
   - Generate text responses