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

Q: Why and when do Best subset selection and forward/backward stepwise selection lead to different models
A: Best subset selection considers all possible feature combinations and hence may have better model vs stepwise selection in case there's multicolinearity among the features. 

Q: Why do RSS & R2 always improve when we add more features
A: RSS & R2 are metrics based on training data, hence will always improve on feature addition as the fit gets better. Hence, we want to use error based on training data not test data 

Q: What does it mean for an experiment to be underpowered, Does this mean that a small sample leads to a “conservative” evaluation of the treatment effect?
A: No, If your sample gets really small, your chance of discovering effects that aren’t really there goes up!. Intuition: random noise in the data leads to more chance differences in small samples.

Q: In Matching, why use Matching - why not just control for the confounders ?
A: The number of confounds might also be large relative to the number of observations we have (= low statistical power).
This also assumes that the income and GPA impact years in school, as well as Scholarship, linearly. What if they do not? Perhaps there is an income cutoff, for example.
Linear regression with controls yields a model that will extrapolate to unobserved units. For example, you might never observe an individual who had a GPA > 3.9 and median income < 20,000 at the same time in your data, but your model will still extrapolate to that non-existent person. This is possible because of the linear additivity assumptions the model is enforcing.- Matching on covariates means you focus on a local sub-population, and no extrapolation can happen.
An advantage of coarsened exact matching over simply controlling for things is that matching requires no functional assumptions, i.e., you get away from model dependence in your findings. Depending on what controls you include in a typical regression model, your estimates will change… matching gets away from this.

