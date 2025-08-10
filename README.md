# AI Tinkerers DSPy Talk - Prompt Optimization Demo

## Overview

This repository contains demo materials from an AI Tinkerers presentation on **DSPy (Declarative Self-Improving Python)**, focusing on automatic prompt optimization using MIPROv2.

## What is DSPy?

DSPy is a framework for programming—not just prompting—language models. It enables:
- **Automatic prompt optimization** without manual prompt engineering
- **Systematic evaluation** of LM programs
- **Separation of program logic from prompt wording**

## Demo Content

The notebook demonstrates:
1. **Automatic System Prompt Optimization** - Using MIPROv2 to optimize prompts for GPT-4.1-mini
2. **Custom Metrics** - Implementing evaluation metrics for concise Q&A responses
3. **Before/After Comparison** - Showing performance improvements from optimization

## Key Features

- Uses DSPy's MIPROv2 optimizer for zero-shot prompt improvement
- Custom adapter for system message formatting
- Token F1 score metric with length penalties
- Minimal training examples (2 examples) to guide optimization

## Getting Started

### Prerequisites
```bash
pip install -U dspy openai tiktoken
```

### Setup
```python
import dspy
import os

os.environ["OPENAI_API_KEY"] = "your-api-key"
dspy.configure(lm=dspy.LM("openai/gpt-4.1-mini"))
```

### Running the Demo
Open `prompt_optimization_gpt41mini_dspy.ipynb` in Jupyter Notebook or JupyterLab and run the cells sequentially.

## Results

The optimization process:
- Starts with a basic prompt: "You are concise. Answer correctly in <= 2 sentences."
- Automatically generates an optimized version that improves task performance
- Exports the learned prompt to `optimized_system_prompt.txt`

## Learn More

- [DSPy Documentation](https://dspy-docs.vercel.app/)
- [DSPy GitHub](https://github.com/stanfordnlp/dspy)
- [MIPROv2 Paper](https://arxiv.org/abs/2406.11695)

## About AI Tinkerers

AI Tinkerers is a community of AI enthusiasts, researchers, and practitioners exploring cutting-edge AI technologies and their practical applications.

## License

MIT