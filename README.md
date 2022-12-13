# NLP_641
Natural Language Processing Project

## Introduction

Sentiment analysis is an application of natural language processing (NLP) that reveals the emotional states in human speech or text, and in this case, the speech and text that customers generate. Style transfer is generally a method used specifically for images and transferring the style of one image to the desired image. For text, we can transfer the style of a particular text to the desired text (e.g Shakespeare to normal text). We propose a model to transfer the sentiment from, e.g negative to positive, of a review on a film. A successful model will be able to rewrite a review/sentence in the desired sentiment. A good model will perform well according to various performance sequence-to-sequence metrics such as BLEU, or other new proposed approaches described in the literature.


## NLP Setup the Environment

https://docs.google.com/document/d/1ZQttvH2tzm2Zpb_SzTMi1rPlxBLxaIZgF_s44i14M6Y/edit?usp=sharing


# Sentiment Analysis

## Sentiment Analysis run Part 1: Build a complete pipeline for solving sentiment analysis problem

In this part wer use different packages in Python to build a complete pipeline for solving sentiment analysis problem. We use the simplest model, Mutinomial NB. There are serval result plot will be shown.

#### Pipeline
<img src="resources/pipeline.png">

Open the terminal
```
python3 Part1.ipynb

```

## Part 2: Word Embeddings and Neural Network

### Neural Network

LR works not so well when features are not linearly separable. It depends heavily on features, so feature engineering is essential if you are using LR.

#### A 2-layer neural network: 1 hidden layer + 1 output layer
<img src="resources/2-layer-nn.png">


This part is Extra work part. Just show the how to implement some NLP methods in another NLP applications. In this part we will use a powerful method to represent word in the numerical way and apply it to a simply 2-layer network for classification. We use the Load moon dataset from sklearn and emoji dataset from https://www.dropbox.com/s/g5pkso42wq2ipti/glove.tar.gz?dl=1.



To run this part
Run the following code in terminal after download the code
```
python3 Part2.ipynb

```


## Part 3: Build a deep LSTM network

#### A 2-layer LSTM sequence classifier. 
<img src="resources/LSTM.png">

#### Word Embedding
<img src="resources/word-vector.png">


This part is Extra work part. Just show the how to implement some more NLP applications.
In this part, we will build a deep LSTM network and insert a fixed pre-trained embedding layer in Keras.We use the Load moon dataset from sklearn and emoji dataset from https://www.dropbox.com/s/g5pkso42wq2ipti/glove.tar.gz?dl=1.

To run this part
Run the following code in terminal after download the code
```
python3 Part3.ipynb

```


## Part 4:
Text Style Transfer Portion:

For raw code featuring model creation and overall process refer to Final_project.ipynb and Sentiment_Style_Transfer_CycleGAN.ipynb. Note that the latter of the two files (i.e the one using CycleGAN) is incomplete and does not work. I have included it as a reference to you for some of the extra modeling that we worked on that did not work. For Final_Project.ipynb, if you would like to run the cells, simply run each cell in order to get the outputs. Note however that the modeling takes approximately an hour. Also note that running these notebooks requires access to training data, and they were run using either google colab or kaggle and so extracting files is dependent on the corresponding file system.

To get immediate results from the model, run main.py with the following command:

python main.py or python3 main.py

Note that this file extracts the model file and vocab files from S3 and so takes a few minutes to extract depending on internet connection strength. The program will give instructions on inputs to give it. Please follow the directions given to you upon running the file. For example, the program will ask if you would like to transfer a statement from negative to positive or vice versa and then will ask you to input a statement with negative or positive sentiment and will output the corresponding output statement in the opposite sentiment.

The required python versioning is given below:

python: 3.8.5
torch: 1.13.0
torchtext: 0.14.0
tqdm: 4.64.0
pandas: 1.1.3
nltk: 3.5
matplotlib: 3.3.2
boto3: 1.17.112

Please use these versions along with their corresponding dependencies to ensure appropriate output from the above files.
