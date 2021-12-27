# [Jigsaw Rate Severity of Toxic Comments](https://www.kaggle.com/c/jigsaw-toxic-severity-rating/overview)


### Train data

- Data1: [Toxic classification](https://www.kaggle.com/c/jigsaw-toxic-comment-classification-challenge/data)

- Data2: [Recognizing toxicity & Reducing bias](https://www.kaggle.com/c/jigsaw-unintended-bias-in-toxicity-classification/data)

- Data3: ruddit dataset

- Data4: [Translation + Toxic classification](https://www.kaggle.com/c/jigsaw-multilingual-toxic-comment-classification/data)


### Method

- Ridge

- Ligression (too slow)

- ~~Lasso (lower performance)~~

- RoBERTa + Margin Ranking Loss

- RoBERTa + triplet Ranking Loss (lower performance)

- RoBERTa + MSE Loss

### score

- TF-IDF(data 1,2,3) + Ridge model: 0.846  

- Word2vec(data1, clean data1, 3) + Ridge model: 0.7

- RoBERTa + Margin Ranking Loss
  
  0.9 (Data1 + Cleaned Data1 + Data3 + Ridge model) + 0.1 (RoBERTa (toxic severity validation data)): 0.845

  0.85 (Data1 + Cleaned Data1 + Data3 + Ridge model) + 0.15 (RoBERTa (toxic severity validation data)): 0.854

  0.8 (Data1 + Cleaned Data1 + Data3 + Ridge model) + 0.2 (RoBERTa (toxic severity validation data)): 0.843
  
  Word2vec + 0.85 (Data1 + Cleaned Data1 + Data3 + Ridge model) + 0.15 (RoBERTa (toxic severity validation data)): 0.816
  
  
- RoBERTa + Margin Ranking Loss + More data
  
  Data1 + Cleaned Data1 + Data3 + Ridge model + RoBERTa (toxic severity validation data + data1): 0.832

- RoBERTa + MSE Loss

  0.85 (Data1 + Cleaned Data1 + Data3 + Ridge model) + 0.15 (RoBERTa (toxic severity validation data)): 0.837

- RoBERTa + triplet Loss
  
  0.85 (Data1 + Cleaned Data1 + Data3 + Ridge model) + 0.15 (RoBERTa (toxic severity validation data + data1)): 0.825
  

## Ideas

- ~~triplet loss~~ 

- ~~Word2vec~~

- Increasing the number of "n fold"

- Back translation ([Data augmentation](https://dzlab.github.io/dltips/en/pytorch/text-augmentation/)) 

- Finding out the wegith ratio of each method

- HateBERT

## To do

- make evaluation metric 


## Comment

- Generate a predicted score for all of the less_toxic and more_toxic comments and calculate the proportion of scores where less_toxic < more_toxic. This is the same way that the leaderboard scores are calculated.

- Hypothesis: Tech companies fillter the "toxic" words in training datasets -> try ["HateBERT"](https://www.kaggle.com/c/jigsaw-toxic-severity-rating/discussion/288788)

- Toxic word [list](https://www.kaggle.com/c/jigsaw-toxic-severity-rating/discussion/287173)
