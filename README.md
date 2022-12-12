


## Background

**Clickthrough rate (CTR):**
![enter image description here](https://github.com/a-oh/project3/blob/master/images/ctr.png?raw=true)
 - A ratio showing how often people who see your ad or product listing end up clicking it.
 - Clickthrough rate (CTR) can be used to gauge how well your keywords and ads are performing.


## Introduction

The term 'clickbait' describes **sensationalist** headlines used by news websites such as Buzzfeed as tactics to gain the maximum number of readers. Rather than delivering a news story that adheres to journalistic integrity, this type of reporting relies on emotionally charged terms and biased stance to provoke curiosity in readers to 'click' and learn more.


However, despite the negative connotation of the term 'clickbait,' Clickthrough Rate (CTR) is a widely used metric for measuring the effectiveness of advertisement and marketing.  

Here, I am using two subreddits r/UpliftingNews and r/NottheOnion, two very different types of news articles that gain popularity online, as case studies for investigating whether there are any distinctive characteristics in their titles that draw readers' attention by implementing NLP models.


## Summary

This notebook contains 3 sub-notebooks that details each step of the NLP modeling:
- subreddit web scraping / EDA
- preprocessing
- NLP modeling using various transformer/estimater




**Number of Words Included in the Title**
![enter image description here](https://github.com/a-oh/project3/blob/master/images/wordscounttitle.png?raw=true)

**Most Frequently Appearing Unique Words from Each Subreddit**
![enter image description here](https://github.com/a-oh/project3/blob/master/images/mostfrequentwords.png?raw=true)

**Sentiment Analysis of Two Subreddits**
![enter image description here](https://github.com/a-oh/project3/blob/master/images/sentanalysis.png?raw=true)


## Conclusion/Recommendations

 - Logistic regression and Random Forest performed relatively well for the train set, but significantly underperform for the test set, implying the model is highly overfitted
 - CountVectorizer/logistic regression combination model has the highest prediction rate


![summary of train/test score of transformer/estimater combination](https://github.com/a-oh/project3/blob/master/images/models.png?raw=true)

 - Overall performance is around 80-85% for all the models. Although the prediction rate is higher than expected, there is no single superior model to be implemented
 - Cvec/Logreg model provides some insights on most impactful words for predicting whether the post is from Uplifting News or NottheOnion

 - ![enter image description here](https://github.com/a-oh/project3/blob/master/images/highcoef.png?raw=true)![enter image description here](https://github.com/a-oh/project3/blob/master/images/lowcoef.png?raw=true)
 - Due to the highly complex nature of language, there is no single equation that can generate titles that would produce high CTR. However, the analysis reveals some insights on how to target length, words, and sentiment of titles
 - More sophisticated analysis using additional measures is needed to sense subtle nuanced tones and sarcasm.
