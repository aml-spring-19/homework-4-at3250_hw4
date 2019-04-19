#Amon Tokoro Timothy Luk
# homework-4-at3250_hw4
homework-4-at3250_hw4 created by GitHub Classroom

Since the reddit_200k_train.csv contains the sufficient number of rows, we did not actually test our models with reddit_200k_test.csv.

Since the data is imbalance, we undersample and have around 60k for each target group. 
Count vectorizer doesn't work well with pipeline, because count vectorizer takes in a list of strings while logistic regression takes in np array or list of list. Therefore, we have to do count vectorizer outside of the pipeline and grid search. Adding new features is also an issue when trying to pipeline the entire process. We couldn't use a column transformer here, because count vectorizor is a sparse matrix and the new features in ndarray needed to be converted into a sparse matrix format in order to be appended to the sparse matrix. Column transformer doesn't support that. Therefore making training unseen data extremely cumbersome. 
