# Setup Guide

## 1. Project Overview

This project consists of two main phases:

* Phase 1: Fine-tuning DistilBERT for a downstream NLP task.
* Phase 2: Evaluating outputs using an LLM-as-a-judge framework.

Both phases are implemented as Jupyter notebooks.

## 2. Prerequisites

Make sure you have the following installed:

* Python 3.9+
* pip or conda
* Git

## 3. Installation

Step 1: Clone the repository

```bash
git clone <your-repo-url>
cd <your-repo-name>
```

Step 2: Create a virtual environment

Using venv:

```bash
python -m venv venv
source venv/bin/activate  # macOS/Linux
venv\\Scripts\\activate     # Windows
```

Step 3: Install dependencies

Install the core dependencies manually:

```bash
pip install torch transformers datasets scikit-learn pandas numpy matplotlib jupyter openai
```

## 4. Running the Project

Launch Jupyter Notebook

```bash
jupyter notebook
```

Then open and run the notebooks in order:

1. `Phase 1 - Fine-tuning DistillBERT.ipynb`
2. `Phase 2 - LLM-as-judge.ipynb`

Make sure to run all cells sequentially.

## 5. External APIs / Services

This project uses external API calls to Google Gemini's free tier. Create an 
This project may use external APIs (e.g., OpenAI API) for evaluation.

Setting up API Keys

1. Log into Google AI Studio with your existing Gmail account.
2. Create a new Gemini Project.
3. Generate an API key.
4. Set the API key as an environment variable. We used Google Colab's "secret key" button to hide the API key from being pushed onto the public repo. 

## 6. How to Test the System

Phase 1 Testing

* Run all cells in the Phase 1 notebook.
* Verify that:

  * The dataset loads correctly.
  * The model trains without errors.
  * Evaluation metrics (e.g., accuracy, F1 score) are produced.

Phase 2 Testing

* Run all cells in the Phase 2 notebook.
* Ensure that:

  * The API key is correctly set.
  * Model outputs are generated.
  * The LLM judge produces evaluation scores or comparisons.
