# IMDB Sentiment Analysis
## Project objectives
In this project, I tried to perform sentiment analysis on the IMDB reviews dataset. I did it in spring 2018.
My primary goal was to improve my knowledge of some of the main deep learning libraries namely TensorFlow (basic APIs and Estimator APIs), Keras, and Pytorch. Even if this project strengthened my knowledge of NLP, sentiment analysis on this IMDB data set was more an excuse to learn these libraries and compare the implementation of a same model architecture (LSTM on top of GloVes embeddings) on the same data, than a goal in itself. I didn't try to optimize the model I was using, and even realized half-way through the project, that Convolutional Neural Networks are better suited for sentiment analysis than LSTM (the model I used
## Results and conclusions
LSTM couldn't beat a baseline made of Logistic Regression on top of Bag of Word.
Here are the accuracy I obtained with the different libraries (picking for each implementation the best value obtained by tuning the number of epochs/steps):
1. Logistic Regression on BOW with TF-IDF: 89.57 \%
2. TensorFlow basic APIs (LSTM on GloVes (100d)) : 85.11\%
3. TensorFlow Estimator APIS (LSTM on GloVes (100d)): 85.77\%
4. Keras (LSTM on GloVes (100d)): 86.39\%
5. Pytorch (LSTM on GloVes (100d)): 85.197\%

Concerning the different frameworks, here are my conclusions (but things may have change since 2018):
* If one wants to use a mainstream neural architecture without to much experimentation Keras is the framework easiest to use.
  It mimicks the style of scikit-learn, which makes it usage very intuitive.
* Unlike keras, Pytorch and Tensorflow offer a direct grip on the neural network architecture and offer the possibility of trying
  completely new architectures.
* Pytorch's functions and classes are simpler to understand and to use (at least for a new user) than those of Tensorflow which
  often seem unintuitive and obscure.
* Pytorch official documentation was good and straightforward whereas the Tensorflow one is not beginner friendly: the first 
  introductory tutorial tells you to use eager execution. The next one completely ignores the first one and tells
  you that TF Estimator is the thing you need. By the third or fourth tutorial (still in the same official 
  documentation for beginners) you're presented some raw Tensorflow without any explanation.
* Tensorflow main advantage that I could personally appreciate was Tensorboard which gives a very nice way to decide when
  to stop the training.

