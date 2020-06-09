# Interesting-Stat-Ques
Loosely built collection of light bulb moments when revising stats

Q: When to use Paired T-test vs Two Sample T-test

Q: When comparing the means of several populations, why use ANOVA when we can use set of paired wise T-test
A: Because the power of the test will decrease

Q: When & why do we use Normal to approximate Binomial 

Q: In multiple linear regression, given these  p-values for each variable, it seems likely that if any one of the p-values for the individual variables is very small, then at least one of the predictors is related to the response<br>
A: This logic is flawed, especially when the number of predictors p is large. For instance, consider an example in which p = 100 and H0 : β1 = β2 = . . . = βp = 0 is true, so no variable is truly associated with the response. In this situation, about 5 % of the p-values associated with each variable (of the type shown in Table 3.4) will be below 0.05 by chance. In other words, we expect to see approximately five small p-values even in the absence of any true association between the predictors and the response. In fact, we are almost guaranteed that we will observe at least one p-value below 0.05 by chance! Hence, if we use the individual t-statistics and associated pvalues in order to decide whether or not there is any association between the variables and the response, there is a very high chance that we will incorrectly conclude that there is a relationship. However, the F-statistic does not suffer from this problem because it adjusts for the number of predictors. Hence, if H0 is true, there is only a 5 % chance that the Fstatistic will result in a p-value below 0.05, regardless of the number of predictors or the number of observations.

Q: Why not use the same cost functoin for Logistic Regression and Linear Regression A: The sum of square errors formula when substituted with Sigmaoid function, becomes non-convex. Hence, the function is not garnteed to reach global minima during gradient descent because there would be numerous local minima

Q: Difference between Min-Max & Z-Score scalling from application perspective 

Q: Normalization in Linear/Logistic regression ?

Q:What are posterior probabilities and prior probabilities?
https://www.statisticshowto.com/posterior-distribution-probability/

Q: L2 vs L1
https://www.kaggle.com/residentmario/l1-norms-versus-l2-norms

Q: Specifisit vs Sensitivity 
https://en.wikipedia.org/wiki/Sensitivity_and_specificity

Q: Why and when do Best subset selection and forward/backward stepwise selection lead to different models
A: Best subset selection considers all possible feature combinations and hence may have better model vs stepwise selection in case there's multicolinearity among the features. 

Q: Why do RSS & R2 always improve when we add more features
A: RSS & R2 are metrics based on training data, hence will always improve on feature addition as the fit gets better. Hence, we want to use error based on training data not test data 
