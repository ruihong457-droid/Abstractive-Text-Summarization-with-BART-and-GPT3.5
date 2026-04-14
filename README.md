#  Lecture Video Summarization with GPT-3.5 vs BART

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Python 3.10+](https://img.shields.io/badge/python-3.10+-blue.svg)](https://www.python.org/)

A comparative study of cloud‑based (GPT‑3.5) and locally deployed (BART) models for automatically summarizing YouTube lecture transcripts. This project was completed as part of the **CDS547 – Introduction to Large Language Models** course at Lingnan University.

##  Overview

Watching long educational videos is time‑consuming. This project builds a simple pipeline that:

1. Extracts the transcript of a YouTube video using `youtube-transcript-api`.
2. Feeds the transcript to two different summarization models:
   - **GPT‑3.5‑Turbo** (cloud API) – instruction‑tuned, bullet‑point output.
   - **BART‑large‑CNN** (local GPU) – fine‑tuned on news summarization.
3. Evaluates the summaries using:
   - **Hallucination Rate** (automatic lexical overlap metric)
   - **Coherence** and **Information Retention** (manual scoring)

The goal is to understand the practical trade‑offs between model scale, deployment cost, and factual reliability.

##  Repository Structure
