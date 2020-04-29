# Rating-Prediction-based-on-Review-Similarity

## Introduction
This is a Machine Learning Project performed on 493887 customer reviews. Reviews are processed using common NLP techniques, then after calculating review similarity, a lasso model is used to predict customer rating. The OOP accuracy of the prediction model is 0.629.

## Data information: 
• reviewerID - ID of the reviewer, e.g. A2SUAM1J3GNN3B 
• asin - ID of the product, e.g. 0000013714 
• reviewerName - name of the reviewer 
• helpful - helpfulness rating of the review, e.g. 2 out of 3 people found the review to be helpful. The starter code’s dataframe would have 2 in the helpful_start column and 3 in the helpful_end column 
• reviewText - text of the review 
• overall - rating of the product 
• summary - summary of the review 
• unixReviewTime - time of the review 

## Steps of the project
1.Treat each review as a document. Ignore misspellings. Convert all reviews to lower case. Remove stop words. 
2. Handle negation: (e.g., don't, didn't etc.). Split off the "n't" part from "xxxn't" into separate words "xxx" and 
"not". Attach all 'not's (any normal "not" appearing in the text as well as the "n't" converted to "not") to the subsequent word, eg "not_nextword". 
3. Stem all words using Porter 1979. 
4. Create frequency count table for all word stems in all reviews. Use the most frequent 500 words to define the word vector. Create a bag-of-word vector representation for each review in electronics. 
5. Establish a method for measuring the distance between different reviews. Print the mutual distance between the first 100 reviews (review IDs) to screen, sorted from closest to furthest. 
6. Run a PCA and graph the first two PCs for the first 100 reviews.
7. Perform a lasso logistic regression and measure the out-of-sample accuracy of your method of choice. 
8. Establish a method for measuring the distance between different products. 
