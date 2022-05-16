# Multilingual-Task-Similarity


The objective of this project is developing the
language processing tool to efficiently obtain the
similarity between different news articles of different
languages based on multiple factors including
geography, entities, time, narrative, style and
tone. The problem statement is defined based on
the Codalab Competition, Multilingual News Article
Similarity and we are obtaining data from the
competition dataset itself. Here, the similarity is
obtained pairwise on a 4-point scale. The data constitutes
over 7 languages namely, English, Spanish,
German, Polish, Turkish, Arabic and French, having
both cross-lingual pairs as well as monolingual
data. There are over 4964 pairs of news articles in
the mentioned languages.

First run the "mbert_model_training.ipynb" for getting the initial mbert model and saving it.
Then run the "All_6_model_training_evaluation.ipynb" for saving weights of 6 models considering 6 features basically training the models and finding individual pearson correlation coefficients.
Then run the "Neural_network_training.ipynb" for running the neural network model.
At last run "Final_Model_evaluation.ipynb" for combining the above two and getting final pearson correlation coefficients.


Following below are the model links which are trained in this task :
 
 6 models for 6 different features -->
https://drive.google.com/drive/folders/1VxWMhx1vNLjSpCOEVsbjh0bXngCK-7MA?usp=sharing

mbert model -->
https://drive.google.com/file/d/1zKDbeXuAkQJsDEF9QVUQjFGYxWIsUfi9/view?usp=sharing

neural network model -->
https://drive.google.com/file/d/1PeBsgRKWyNQdfmc1VInYlHmtKvjpzy1B/view?usp=sharing


## Requirements 
install git+https://github.com/huggingface/transformers.git

install sentence-transformers

## Results 

The Pearson’s correlation with the ground truth
labels on the evaluation dataset for different models
and loss functions are shown in table below: 

| Model Name  | MSE Loss | L1 Loss |
| ------------- | ------------- | ------------- |
| mBERT  | 0.7325  | 0.7198 |
| XLM-RoBERTa-Base  | 0.5915  | 0.4276 |
| XLM-RoBERTa-Large  | 0.3188  | 0.2234 |
