# Lecture 1
## Introduction
* What is computer vision?
    * Teaching computers to see
* What is it used for?
    * Object detection
    * Object recognition
    * Robotics
    * Event detection
    * Gesture recognition
    * 3D reconstruction
        * Stereoscopic vision
    * Augmented Reality
    * Generative Adverserial network
    * Discriptive Models
    * Shape models
* Kinfu - 3D scene generator 
* Deep Learning
    * Given raw data
    * Lots of layers

# Computer Vision: models, learning and inference
Introduction to Probability

# Random Variables
* A random variable $x$  denotes a quantity that is uncertain
* A variable that can take on a random value in *some* range
  * The value of the variable is uncertain
* If observe several instances of $x$ we get different values
* Some values occur more than others and this information is captured by a probability distribution (PD)
* Probability is the relevant propensity of an even happening

# Discrete Random Variables
* Discrete but unordered variable - colour
* Can represent them with bar graph/histogram etc

# Continuous Random Variables
* Normal distribution
* Think in terms of standard deviations

> Some proportion of the population sits within a *standard deviation* of the mean

# Joint Probability
* Consider two random variables $x$ and $y$

# Marginalization
We can recover probability distribution of ny variable in a joint distribution by integrating (or summing) over the other variables.

To marginalise out $y$ we integrate over $y$, to marginalise out $x$ we integrate over $x$.

# Conditional Probability
* Conditional probability of $x$ given that..

If we know something about one variable, its likely that it can tell us something about another variable. 

The line $y_1$ is representative of a probability, but it does not represent the entire probability $Pr(x,y)$. 

$$Pr(x|y = y*) = \frac{Pr(x,y=y*)}{\int(Pr(x,y=y*)dx)} ...$$

## Bayes Rule Proof
$$P(x,y) = P(x|y)\cdot P(y) \\
P(x,y) = P(y,x) \cdot P(x)\\
P(x,y)\cdot P(y) = P(y|x)\cdot P(x)\\
P(x,y) = \frac{P(y|x)\cdot P(x)}{P(y)}\\
= \frac{P(y|x)\cdot{(x)}}{\int P(x,y)dx}
= \frac{P(y|x)\cdot P(x)}{}
$$

## Bayes Rule Terminology
prior allows us to build in previous knowledge into a model.

# Independenec
Two variables are independent then variable x tells us nothing about variable y. 

# Expectation
Fancy weighted average based on probability 

## Rules
Expectation of the product is the same as the product of the expectation (if they are independent)


## Tutorial Questions
From the textbook:
Chapter 2: 1,2,3,4,6,7,8,9,10 - everything except 5
Chapter 3: 1,2,3,6,8,9,10,11 - 4 if you feel like it, 12 will make you sad

Hint, completing the square! 

# Computer Vision: Models, learning and inference
Common Probability Distributions

Copy that sweet sweet table

Positive definite - normal inverse Wishart 

Normal-scaled inverse gamma, can allow one to sample distributions over distribution. For instance, a mean and a variance. 

## Beta Distribution
$\Gamma$ function - not going to ask us to derive it, but it is the continuous version of a factorial. Try to do it by integration by parts 

You can set alpha and beta or you can find them. This is a distribution that covers the Bernoulli distribution. Coin could be in the center, and then could be biased left or right. 

The Bernoulli distribution and the Beta distribution both share $\mathbf{\lambda}$

## Categorical Distribution
Instead of two categories there can be as many as we want. All the lambdas disappear instead of the one we are talking about.

$$ Pr(x) = Cat_x[\lambda]$$

All the $\lambda$s must be between 0 and 1

## Dirichlet Distribution
Does for the categorical, what the Beta does for Bernoulli. $\Gamma$ of the sum, over the sum of the $\Gamma$s. 

$$P(\lambda_1, \lambda_2, ..., \lambda_k) = \Gamma[\sum_\infin]$$

There is a part of the distribution that we use, and everything else is there to normalise it to $1$. 

$$Dir_{\lambda_1,...,k}[\alpha_1,\alpha_2,\alpha_3,...,\alpha_k]$$

Dirichlet is the generalised form of beta

## Univariate Normal Distribution
Its basically a sad parabola. Mean moves it around, variance stretches it

## Normal Inverse Gamma Distribution
We have a probability distribution over the norm and variance. 

We can draw normal distribution form here, we have a term that depends on the mean and variance and a term that nullifies it. 

We can sample and variance from the normal inverse gamma distribution . Has the four parameters: $\alpha, \beta, \gamma,  \delta$

$\gamma$ - how close we expect to be to the expected mean

We have a distribution over the normal distribution, we can sample normal distributions from this

## Multivariate Normal Distribution
Exactly the same as the normal distribution but we have matrices instead. Multi-dimensional parabola.

Still a sad parabola. 

We have a mean vector and some covariance around it.

## Types of Covariance
Covariance matrix has three forms, termed spherical, diagonal and full. 

## Normal Inverse Wishart
Never expect us to do any maths for this. Don't worry about it, but know that it is effectively the same comparison. 

We use the normal inverse wishart for the multivariate normal distribution. 

The important thing is that there are parameters, that tell us where we expect the mean to be and how much we expect it to move. 

Defined on two variables: a mean vector $\mu$ ad a symmetric positive definite matrix, $\Sigma$

$\gamma$ tells us how far from the expected mean we are allowed to get.

Just know that there are parameters to tell us where we expect to find the mean and how much it can move.

# Conjugancy
* Two distributions with Bayes give us the same probability as before