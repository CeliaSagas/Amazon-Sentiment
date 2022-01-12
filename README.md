![Banner](https://github.com/CeliaSagas/EV-Queue/blob/1c39bc96dd561033cb5c162b8bdbf11fb56555bb/img/EV%20Queue.jpg)

# Amazon Review Sentiment Analysis


**Analyzing Sentiment using ULMFiT**

The Amazon Reviews Dataset holds 3 Million 1 through 5 star reviews on a variety of topics including books, movies, and consumer tech. In order to analyze the sentiment of the reviews, I chose to focus on 1 star and 5 star reviews, sampling 10k of each, which represent the Negative (1-star) and Positive (5-star) ends of the spectrum in the dataset.

A cursory view of the sentiment across 1 and 5 star reviews using VADER confirms that the compound sentiment score across both categories is sufficiently different.

![Compound](https://github.com/CeliaSagas/Amazon-Sentiment/blob/ed665550c473ce94df700852d3e521da67e4cf11/img/compound.png)

The 1 star reviews are significantly more negative compared to 5 star reviews, and the comparison between both will reveal negative and positive trends in the data.

![Negative](https://github.com/CeliaSagas/Amazon-Sentiment/blob/ed665550c473ce94df700852d3e521da67e4cf11/img/negative.png)

Topic Modeling with LDA reveals that there are four main product review types in the dataset, "books" , "products", "movies", and "music", although all topics contain the word "book" which implies this may be the predominant product category.

![Topic Modeling](https://github.com/CeliaSagas/Amazon-Sentiment/blob/ed665550c473ce94df700852d3e521da67e4cf11/img/topics.png)

ULMFiT is a transfer learning model that requires very little text cleaning before modeling. Therefore, the only text processing I did before training the model was removing punctuation and combining the comment title with the comment text.

![Learning Rate](https://github.com/CeliaSagas/Amazon-Sentiment/blob/ed665550c473ce94df700852d3e521da67e4cf11/img/class_lr.png)

The best learning rate for the ULMFit model on comment data is 1e-2, as revealed by the learning rate plot.

The final model predicts 1 star (0) and 5 star (1) reviews with an accuracy rate of 95.3%.

<!-- Add the footer here -->

![Footer](https://github.com/CeliaSagas/Amazon-Sentiment/blob/ed665550c473ce94df700852d3e521da67e4cf11/img/amazon_footer.jpeg)
