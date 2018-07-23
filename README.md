# IMDB Sentiment Analysis
In this project, I tried to perform sentiment analysis on the IMDB reviews dataset.
My primary goal was to improve my knowledge of some of the main deep learning libraries namely TensorFlow (basic APIs and Estimator APIs), Keras, and Pytorch. Even if this project strengthened my knowledge of NLP, sentiment analysis on this IMDB data set was more an excuse to learn these libraries and compare the implementation of a same model architecture (LSTM on top of GloVes embeddings) on the same data, than a goal in itself. I didn't try to optimize the model I was using, and even realized half-way through the project, that Convolutional Neural Networks are better suited for sentiment analysis than LSTM (the model I used). LSTM couldn't even beat a simple baseline made of Logistic Regression on top of Bag of Word.
Here are the accuracy I obtained with the different libraries (picking for each implementation the best value obtained by tuning the number of epochs/steps):
1. Logistic Regression on BOW with TF-IDF: 89.57 \%
2. TensorFlow basic APIs (LSTM on GloVes (100d)) : 85.11\%
3. TensorFlow Estimator APIS (LSTM on GloVes (100d)): 85.77\%
4. Keras (LSTM on GloVes (100d)): 86.39\%
5. Pytorch (LSTM on GloVes (100d)): 85.197\%

