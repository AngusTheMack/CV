# Computer Vision: models, learning and inference
## Fitting Probability Models
# Recap
* The conjugacy allows us to take integrals over the other distribution
* Maximum Likelihood
  * Find the parameters that make the data most likely
  * $\arg \max P(x_{1 ... I}|\Theta)$
* Maximum A Posteriori
  * Find the parameters that are most likely
  * $\arg \max P(\Theta|x_{1 ... I}) = \argmax_\Theta P(x_{1 ... I}|\Theta)P(\Theta)$
  * This gives us some $\hat{\Theta}$
  * $P(x^*|\hat{\Theta})$ - Predictive Density, the probability of some new data, given the parameters we have
  * $P(x^*|x_{1 ... I}) = \int P(x^*|\hat{\Theta}) P(\Theta | x_{1 ... I}d \Theta$
* Gaussian

# Maximum A Posteriori (MAP)
* Can only be done when the data was independent
* Can't use this for pixels, as they aren't independent
* **Fitting**
  * As the name suggests we find the parameters which maximize the posterior probability $Pr(\Theta|x_{1 ... I})$
$$
\begin{aligned}
\hat{\Theta} &= \argmax_\Theta[Pr(\Theta|x_{1...I})] \\
&= \argmax_\Theta[\frac{Pr(x_{1 ... I|\Theta})Pr(\Theta)}{}]
\end{aligned}
$$

# Bayesian Approach
Predictive Density
* Each Possible parameter value makes a prediction
* Some Parameters more probable than others
* E.g.: Door example, you can gu
# Notes
* These equations look very complex, but they are very simple for what we are doing. 
* Why not just use CNNs:
  * Sometimes you need a nuanced approach

# Why?
* We want to model something to do with the world, but make it depend on our data $x$. 
* $P(w | x)$
* We can now phrase linear and logistic regression within this new framework, do the maths and see how they work out.
  * ML will give us the equation we expect
  * MAP will give us the equation with some prior
  * Bayesian will give us the same thing but with some iterative update technique
* We can have the world which can be discrete or continuous, as well as our data which could be either. When they are both continuous it is regression, when it is discrete it is classification. 
* We can model some data that is contingent on the world state. We can model $P(x|w)$ which will be easier than modelling $P(w|x)$ - but how do we get from one to the other?
  * Bayes!
* We can model the joint probability of $P(x,w)$ - giving us a generative model for the world
$$
\frac{P(x|w)P(w)}{\int P(x|w)P(w)dw}
$$
# Exercise
* We have a bunch of coins on a table and a mask
* $w \in {0,1}$ - Bern
* $x \in \mathbb{R}$  - Norm
$$
P(w|x) = Bern_\lambda[sig[\theta \cdot x + \theta]]
$$
* What if we wanted a generative model
  * $P(x|w) = Norm_x[\mu_w,\sigma^2_w]$ - we can use this to give us the mean of the coins, mean of the desk
  * $P(w) = Bern_w[\lambda]$
* Probability of a coin, given the values:
$$\begin{aligned}P(w=1|x) &= \frac{P(x|w=1)P(w=1)}{\sum_{i=0}^1P(x|w=i)P(w=i)}\\ &= \frac{Norm_x[\mu_c,\sigma_c^2]\cdot \lambda}{(1-\lambda)\cdot Norm_x[\mu_d,\sigma_d^2]+\lambda\cdot Norm_x[\mu_c,\sigma_c^2]}\\ &= \frac{N_c}{N_c+N_d}\end{aligned}$$

# Homework:
* Everything except 4.5, 4.6 for tutorial