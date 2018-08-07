# Exercises

1. Given historic observations `x1, x2, ..., xn`, prove that the prediction `y = average(x1, x2, ..., xn)` will minimize the RMSE error metric.

    For example, if `[x1, x2, x3] = [1, 2, 6]`, then your best prediction is `y = 3` as that leads to a minimum `RMSE = 2.16`, as can [be seen here](https://www.desmos.com/calculator/98cfi3mcka). 

2.  Given historic observations `x1, x2, ..., xn`, prove that the prediction `y = median(x1, x2, ..., xn)` will minimize the MAE error metric.

    With the same data as in question 1, `y = 2` leads to a minimum `MAE = 1.66`, as can [be seen here](https://www.desmos.com/calculator/mhhbextqkk).

3. The python notebook pi_monte_carlo.ipynb has all the code to calculate `Pi` using the monte carlo algorithm, and to calculate the spread in the output as a function of sample size. Using that notebook as the starting point, calculate the 95% confidence interval within which the `Pi` value will lie within if we used 1000 samples to calculate `Pi`.

4. Let's build some intuition for what kind of values pass statistical significance tests for A/B test results. In the table below, I have listed some sets of values, which contain visitor and conversion counts for Test A and Test B. Using an online A/B test significance calculator ([like this one](https://abtestguide.com/calc/)), check every row if the test results are statistically significant.

    | id  | Visitors Test A | Conversions Test A | Visitors Test B | Conversions Test B | Note |
    | --- | --- | --- | --- | --- | --- | 
    | 1 | 10 | 1 | 10 | 2 | 100% improvement |
    | 2 | 10 | 1 | 10 | 4 | 300% improvement |
    | 3 | 100 | 10 | 100 | 15 | 50% improvement |
    | 4 | 100 | 10 | 100 | 19 | 90% improvement |
    | 5 | 10,000 | 1,000 | 10,000 | 1,075 | 7.5% improvement |
    | 6 | 10,000 | 100 | 10,000 | 120 | 20% improvement |
    | 7 | 1,000,000 | 10,000 | 1,000,000 | 10,250 | 2.5% improvement |


In the following two exercises, we build machine learning models using real life data. The exercises are partially worked out, though, and the part where we read the data and build the model is already implemented. The goal for these exercises is to understand the concepts of **Curse of Dimensionality** and **Training vs. Test Error correlation** using practical models.

5. In this exercise, we train a model to classify email spam. In the python notebook spam_naive_bayes.ipynb, I have taken a spam database found online, and trained a Naive Bayes model to classify spam that uses all 57 features in the dataset. Your exercise is to modify the dataset to include fewer features and see the relationship between number of features and the accuracy of the model. The goal is to examine if the accuracy of the model improves as we include more features, and if the **Curse of Dimensionality** hurts the accuracy of the model when we use too many features.

6. This exercise illustrates how reducing training error doesn't necessarily reduce test error. We build a model to predict the price of a house given certain features of the house, like area and number of bedrooms. We build linear and higher degree polynomial models, and examine how the training error and test error vary as we increase the degree of our polynomial model from 1 to 5.


 
 