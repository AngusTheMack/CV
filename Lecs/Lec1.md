# Computer Vision: models, learning and inference
Chapter 3 - Common Probability Distributions
## Recap
* Bernoulli Distribution
  * True or False
  * Can be modelled with a Beta Distribution
* Categorical
  * As many categories as you want
  *  We can model the parameters with the Dirichlet distribution

Be comfortable with sampling parameters from another distribution.

## Why these specifc distributions?
* They have a very important quality, conjugancy

# Conjugate Distributions
* THe pairs of distributions discussed have a special relationship: they are conjugate distributions
  * Beta is conjugate to Bernoulli
  * Dirichlet is conjugate to categorical
  * Normal inverse gamma is conjugate to univariate normal
  * Normal inverse Wishart is conjugate to multivariate normal 
* When we take product of distribution and it's conjugate, the result has the same form as the conjugate
* For example:

$$
\operatorname{Pr}(x)=\operatorname{Bern}_{x}[\lambda]
$$

$$
\operatorname{Pr}(\lambda)=\operatorname{Beta}_{\lambda}[\alpha, \beta]*
$$


$$ P(x|\lambda)P(\lambda) \\
= Bern_x[\lambda]$$
 Some crazy maths

 * We can actually marginalise a second time
   * By using a prior that goes over the parameters
   * This is called bayesian inference
   * $\kappa(X,Y,x*)* P(...)d\theta$
   * Integrate over all possible parameters

* One distribution is conjugate to another distribution
* Will have the same shape as the conjugate, Bern * Beta is a constant * Beta.
* Constant can get pulled out 
* They are i

# Chapter 4 - Fitting Probability Models
We can have a belief about the world, we can observe something in the world, and then incorporate that observation into our prior.

We started off with our belief encoded in $\alpha$ and $\beta$. 

# Structure
* Fitting probability distributions
  * Maximum likelihood (ML)
    * argmax over mean and variance
    * $P(x_i...I|\mu, \sigma^2)$
    * Find the model that maximises $P(x_{i ... I}|\mu, \sigma^2)$
    * Fitting the model
  * Maximum a posteriori (MAP)
    * find the parameters that are most likely given our data 
    * $P(\mu,\sigma^2|...)$
    * Fitting the model with a prior
    * $P(\mu,\sigma^2|x_{i...I}) = P(x_{i...I}|\mu,\sigma^2)\cdot P(\mu,\sigma^2)$
    * Maximise the posterior of bayes rule, the denominator is not a function of that so we can ignore that 
  * Bayesian Approach

# Maximum Likelihood
Fittin: As the name suggests: find the parameters under which the data $X_{1...I}$ are most likely:
$$
\hat{\theta} = argmax_0[Pr(x_{1...I}|\theta)]
= argmax_0[]
$$

We have assumed that data was independent (hence product)

## Predictive Density
Evaluate new data point $x*$ under probability distribution $Pr(x*|\theta)$

# Maximum A Posteriori (MAP)
Fitting
As the name suggests, we find parameters which maximize the posterior probability

# Bayesian Approach
## Fitting
Computer the posterior distribution over possible parameter values using Bayes' rule

Pr()

Principle: why pick one set of parameters? There are many values that could have explained the data. Try to capture all of the possibilities. 

## PRedictive Density
* Each possible parameter value makes a prediction
* Some parameters more probable than others

$$ 

$$

# Predictive Densities for 3 Methods
* How to rationalize different forms?
* Consider ML and MAP estimates as probability distributions with zero probability everywhere except at estimates (i.e. delta functions)

* Delta function, value is 0 everywhere, but the integral over a thin slice goes to 1.

# Univariate Normal Distribution
* We use the inverse gamma to model the univariate normal distribution
* The $sigma$ value is the mean we expect for our prior. 
* $\prod^I_{\mu_i} Norm_x[\mu,\sigma^2]$
* We can take the log of this, in order to make it easier to differentiate. 
* $L = log(p) = log(\prod^I_{i=1}Norm_x[\mu,\sigma^2])$
* $=\sum^I_{i=1}log[Norm_x[\mu,\sigma^2]]$

$$
=\sum_{i=1}^I log(2\pi\sigma^2)^{-\frac{1}{2}}+\frac{-0.5(x-\mu)^2}{\sigma^2}
$$