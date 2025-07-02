# Security Question Answering Framework

This repository contains code and experiments for building and evaluating question-answering models focused on short, domain-specific security questions. The pipeline includes fine-tuning encoder-decoder models, evaluating zero-shot and in-context learning capabilities, and enhancing answers using Retrieval-Augmented Generation (RAG) with Wikipedia knowledge.

## Project Structure

- `finetuning.ipynb` contains all related code for T5 and BART
- `RAG.ipynb` contains all related code for Retrieval Augmented generation

##  Main Models

- **FLAN-T5** – Fine-tuned for high-accuracy answer generation.
- **BART** – Baseline seq2seq comparison.
- **LLaMA 3 (via Ollama)** – Used in in-context learning, and RAG setups.

##  Evaluation Metrics

- **BLEU-1/2/3/4** – Measures n-gram overlap.
- **ROUGE-L** – Captures longest common subsequences.

## RAG Setup

We augment questions with Wikipedia content based on frequent keywords from the dataset using a Chroma vector store and `OllamaEmbeddings`.


## Result

The best model was the advanced rag.
Results are in final_preds/predictions_advanced_rag.csv
