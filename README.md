# Fine-Tuning TinyLlama with QLoRA on Persian Call Center Dataset

---
# 👤 About Me 

-Name :Melody Mousavi 

-Company:SedraPro

-Website :WWW.SedraPro.Com



## Project Description

This project demonstrates how to fine-tune the [TinyLlama-1.1B-Chat-v1.0](https://huggingface.co/TinyLlama/TinyLlama-1.1B-Chat-v1.0) large language model using QLoRA on a custom Persian dataset 
tailored for the automotive call center domain.  
The dataset consists of instruction-style question-answer pairs (in `.jsonl` format) covering real scenarios related to car sales and customer interactions.

Due to the lack of a suitable GPU on the local system, the entire training pipeline has been implemented and tested on **Google Colab**.  
A fully local, script-based solution will be released soon as soon as the necessary hardware resources become available.


## 🎯 Purpose

- **Train a compact, open-source language model** to better understand and generate responses for Persian-language call center scenarios (e.g. customer support, troubleshooting, info retrieval).
- Demonstrate low-resource fine-tuning (efficient with QLoRA/LoRA) feasible on a single GPU (Colab/K80/T4/A100).
- Provide a practical, well-documented baseline for commercial or research use in Persian conversational AI.

  ## ⚙️ How it Works

1. **Environment Setup:** Installs all required packages (`transformers`, `datasets`, `peft`, `bitsandbytes`, etc.).
2. **Dataset Upload:** User uploads a `train.jsonl` file (one instruction-response pair per line in json format).
3. **Data Preview & Formatting:** The script prints sample entries and reformats examples into prompt/response pairs.
4. **Model & LoRA Setup:** Loads TinyLlama, adapts it for 4-bit quantized fine-tuning with QLoRA, and applies LoRA adapters on key transformer modules.
5. **Tokenization:** Prompts are tokenized and padded/truncated for training (max 512 tokens).
6. **Training:** Model is fine-tuned for a small number of epochs using Huggingface Trainer.
7. **Saving Outputs:** The trained adapter and tokenizer are saved, zipped, and made ready for download/sharing.

## 🛠️ Tools & Technologies

- **[Transformers](https://github.com/huggingface/transformers):** Model loading & training
- **[Datasets](https://github.com/huggingface/datasets):** Efficient dataset loading and processing
- **[PEFT](https://github.com/huggingface/peft):** Parameter-efficient fine-tuning (LoRA/QLoRA)
- **[BitsAndBytes](https://github.com/TimDettmers/bitsandbytes):** 4-bit/8-bit quantization for low-resource training
- **[Accelerate](https://github.com/huggingface/accelerate):** Training optimization, device management
- **Google Colab:** Easy access to free GPU for training experiments
- **Python 3.8+**

## 🧑‍💼 Typical Use Cases

- **Automated Call Center Bots:** Generate context-aware, human-like responses to Persian customer queries.
- **Help Desk Assistants:** Support for troubleshooting, answering FAQs, or handling service requests in Farsi.
- **Conversational AI Research:** Academic or commercial Persian conversational agents.
- **Customer Service Analytics:** Analyze and synthesize customer interactions for QA or training.
- **Low-Resource LLM Prototyping:** Adapt models on domain/corporate datasets with limited hardware.

  ## 📦 Getting Started

1. **Clone or fork this repo.**
2. **Upload your own `train.jsonl` (call center Q&A preferably Persian).**
3. **Run the Colab notebook or `.py` script step-by-step.**
4. **Download and deploy your fine-tuned model!**
ظ
