# Text Classification (Deep Learning vs Decision Tree)

## Introduction

In this project we perform **_Text Classification_** using 2 different techniques and compare the results.

Classification techniques used:
1. Deep Learning 
2. Decision Tree

The libraries used in this project:
- **_Sentence Transformers_** _(based on PyTorch and Transformers)_
- **_Numpy_**
- **_Sklearn_**
- **_Matplotlib_**


## Files

**text_classification.ipynb** 
This notebook contains the necessary code for text classification using deep learning, followed by decision tree and the analysis of the results.


## Data 

The data contains a **total of 30 sentences** which includes **12 sentences about Computer** and **18 sentences about Cars.**

Example Sentences:
- _'computer powered autonomous rockets will take us to mars one day'_
- _'Artificial Intelligence will take over'_
- _'With electric cars there is a big environmental payoff'_


## Classification using Deep Learning

1. Here, we use a _Sentence Transformer model 'bert-base-nli-mean-tokens'_ for encoding our sentences and getting the embeddings.
2. Then we use the function _pytorch_cos_sim()_ to calculate the cosine similarity values of the class names (Automobile and Computers) and the embeddings of the text data.
3. Finally we compare the cosine similarity values of the input text with the class names and predict the class based on the result.

### Analysis of results from Deep learning:

Here we were able to classify all the sentences correctly.

<img width="985" alt="Screen Shot 2022-04-15 at 12 13 44 AM" src="https://user-images.githubusercontent.com/50517893/163517139-23f0e318-cca1-43af-a4a5-679d3b0c5735.png">


## Classification using Decision Tree

1. Before performing the classification, we provide classes for the sentences manually.
2. Now, we just tokenize the sentences and fit the model.

Following is a visualization of the decision tree.

<img width="800" alt="dt" src="https://user-images.githubusercontent.com/50517893/163514514-9d372550-06e4-42c2-bc19-beea7f53cc32.png">

### Analysis of results from Deep learning:

<img width="309" alt="Screen Shot 2022-04-15 at 12 15 08 AM" src="https://user-images.githubusercontent.com/50517893/163517228-4a6fb91b-177a-478b-ac0c-9ac963e2b601.png">


In the above results, '1' refers to the cars class and '0' refers to the computers class.
So as we can see, out of the 4 test sentences used 1 sentence was classified wrong.

# Conclusion

From analyzing the results from both approaches, deep learning style appears to be more accurate overall because the decision tree failed to classify a simple sentence.
