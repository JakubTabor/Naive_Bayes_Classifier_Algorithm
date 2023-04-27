# Naive_Bayes_Classifier_Algorithm
# My df include spam messages and normal messages, I am gona train my "model" and "classifier" to predict the type of message
# I use method "groupby" "Category" and "describe" to look at values that interested me
# Then i create new column "spam" and apply numerical values on my "Category" data """df['spam'] = df['Category'].apply(lambda x : 1 if x=='spam' else 0)"""
# Now i have my df prepared for "train_test_split", as "X" i use "df.Message" and as "y" "df.spam"
# I need to change my "Message" into numerical value, so from "sklearn.feature_extraction.text" I import "CountVectorizer"
# First i get "X_train_count" using "fit_transform" method on "X_train" on "values"
# Then on "X_train_count" I use method "toarray" on my (3) column, I get my values in array
# Next from "sklearn.naive_bayes" import "MultinomialNB" and train my model """model.fit(X_train_count, y_train)"""
# I take 2 emails "true" and "spam" and use my "CountVectorizer" to "transform" my "emails", next i use my "model" to "predict" "prepared" "emails"
# """emails_count = v.transform(emails)""" """model.predict(emails_count)""" and I get good predictions
# Then I take "X_test" and "transform" it using "CountVectorizer" """X_test_count = v.transform(X_test)""" and i get "score" """model.score(X_test_count, y_test)"""
