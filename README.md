## The goal of this Project is to classify documents in a corpus. I will train a variety of linear models and 
evaluate each one using 5-fold cross-validation. Using my best performing model, I will run inference on a test set and show the predicted labels.

Dataset description:
The dataset contains five categories (sport, business, politics, entertainment, tech). The task is to classify documents to one of these five categories. I will be provided with the following datasets:
Raw training data (24_train_1.csv) with labels:
- The dataset contains the raw text of 1063 news articles and the article category. Each row is a document.
- The raw file is a .csv with three columns: ArticleId, Text, Category 
- The “Category” column are the labels I will use for training
Raw test data (news-test.cvs) without labels:
- This dataset contains raw text of 735 news articles. Each row is a document.
- The raw file is a .csv with two columns: ArticleId,Text. 
- The labels are not provided

Tasks:
1) Preprocess the raw training data:
Run Neural Networks with the 2-hidden layers, each has 128 neurons, extracting features by CountVectorizer() as the original features. Use 5-fold cross-validation to evaluate the performance.
Feature exploration. Use other features like TFIDF, or any word embeddings provided by other packages like GloVe with gensim, or BERT. Use 5-fold cross-validation to evaluate the performance of my Neural Network.
Describe how I generate features. 
Report the average training and validation accuracy, and their standard deviation for different feature construction (organize the results in a table).
Draw a bar figure showing the training and validation result, x-axis should be the parameter values, y-axis should be the training and validation accuracy. 

2) Explore the Neural Network model on pre-processed training data:
   Describe my parameter setting. Use 5-fold cross-validation to evaluate the performance w.r.t. the learning rates,
   I could use the feature engineering method that has the best performance from Question 1.  Recommended candidate values: [0.0001, 0.0003, 0.001, 0.003, 0.01, 0.03, 0.1]

3) Predict the labels for the testing data (using raw training data and raw testing data). 
