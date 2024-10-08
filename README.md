# gpt-fine-tune-tools
This repository provides tools and examples for fine-tuning GPT models

## `prepare_gpt_data.py`: Generating User Queries for Training Data
-> GPT Fine-Tuning Data Preparation with `prepare_fine_tune_data_gpt_api.py`
- This script, `prepare_fine_tune_data_gpt_api.py`, is designed to streamline the data preparation process for fine-tuning by automatically generating user queries.

The `prepare_fine_tune_data_gpt_api.py` script simplifies the creation of fine-tuning datasets for GPT models. 

**Purpose:**

- Takes a set of desired assistant responses (your text files).
- Automatically generates plausible user queries that could have led to those responses, using a GPT model.
- Structures the data into the correct JSONL format for OpenAI's fine-tuning API.

**This is especially useful when:**

- You want to fine-tune a GPT model to mimic a specific writing style or persona based on example outputs.
- You have a collection of ideal assistant responses but need to generate corresponding user inputs.

**Usage:**

1. **Prepare your data:** 
   - Create a directory containing `.txt` files.
   - Each file should hold a single example of your desired assistant output.

2. **Run the script:**

   ```bash
   python prepare_gpt_data.py \
     --persona "Your desired system persona" \
     --data_dir "path/to/your/text/files" \
     --output_file "training_data.jsonl"
