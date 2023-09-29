# Motivation for Bayesian statistics
Before we begin our adventure on learning Bayesian Statistics, it's worth exploring some of the content we know of thus far as this will motivate our study of this subject.  It's also worth brushing up on your probability and mathematics skills, such as:
- Separating derivatives and integrals
- Probability distributions
- Transformations of random variables
- Calculating probabilities and obtaining probabilities from integrals (CDFs)

So far, I am assuming you have covered:
- Hypothesis tests, p-values
- Confidence intervals
- Unbiased estimators, MSE

These topics are from the "Frequentist" approach to statistics. To find an estimator of interest, for example, the average weight (kg) of the UK population, we would find the Maximum Likelihood Estimator ([MLE](https://en.wikipedia.org/wiki/Maximum_likelihood_estimation)) of our sampling distribution. Following our estimation, we would calculate the mean, variance and confidence intervals of our estimate. This is known as *statistical inference*.

However, there are some problems with this approach. A [2015 study published in nature](https://www.nature.com/articles/nmeth.3288#:~:text=P%20values%20are%20only%20as,features%20of%20that%20population21.) stated that the p-values (that is, the probability of obtaining the observed data assuming the null hypothesis to be true) "*p-values are only as as reliable as the sample from which they have been calculated*". In other words, if your sampling distribution was obtained from a small sample size or if there were any problems with the sampling method (such as unintentional bias being introduced), your p-values are suspect! This presents another problem: reproducibility.  If you have to design experiments extremely carefully and plan it properly or resort to "hacky" methods like using very high alpha values, you reduce the ease of reproducibility. If an experiment is difficult to replicate then how can we validate our results? This can block scientific progress and discoveries.

### Are there any alternatives?
Fortunately, Bayesian Statistics offers a solution to the woe's of Frequentist statistics. Its approach differs but in a perfect world, but approaches should result to the same conclusion. Bayesian statistics focuses on:
- **Subjective probability:** Instead of having a sampling distribution of the statistic given some parameter, bayesian statistics considers a *probability distribution* of the parameter given the statistic, which allows us to quantify the uncertainty about the quantity of interest.
- **Bayes theorem:** The core of Bayesian Statistics. In a nutshell, it is a formula that links our "guess" of the parameter with our data or information, generating an output with a "new guess". We'll explore this in more depth later.

## Subjective Probability - Frequentist approach
if, in an sequence of $n$ independent trials an event $E$ occurs $r(n)$ times, then $\frac{r(n)}{n}$ converges to $P[E]$ as $n \rightarrow \infty$.

In order to satisfy the above statement, any trail under which the event $E$ occurs **must** be repeatable.

## Subjective Probability - Bayesian approach
$P[E]$ is defined as an **individual's degree of belief** in the likelihood of $E$ occurring (or being true), on a scale of 0 (certain not to occur) to 1 (certain to occur).

In other words, the probability we assign to any event is based on our belief, not on objectivity! For example, I might believe the chance of me winning the lottery is 50%, but you may say it's only 0.00001%! This is an important concept to understand for bayesian statistics. Our models change depending on our belief and this ties in to Bayes theorem. Bayes theorem is used as a way of updating our guesses of the parameter based on newly acquired information. However, the initial guess we make is **subjective**! Of course, this can lead you to taking a longer or shorter time to converging towards the population value parameter or not all!

Any points to keep in mind:
- Frequentist probabilities can only be stated for repeatable events. Subjective probabilities can be stated for *any* uncertain event
- All applied statistics involve subjective judgement

## Constructing subjective probabilities
How can we measure the probability of an event occurring, $P[E] \preceq$? 


