# 626
In the 626 q1, I have answered question 1. 
1.import and read the data set:
First I import the given txt file into R. Because the header is spaced by spaces and the data is spaced by tabs, the data set cannot be read directly. So, I use the strsplit() function to separate the first line of text by spaces and store the result in "header". Then I delete the first line of text in "data" because it is a header and not data, and then use the read.table() function to convert the text in "data" into a data frame.
2.Grouping of activity and modeling by GLM
According to the requirements of the question, I classified the activities by classifying 1, 2 and 3 as 1 and the rest as 1 in training data. A commonly used method is to employ logistic regression models, which are also referred to as generalized linear models (GLMs). I applied GLM to generate a model.
3.make prediction
Based on the model formed by GLM, I made a prediction based on the test data and extracted the prediction using the write.table() function. 

In the rf 626 q2, I use the baseline algorithm to answer question 2. 
1.import and read the data set:
First I import the given txt file into R. Because the header is spaced by spaces and the data is spaced by tabs, the data set cannot be read directly. So, I use the strsplit() function to separate the first line of text by spaces and store the result in "header". Then I delete the first line of text in "data" because it is a header and not data, and then use the read.table() function to convert the text in "data" into a data frame.
2.Grouping of activity and modeling by random forest
According to the requirements of the question, I classified the activities into 1 to 7, and the activities greater than 7 were also classified into 7. Then I applied random forest to form the model. Because random forests can handle large data sets and avoid overfitting. Random forests are also able to capture complex nonlinear relationships in the data, and it works well for classification problems. I think random forests are suitable for building a refined multi-class classifier, so I first tried using random forests to form a model.
3.make prediction
Based on the model formed by random forest, I made a prediction based on the test data and extracted the prediction using the write.table() function. 

In selftest, I split the training data into new training data and new test data in the ratio of 75 percent and 25 percent, then I use new training data to predict the new test data, and compare this predicted data with the original data to self-check the accuracy.
 
 
LDA can map high-dimensional data to low-dimensional space by linear transformation to reduce the number of features and improve the classification accuracy, and lda can classify quickly and accurately even in high-dimensional space, which is very suitable for classification problems, so I have tried to use lda
Here I tested lda, svm and boosting to form the model, I found that svm had the highest accuracy and used it as the final algorithm 

In the svm 626 q2, I use the final algorithm  to answer question 2. 
1.import and read the data set:
First I import the given txt file into R. Because the header is spaced by spaces and the data is spaced by tabs, the data set cannot be read directly. So, I use the strsplit() function to separate the first line of text by spaces and store the result in "header". Then I delete the first line of text in "data'' because it is a header and not data, and then use the read.table() function to convert the text in "data" into a data frame.
2.Grouping of activity and modeling by random forest
According to the requirements of the question, I classified the activities into 1 to 7, and the activities greater than 7 were also classified into 7. Then I applied SVM to form the model. SVM can efficiently handle large datasets with features and can obtain good generalization even with small training data. In addition, SVM has several advantages over other classification algorithms. For example, they are less prone to overfitting than other algorithms (e.g random forests), so I adopted SVM as my final algorithm.
3.make prediction
Based on the model formed by svm, I made a prediction based on the test data and extracted the prediction using the write.table() function.


According to the results of my self-test, SVM has the highest accuracy, and the self-test is formed based on training data. lda does not perform well when dealing with large sample data, and random forests may have overfitting problems when dealing with high-dimensional data, so compared to them, SVM performs better and has higher accuracy

Data preprocessing can help reduce the influence of noise and outliers and improve the accuracy of SVM. Ensemble learning can combine multiple SVM models to improve classification accuracy. For example, bagging, boosting, etc. can be used to ensemble multiple SVM models and obtain better classification results.

The final accuracy of Q1 is 1 and  final accuracy of Q2 is 0.959. I tried some different models to improve accuracy. 

