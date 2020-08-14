# Text-Classification_sentiment-Analysis_financial-news-data


Summary of the notebook

The notebook is divided into the several sections, and will be keep updated during my internship with a further study of a text classification.

The purpose of this notebook is to perform a text classification of financial news article with target value of Sentiment ($positive, neutral, negative$) and Importance ($important, normal, negligible$) regarding the firm it covers. With two parameters, our team will select 15-20 firms that are worth spotlight of a day and publish a report about the firm automatically.

In this notebook, I have implemented text classification using deep learning method, and have achieved $76$% accuracy on 5-fold cv but our team focuses on what we defined as critical error.

Let $S_i,r$ be the actual sentiment of the article labeled by analyst, and $S_i,p$ be the predicted sentiment of the article by the model. Then, the critical error is defined as below:

* $Critical\enspace Error = \frac{\sum_{i=1}^{n} \mathbb{1}_\{S_i,r = positive, S_i,p\ = negative\} +  \mathbb{1}_\{S_i,r = negative, S_i,p\ = positive\}}{Total\enspace number\enspace of\enspace article}$

The sentiment can be changed to importance with $positive = importance$ and $negative = negligible$. Since the evaluation of the article might be different by analysts' perspectives, we do not like to publish a report with news tagged as negative but some view as positive. We want such report to be published as neutral. Therefore, we care more about the critical error that we have defined. 
