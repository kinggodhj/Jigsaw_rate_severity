# Jigsaw_rate_severity


[Jigsaw Rate Severity of Toxic Comments](https://www.kaggle.com/c/jigsaw-toxic-severity-rating/overview)

Firstly, using the ["Ruddit" data](https://github.com/hadarishav/Ruddit/tree/main/Dataset)

Crawling the comment using comment id from Ruddit data

cf) https://lovit.github.io/dataset/2019/01/16/get_reddit/

```
pip isntall praw

#Reddit auth: https://www.reddit.com/prefs/apps
```


```
import praw
reddit = praw.Reddit(client_id = 'qxVQztn8sSzupnPuqVE3lA',
                     client_secret = 'ByQJzTCkTAHzy0tU5M6Tj18GUiO3Eg',
                     user_agent = 'Heejin')
                     
```
