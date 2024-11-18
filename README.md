Comment from the coding mentor: Again, great job on this task, however I want you to take note of the following:
1. All comments must be enclosed by a hash (#) as per the PEP8 Style Guide or if you wish to add a section of only text add the markdown cell.

2. You cannot guess the value of the parameter to be 100. You must tune the parameter to determine the value that optimises the model’s performance. How do we do this?
a) Define the range of values n_estimators = 20, 50, 100 and 15.
b) Create a RandomForestClassifier().

c) Then we can use GridSearchCV() to perform parameter tuning. This function takes the RandomForestClassifier, a range of values and the value of cv (cross-validation).

d) From GridSearchCV you will get the best_params_ which is the value of n_estimators.

e) Once you have determined the value of n_estimators. You then must predict y_pred to the best random forest model which is given by grid_search.best_estimator.

3. You did not interpret the model performance measures. Hint on how to interpret the model performance:
a) If accuracy is 95% it means that the model is correct 95% of the time.

b) If precision is 95% it means that 95% of the instances the model predicted as positive are positive.

c) If recall is 95% it means that the model identified 95% of all actual positives.

d) If precision is 95% it means we have an almost perfect precision and recall which is desirable because we want a single metric that summarises both precision and recall.

4. There is better way to display the confusion matrix which improves readability of the output. Check example: https://gist.github.com/MamakgooaM/ec39552fb1f8e0e1f965f13e3e841427
