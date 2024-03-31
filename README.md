# LLM LORA Fine Tuning Classification
 Fine tuning LLM with LORA PEFT technique for classification task and comparing the result with Foundational Model.


In this repository, I have used HuggingFace Transformer library for a Supervised ML task. The repo contain generic code to
train a LLM model first from scratch on small epochs. Then the model is trained using LORA PEFT techiniqe. The result using LORA were better as the testing loss is compartively less after 3 epochs 0.48(in foundational model) to  0.25(using LORA training). 

The foundational model is trained completely from scratch on the dataset which will create new weights while learning. Whereas
using PEFT technique only specific layers of transformer model is trained,
this have huge adavantage as training using PEFT technique is much faster and the results were still better than retraining the model 
from scratch. Another disadvantage of training the LLM model from scratch is that it may suffer from Catastropic Forgetting, where the model
forget its already learnt weights and overrides them using the new learnt weights. This code uses Trainer module from HuggingFace for creating the training pipeline.

The notebook can be extended to train any HuggingFace Sequence Classificaiton LLM model with minor modifications as per the use case to train a model from scratch or train the model using LORA PEFT. 





