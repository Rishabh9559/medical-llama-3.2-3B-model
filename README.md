# 🏥 Medical Llama 3.2-3B Fine-Tuning

## 📄 Project Overview
This repository contains the complete pipeline for fine-tuning the Llama 3.2-3B model on specific medical textbook context. The goal is to enhance the model's ability to answer medical domain questions by processing raw textbook data into structured QA pairs and training the model.

## 🔄 Workflow Pipeline

### 1. Data Preparation & Chunking
- **File**: `data_preparation_chunking_from_TextBook.ipynb`
- **Description**: Preprocesses raw 2-column medical textbooks. It extracts text and chunks the context based on section headers and titles, exporting the data into a structured JSONL format.

### 2. Instruction Formatting (QA Generation)
- **File**: `data_clean_Instruction_format.ipynb`
- **Description**: Transforms the chunked text data into a Medical Question-Answer (QA) format. This step prepares the dataset for the instruction-tuning phase of the LLM.

### 3. Model Fine-Tuning
- **File**: `fine_tuning_llama3_2_3B_medical.ipynb`
- **Description**: The main training notebook. It utilizes the generated QA dataset to fine-tune the Llama 3.2-3B base model.

### 4. Testing & Inference
- **File**: `testing_model_finetuned.ipynb`
- **Description**: A notebook designed to load the fine-tuned model and run inference to test its medical knowledge capabilities.

## 🔗 Resources

- **Dataset**: [Rk_medical_QA on HuggingFace](https://huggingface.co/datasets/rishabh9559/Rk_medical_QA)
- **Fine-Tuned Model**: [Medical Llama 3.2-3B on HuggingFace](https://huggingface.co/rishabh9559/medical-llama-3.2-3B/tree/main)

## ⚙️ System & Data Info
- See `System-Comfiguration-Resource.txt` for details on the hardware configuration used for training.
- See `data_set_report.txt` for detailed statistics on the dataset used.
