# Interesting-Stat-Ques
Loosely built collection of light bulb moments when revising stats

Q: When to use Paired T-test vs Two Sample T-test

Q: When comparing the means of several populations, why use ANOVA when we can use set of paired wise T-test
A: Because the power of the test will decrease

Q: When & why do we use Normal to approximate Binomial 

Q: In multiple linear regression, given these  p-values for each variable, it seems likely that if any one of the p-values for the individual variables is very small, then at least one of the predictors is related to the response
A: This logic is flawed, especially when the number of predictors p is large. For instance, consider an example in which p = 100 and H0 : β1 = β2 = . . . = βp = 0 is true, so no variable is truly associated with the response. In this situation, about 5 % of the p-values associated with each variable (of the type shown in Table 3.4) will be below 0.05 by chance. In other words, we expect to see approximately five small p-values even in the absence of any true association between the predictors and the response. In fact, we are almost guaranteed that we will observe at least one p-value below 0.05 by chance! Hence, if we use the individual t-statistics and associated pvalues in order to decide whether or not there is any association between the variables and the response, there is a very high chance that we will incorrectly conclude that there is a relationship. However, the F-statistic does not suffer from this problem because it adjusts for the number of predictors. Hence, if H0 is true, there is only a 5 % chance that the Fstatistic will result in a p-value below 0.05, regardless of the number of predictors or the number of observations.
