# Attribution

## 1. Dataset
This project uses the ToxicChat dataset, 'lmsys/toxic-chat', which we accessed through the Hugging Face 'datasets' library. The dataset contains user-generated prompts that were annotated for toxicity vs. safety. These labels are used in this project to train and evaluate a binary classification model. 

## 2. Pretrained Model

This project uses DistillBERT from Hugging Face Transformers. Model='distilbert-base-uncased'. We used this model as a pretrained transformer encoder and fine-tuned it for binary toxic/safe classification. 

## 3. Libraries and Frameworks

We used the following libraries were used in this project:

* Pytorch for model training
* Hugging Face Transformers for pretrained model access/fine tuning
* Hugging Face Datasets for dataset loading
* Scikit-learn was used for train/validation/test splitting and final metric calulations
* NumPy, Pandas, and matplotlib were used for visualizing training curves

## 4. AI Assistance

We specifically used ChatGPT for generating policy prompts, and debugging a few syntax issues we were having with the Hugging Face Trainer capability. We made sure to review any suggested debugging mechanisms, and all final interpretations were our own.

We used ChatGPT to generate policies for Version 2B and 2C and it initially generated very generic policies, so we updated our prompts to make sure that B represented a policy that was concise but very strict with its definitions, while C was also concise but much more lenient in its definitions and allowing minor instances of problematic text to be classified as safe. 

And for the debugging help, we used ChatGPT to find out why a certain package wouldn't install or if there were any issues with our Colab environment. For that, it also took some reworking to be more specific in our prompts to the model to make sure the guidance we were getting was accurate. 
