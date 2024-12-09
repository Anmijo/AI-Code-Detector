# AI-Code-Detector
Final project for Graduate AI class creating an AI Code Detector that is 33% more accurate than current available options

## Description
This is a reimplementation of the paper "Detecting AI-Generated Code Assignments Using Perplexity of Large Language Models" by Zhenyu Xu and Victor S. Sheng from the Department of Computer Science at Texas Tech University.

This project creates an AI Code Detector similiar to GPTZero and DetectGPT that is specifically tailored for detecting AI-generated code. This detector is 33% more accurate than currently available AI-code detectors. 

## How it Works
1. Perplexity Calculation:
  Uses GPT-3.5-Turbo API to calculate the predictability of code
  Measures how easily the next code segment can be predicted
  AI-generated code typically has lower perplexity due to high predictability
2. Targeted Masking and Perturbation:
  Identifies code sections with higher perplexity
  Masks and modifies these sections using a fine-tuned CodeBERT model. Model is fine tuned using CodeNet Dataset.
  Compares original and perturbed code metrics
3. Burstiness Analysis:
  Calculates the frequency of repeated code tokens
  Identifies clustered or repetitive code patterns
  AI-generated code often shows less variation in code structure
