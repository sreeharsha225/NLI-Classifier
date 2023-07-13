# Natural Language Interference

## Introduction

This is a project for the course NLP. The goal of this project is to build a model that determine whether a given hypothesis is true (entailment), false (contradiction), or undetermined (neutral) based on a given premise. We used SNLI dataset, which is a collection of 570k human-written English sentence pairs manually labeled for balanced classification with the labels entailment, contradiction, and neutral, supporting the task of natural language inference (NLI), also known as recognizing textual entailment (RTE). and MultiNLI dataset, which is a crowdsourced collection of 433k sentence pairs annotated with textual entailment information. The sentence pairs cover a range of genres of spoken and written text, as well as a range of phenomena studied in NLP, including delexicalization, reference, lexical semantics, and knowledge and reasoning. We used the pre-trained BERT model to build our model. We also used the pre-trained BERT model to extract the features of the sentences and then used the features to train a classifier. We compared the performance of the two models and found that the model based on the pre-trained BERT model has better performance.

## Dataset

We used the SNLI dataset and MultiNLI dataset. and glove.42B.300d.txt,glove.6B.300d.txt as the pre-trained word embedding for the LSTMNLI model.The dataset of the project is in the data folder. Due to size constraints.The complete dataset can be downloaded from the following link:[Data Folder](https://iiitaphyd-my.sharepoint.com/:f:/g/personal/veera_sree_students_iiit_ac_in/EifQa3zOM9xBkcPjlE9dpv8BKb083Jv0NQQxb2aotSQAxg?e=qVRXhH)

## Model

We used LSTM to build NLI model. And we used the pre-trained BERT model to extract the features of the sentences and then used the features to train a classifier. We compared the performance of the two models and found that the model based on the pre-trained BERT model has better performance. The model is in the model folder. Due to size constraints.The complete model can be downloaded from the following link: [Models Folder](https://iiitaphyd-my.sharepoint.com/:f:/g/personal/veera_sree_students_iiit_ac_in/EinkwmUqtrxLuLKfgMiPRkkBb1EQFUlS9psmasBsFfjjhA?e=q5T4ce)

## Structure of submission

```
.
├── Readme.md
├── reports_and_results
│   ├── report_lstm_nli_mnli_foreachepoch_42B.txt
│   ├── report_lstm_nli_mnli_foreachepoch.txt
│   ├── report_lstm_nli_snli_foreachepoch_42B.txt
│   └── report_lstm_nli_snli_foreachepoch.txt
└── src
    ├── bert_nli_pytorch.ipynb
    ├── distilbert_nli_pytorch.ipynb
    ├── lstm_nli_42B.ipynb
    ├── lstm_nli.ipynb
    └── roberta_nli_pytorch.ipynb
```
## Instructions to reproduce the results

### LSTM

#### SNLI

- Run the lstm_nli.ipynb file in the src folder to train the model.

#### MultiNLI

- Run the lstm_nli_42B.ipynb file in the src folder to train the model.

### BERT

#### SNLI

- Run the bert_nli_pytorch.ipynb file in the src folder to train the model.


## Results

|    Models   |  SNLI | MultiNLI | ContractNLI |
|:-----------:|:-----:|:--------:|:-----------:|
|     LSTM    |  75%  |    62%   |      -      |
|     BERT    | 86.4% |   80.3%  |      -      |
|   SpanBERT  | 88.5% |   82.5%  |      -      |
| SpanNLIBERT |   -   |     -    |    81.6%    |
## Presentation
- The following link contains the presentation of the project [Presentation](https://iiitaphyd-my.sharepoint.com/:p:/g/personal/sri_ram_students_iiit_ac_in/ERZQiqSlufZCt4w3N5P2bGoBkJP3pC9tkha3umt5dcT6tQ?e=DkS6n1)

## Reference

- [BERT: Pre-training of Deep Bidirectional Transformers for Language Understanding](https://arxiv.org/abs/1810.04805)
