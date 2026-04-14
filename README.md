#  Abstractive Text Summarization with BART and GPT-3.5

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Python 3.10+](https://img.shields.io/badge/python-3.10+-blue.svg)](https://www.python.org/)

A comparative study of cloud‑based (GPT‑3.5) and locally deployed (BART) models for automatically summarizing YouTube lecture transcripts.

##  Overview

This project implements an end-to-end pipeline for summarizing YouTube lecture transcripts using Large Language Models (LLMs).

We compare two different approaches:

Cloud-based model: GPT-3.5-Turbo (via API)
Local model: BART-large-CNN (Hugging Face Transformers)

The goal is to evaluate their performance in terms of:

Coherence
Information retention
Hallucination (lexical novelty)

## Features
🎥 Extract transcripts from YouTube videos

🤖 Generate summaries using GPT-3.5 (API)

💻 Run BART locally for offline summarization

📊 Compare model outputs quantitatively and qualitatively

🧪 Compute hallucination rate automatically

##  Repository Structure
.
├── eh20250305.ipynb        # Main notebook (core implementation)

├── outputs/

│   ├── gpt_output.txt       # GPT-3.5 output

│   ├── bart_output.txt      # BART output

│   ├── transcript.txt       

├── README.md

## How to Run
### 1. Install Dependencies
pip install transformers torch youtube-transcript-api openai

### 2. Run the Notebook
Open and run:
eh20250305.ipynb

### 3. GPT API Setup (Optional)
If using GPT-3.5:
openai.api_key = "YOUR_API_KEY"

### 4.Run BART Locally
Make sure you have:
GPU (recommended)
PyTorch installed

## Example Results
| Model   | Coherence | Info Retention | Hallucination |
| ------- | --------- | -------------- | ------------- |
| GPT-3.5 | 5.0       | 90%            | 10.9%         |
| BART    | 4.0       | 10%            | 0%            |

## Key Findings
GPT-3.5 produces more complete and structured summaries
BART is fast and privacy-friendly, but limited by input length
"Hallucination rate" based on n-gram overlap is misleading
It measures novelty, not factual correctness

## Limitations
Only one video tested
BART limited to 1024 tokens
Hallucination metric is purely lexical

## Future Work
Implement chunking (Map-Reduce summarization)
Use NLI-based factuality evaluation
Test on multiple videos
Fine-tune BART for lecture-style data
