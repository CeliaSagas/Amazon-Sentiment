![Banner](https://github.com/CeliaSagas/EV-Queue/blob/1c39bc96dd561033cb5c162b8bdbf11fb56555bb/img/EV%20Queue.jpg)

# Amazon Review Sentiment Analysis

<!-- Add buttons here -->


![GitHub last commit](https://img.shields.io/github/last-commit/celiasagas/ev-queue)
![GitHub issues](https://img.shields.io/github/issues-raw/celiasagas/ev-queue)
![GitHub pull requests](https://img.shields.io/github/issues-pr/celiasagas/ev-queue)
![Project Code](https://img.shields.io/github/languages/top/celiasagas/ev-queue)


<!-- Describe your project in brief -->

**Analyzing Sentiment using ULMFiT**

The Amazon Reviews Dataset holds 3 Million 1 through 5 star reviews on a variety of topics including books, movies, and consumer tech. In order to analyze the sentiment of the reviews, I chose to focus on 1 star and 5 star reviews, which represent the Negative (1-star) and Positive (5-star) ends of the spectrum in the dataset.

A cursory view of the sentiment across 1 and 5 star reviews using VADER confirms that the compound sentiment score across both categories is sufficiently different.

The 1 star reviews are significantly more negative compared to 5 star reviews, and the comparison between both will reveal negative and positive trends in the data.

Topic Modeling with LDA reveals that there are four main product review types in the dataset, "books" , "products", "movies", and "music", although all topics contain the word "book" which implies this may be the predominant product category. 

ULMFiT is a transfer learning model that requires very little text cleaning before modeling. Therefore, the only text processing I did before training the model was removing punctuation and combining the comment title with the comment text.

The best learning rate for the ULMFit model on comment data is 1e-2, as revealed by the learning rate plot.

The final model predicts 1 star (0) and 5 star (1) reviews with an accuracy rate of 95.2%.

<!-- Add the footer here -->

![Footer](https://github.com/CeliaSagas/EV-Queue/blob/3255463ca3e10f165698d1ac0fc2dc03dc9a994b/img/evqueuefooter.png)
