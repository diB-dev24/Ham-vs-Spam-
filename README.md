# Ham-vs-Spam-
a project attempting to analyse and identify the best classification model for filtering spam messages from a dataset 'spam.csv' from Kaggle. The notebook was made for a bootcamp training from Codecademy.

For this project, I first explored the dataset, analysing all through the columns and assessing their relevance to the task at hand. The unnamed columns did not seem to hold much of a correlation to whether a text message, was a spam or a ham, so I dropped them. Even analysing their length did not prove much of their importance. I am interested, however, with the relationship of the length of a text message and its label. 

to clean the data further, I also relabeled the v1 and v2 columns to 'labels' and 'texts' respectively. this would help make the code more readable/understandable. 

Also changed the value for spam to 1 and ham to 0.

I then ran the data through a train-test split to keep the labels aligned, then vectorized the data using a TF-IDF Vectorizer. This would convert the texts to weighted word counts, helping to identify typical spam words like 'free'.
I preferred TF-IDF, over N_grams because the texts had a lot of rare phrases that N_grams would not have generalized well, and thought CountVectorizer would be too basic for this task.

For the baseline Machine Learning model, I chose to go with the best version of Decision Tree I could model because I wanted to compare its performance with that of Logistic Regression. Logistic Regression was had a better Classification report, and even better results when the hyperparameters were tuned. Making it the best model for this project.

I also looked at RandomForest Classifier but the results were not as promising, although, it did have a 100% score for Precision with hyperparameters tuned.

For recommendation, I would suggest trying out N_grams as a vectorizer, just to see how it plays out with the data, and using the K-Nearest Neighor(KNN), as a ML model.
