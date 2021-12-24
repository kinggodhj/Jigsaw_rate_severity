# [Jigsaw Rate Severity of Toxic Comments](https://www.kaggle.com/c/jigsaw-toxic-severity-rating/overview)


### Train data

- Data1: [Toxic classification](https://www.kaggle.com/c/jigsaw-toxic-comment-classification-challenge/data)

- Data2: [Recognizing toxicity & Reducing bias](https://www.kaggle.com/c/jigsaw-unintended-bias-in-toxicity-classification/data)

- Data3: ruddit dataset

- Data4: [Translation + Toxic classification](https://www.kaggle.com/c/jigsaw-multilingual-toxic-comment-classification/data)


# score

- Data1 + Data2 + Data3 + Ridge model: 0.846  

- Data1 + Cleaned Data1 + Data3 + Ridge model + RoBERTa (toxic severity validation data): 0.854

- Data1 + Cleaned Data1 + Data3 + Ridge model + RoBERTa (toxic severity validation data + data1): 0.837


### Data augmentation

[Back-translation](https://dzlab.github.io/dltips/en/pytorch/text-augmentation/)
