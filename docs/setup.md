# Setup Guide

## 1. Project Overview

This project contains two main phases:

* Phase 1: Fine-tuning DistilBERT for toxicity detection of user prompts to an LLM
* Phase 2: Using LLM-as-judge to automate classification for a smaller batch of user prompts

We implemented both phases with Jupyter notebooks. 

## 2. Prerequisites

Make sure you have the following installed:

* Python 3.9+
* pip or conda
* Git

## 3. Installation

Step 1: Clone the repo

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

Make sure to run all of the cells in order.

## 5. External APIs / Services

This project uses external API calls to Google Gemini's free tier, so follow these steps to create your own API key with Gemini:

1. Log into Google AI Studio with your existing Gmail account.
2. Create a new Gemini Project.
3. Generate an API key.
4. Set the API key as an environment variable. We used Google Colab's "secret key" button to hide the API key from being pushed onto the public repo. 

## 6. How to Test the System

Phase 1 Testing

* Run all cells in the Phase 1 notebook.
* Make sure that:

  * The dataset loads correctly.
  * The model trains without errors.
  * Evaluation metrics (e.g., accuracy, F1 score) are produced.

Phase 2 Testing

* Run all cells in the Phase 2 notebook.
* Make sure that:

  * The API key is correctly set.
  * Model outputs are generated.
  * The LLM judge produces evaluation scores or comparisons.
