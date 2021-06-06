# CS 522 hate speech project
## Evaluating the effectiveness of GPT-2 generated hate speech for SVM and BERT hate speech classification

### Problem Statement

The aim is to see if using GPT-2 generated data to train a predictive hate speech model will improve the accuracy of the model. 

### Methodology

The models we will be building are from using SVM and BERT. We will be comparing the effects of different amounts of GPT-2 generated data on the accuracy of the model. This project will be completed in python and run on google Colab. In order to utilize the data sets properly, much cleaning and pre-processing was done on them. Please read the final report for more details.

### Data set used
https://www.kaggle.com/mrmorj/hate-speech-and-offensive-language-dataset

This data set contained over 24000 tweets that were classified into hate speech, offensive language, or neither.

### SVM
Support Vector Machine essentially creates a line (or hyperplane) that divides and classifies the data. It makes sure that this line is as far away as possible from each of the closest data points on either side in order to find the best line. Tuning parameters include: C (higher C means higher accuracy for the training model), Gamma (higher Gamma means more influence from the points closer to the hyperplane than those further away). SVM is not specialized for NLP and does not contain its own dictionary.

### BERT
Bidirectional Encoder Representations from Transformers is a natural language processor. It takes text and learns contextual relations between the words in order to make predictions. BERT employs 2 strategies in its training: Masked LM (MLM), and Next Sequence Prediction (NSP). In MLM, BERT masks some percentage of the words getting fed into the trainer and then tries to predict those masked words based on what it has seen. This makes BERT more robust to noise. In NSP, pairs of sentences are sent as input. Part of the input pairs are sequential sentences (one follows the other and they are connected in some way), while the other part of input pairs has 2 disconnected sentences. BERT learns to predict if the second sentence in the pair is the subsequent sentence in the original document. BERT comes with its own corpus of words since it has already been trained.

### Tools used
Python (ipynb),
Numpy,
SVM,
BERT,
GPT-2, 
Microsoft Excel


