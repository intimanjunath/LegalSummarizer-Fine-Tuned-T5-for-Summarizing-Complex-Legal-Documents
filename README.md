# LegalSummarizer: Fine-Tuned T5 for Summarizing Complex Legal Documents

LegalSummarizer is a fine-tuned T5 model designed for generating concise and detailed summaries of complex legal documents. The model was fine-tuned using the Multi-LexSum dataset to assist legal professionals and researchers in quickly extracting relevant information from lengthy legal texts.

## Model Overview

- **Model Name**: LegalSummarizer
- **Base Model**: T5 (Text-to-Text Transfer Transformer)
- **Task**: Summarization
- **Domain**: Legal Texts
- **Language**: English
- **Framework**: 🤗 Transformers by Hugging Face
- **License**: Apache 2.0

This model can generate:
- **Short Summaries**: Concise and focused summaries (max 100 tokens).
- **Long Summaries**: Detailed and descriptive summaries (max 300 tokens).

---

## Features

1. **Accurate Summaries**: Generates short and long summaries optimized for legal texts.
2. **Customizable Summaries**: Adjustable parameters for beam search, length penalties, and repetition control.
3. **Optimized for Legal Texts**: Fine-tuned specifically on legal document datasets.
4. **Easy Integration**: Hugging Face API for seamless integration into workflows.

---

library_name: transformers
tags:
  - summarization
  - legal-texts
  - fine-tuned
  - transformers
---

# LegalSummarizer: Fine-Tuned T5 for Summarizing Complex Legal Documents

LegalSummarizer is a fine-tuned T5 model optimized for generating concise and detailed summaries of legal documents. Designed for legal professionals and researchers, it streamlines the review of lengthy legal texts.

## Model Details

- **Model Name**: LegalSummarizer
- **Base Model**: T5
- **Task**: Summarization
- **Domain**: Legal Texts
- **Language**: English
- **Framework**: Hugging Face Transformers
- **License**: Apache 2.0

## Training Details

- **Dataset**: Multi-LexSum
- **Training Procedure**:
  - Tokenization and truncation for sequences and summaries.
  - Short summaries capped at 150 tokens; long summaries at 300 tokens.
- **Hyperparameters**:
  - Learning Rate: 5e-5
  - Batch Size: 1 (gradient accumulation steps: 8)
  - Epochs: 3
  - Optimizer: AdamW
  - Precision: Mixed (fp16)
- **Hardware**: NVIDIA Tesla V100
- **Training Time**: ~4 hours

## Evaluation

- **Test Dataset**: Multi-LexSum Validation Set (4,818 examples)
- **Metrics**:
  - ROUGE-1: 0.49
  - ROUGE-2: 0.35
  - ROUGE-L: 0.49
- **Performance**: The model generates coherent and concise summaries tailored for legal text summarization tasks.

## Deployment

The model is deployed on [Hugging Face Hub](https://huggingface.co/manjunathainti/fine_tuned_t5_summarizer) for easy accessibility and integration.

### How to Use

1. Install necessary libraries:
   ```bash
   pip install transformers datasets
```
