# LLM LORA Fine Tuning Classification
 This notebook, explores the difference between training a LLM model from scratch and training the same LLM model using the Low Rank Adaptation (LORA) technique.

LORA is a Performance Efficient Fine Tuning (PEFT) technique where only a few specific layers of a transformer LLM layer are trained instead of training the whole model from scratch. 




Here are the advantages of using the LORA-PEFT technique:

- Training the LLM model using the LORA technique is much faster, and the results were still better than retraining the model from scratch.

- Training the LLM model from scratch means that it may suffer from Catastropic Forgetting, where the model forgets its already learned weights and overrides them using the newly-learned weights. (The LLM model forgets its previous learning and replaces it with new learning from a new dataset.)




I have used HuggingFace transformer library and trained the classification model (Supervised Machine Learning)  using the Trainer module. This code pipeline can be easily extended to any Hugging Face Sequential Classification LLM model with minimal changes.




When to use the above models for classification tasks

- When you have a very small training dataset, LLM works magic in these scenarios, and even with a small dataset, the model can be trained to perform classification tasks efficiently. (Note, use the LORA PEFT technique here.) 

- If you have large training data, I would recommend going for traditional Deep learning models with pre-trained weights, and training your model on a large dataset. The advantage will be faster inference, as LLM takes up a lot of space and requires a longer inference time for prediction.

- Train your LLM model from scratch if you have a specialized scenario (e.g., an insurance domain) and a large dataset to train your LLM from scratch. LLMs like GPT are generally trained on public data sources from internet like Wikipedia, web scraping, etc. However, my recommendation will be to first train the model using LORA and go for model training from scratch only if training results are not better. 




Feel free to extend the code or add comments for improvement. This code is part of the Udacity Generative AI Nanodegree project.