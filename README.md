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
1. Binary Classification: https://github.com/pravinvarma/ML/blob/main/horseHuman.ipnyb
2. Multiclass Classification: https://github.com/pravinvarma/ML/blob/main/load-rps-model.ipynb
