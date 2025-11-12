## Types of ML systems
1. **Supervised**
    1. **Regression**: predicts numeric value
    3. **Calassification**: predicts likelyhood of something belonging to some category 
        1. Binary: in binary classification there are only two possible outcomes. ex. spam or not spam
        2. Multiclass: in multiclass classification there are more than two possible outcomes.
3. **Unsupervised: Model**: is given data that does not contain correct answer instead it employs technique called as clustering which creates grouping of the data. ex. private, public, work
4. **Reinforcement learning**: It learns by getting reward or penalties based on the action performed. ex. Self driving cars
5. **Generative AI**: creates content from user input

##

**Regression Model**:
1. Linear Regression: y = mx + b https://github.com/pravinvarma/tensorflowJS/blob/master/3x%2B1.html
2. Polynomial Regression: y = ax^2 + bx + c https://github.com/pravinvarma/tensorflowJS/blob/master/x%5E2%2B2x%2B1.html
3. Logistic Regression: <pre> It has two parts(z = wx + b) a. linear regression b. logistics function y = 1 / (1 + e^(-z)) where z = wx + b
    For calculating probabilities, we need to have output of logistic regression between 0 to 1. Logistics function is used to convert the output of linear regression to a value between 0 to 1. Tha standard logistic function is sigmoid function. f(x) = 1/1+e^-x where e is Eurels number(2.71828)
    ex: z = w1x1 + w2x2 + w3x3 + b
        y = 1 / (1 + e^(-z))
    for b=1, w1=1, w2=1, w3=1, x1=1, x2=1, x3=1, => z = 3
        y = 1 / (1 + e^(-3)) = 0.9525741268224334
    which mean for z= 3 linear value, the sigmoid output is 0.95 which is very close to 1. So the probability of y being 1 is 0.95.</pre>

**Classification Model**:
Logistics regression tells you probablity in percentage whether a given email is spam or not. Classification tells you whether given email is spam or not instead of predicting the probability.
1. Binary Classification: https://github.com/pravinvarma/ML/blob/main/horseHuman.ipnyb
2. Multiclass Classification: https://github.com/pravinvarma/ML/blob/main/load-rps-model.ipynb

If we have probability of a given email to be spam say 0.50 then we need to define some threshhold for the clssification. The threshold then assigned to classes

1. Positive class(email is spam)
2. Negative class(email is not spam)

Depending on the outcome of classes,  we can have a matrix where columns are truths and rows are predictions which is called as **confusion matrix**.

|  | Actual Positive | Actual Negative |
| :---         |     :---      |      :--- |
| **Predicated Positive**  |   TP(spam is predicted correctly as spam   |  FP(not spam email is predicted as spam)  |
| **Predicted Negative**     |   FN(spam email is predicted as not spam)     | TN(not spam email is correctly predicted as not spam)    |

TP - True positive, the actual outcome is positive and predicated is also positive
FP - False positive, the actual outcome is positive while predicated is negative
FN - false negative, the actual prediction is positive while predicted is negative
TN - True negative, the actual outcome is negative and predicated is also negative

#### Accuracy, recall and precision,FPR

Suppose Dhanno received 10 emails in her inbox. Out of 10 emails, 2 are correctly identified as spam emails but 2 emails which were not spam identified as spam. So, we have following
TP(emails identified as spam which were actually spam): 2
FP(emails which were not actually spam but identified as spam): 2
So, these two emails falsely identified as spam will become
FN(emails identified as spam which were not actually spam): 2
So these becomes total 6. Which mean remaining 4 were TN(not identified as spam)

Formulae:
1. Accuracy = TP + TN/ TP+TN+FP+FN
2. recall(True positive rate) = TP/ TP+FN(How many actual span were caught)
3. precision = TP/TP+FP
4. FPR = FP/FP+TN(how many not spam emails wrongly flagged)

So, in our example,
1. Accuracy = 2+4/2+4+2+2=0.5. So the accuracy is 50%
2. Recall = 2/2+2=0.5, which means model found half of the spam email.
3. Precision = 2/2+2 = 0.5 which mean half of the spam prediction is correct
4. FPR = 2/2+4=0.3 which means 33% were wrongly flagged as spam
