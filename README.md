# [Jigsaw Rate Severity of Toxic Comments](https://www.kaggle.com/c/jigsaw-toxic-severity-rating/overview)


### Train data

- Data1: [Toxic classification](https://www.kaggle.com/c/jigsaw-toxic-comment-classification-challenge/data)

- Data2: [Recognizing toxicity & Reducing bias](https://www.kaggle.com/c/jigsaw-unintended-bias-in-toxicity-classification/data)

- Data3: ruddit dataset

- Data4: [Translation + Toxic classification](https://www.kaggle.com/c/jigsaw-multilingual-toxic-comment-classification/data)


### Method

- Ridge

- Ligression (too slow)

- Lasso (lower performance)

- RoBERTa + Margin Ranking Loss

- RoBERTa + triplet Ranking Loss (lower performance)


### score

- Data1 + Data2 + Data3 + Ridge model: 0.846  

- Data1 + Cleaned Data1 + Data3 + Ridge model + RoBERTa (toxic severity validation data): 0.854

- Data1 + Cleaned Data1 + Data3 + Ridge model + RoBERTa (toxic severity validation data + data1): 0.837


## Ideas

- ~~triplet loss~~ 

- Back translation ([Data augmentation](https://dzlab.github.io/dltips/en/pytorch/text-augmentation/)) 

- Finding out the wegith ratio of each method

- HateBERT

## Comment

- Generate a predicted score for all of the less_toxic and more_toxic comments and calculate the proportion of scores where less_toxic < more_toxic. This is the same way that the leaderboard scores are calculated.

- Hypothesis: Tech companies fillter the "toxic" words in training datasets -> try ["HateBERT"](https://www.kaggle.com/c/jigsaw-toxic-severity-rating/discussion/288788)

- Toxic word [list](https://www.kaggle.com/c/jigsaw-toxic-severity-rating/discussion/287173)
