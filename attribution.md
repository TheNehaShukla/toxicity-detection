Dataset: This project uses the ToxicChat dataset 'lmsys/toxic-chat', which we accessed through the Hugging Face 'datasets' library.

The dataset contains user prompts that were labeled for toxic/safety.
Pretrained Mode: This project uses DistillBERT from Hugging Face Transformers.

Model='distilbert-base-uncased'. We used this model as a pretrained transformer encoder and fine-tuned it for binary toxic/safe classification.
Libraries:

This project uses Pytorch for model training, Hugging Face Transformers for pretrained model access/fine tuning, and Hugging Face Datasets for dataset loading.
Scikit-learn was used for train/validation/test splitting and final metric calulations.
NumPy, Pandas, and matplotlib were used for visualizing training curves.
AI Usage We specifically used ChatGPT for generating policy prompts, and debugging a few syntax issues we were having with the Hugging Face Trainer capability. We made sure to review any suggested debugging mechanisms, and all final interpretations were our own.
