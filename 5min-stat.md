# This Repo is dedicated for the reading notes of [Five Minute Stats](https://stephens999.github.io/fiveMinuteStats/)


1. For the likelihood ration of Model M1 vs Model M0 for discrete random variable X, it is naturally to put the PMF function of the given observation into the computation. When the variable X is continuous, we can use the ratio of the model densities of X as an approximation. However, it has the assumption that the pdf function are constant within the neighborhood of x that has radius equal to the measurement precision. 

2. LR: likelihood ratio can only reveal the relative strenth of the two candidate models. For example, LR(M0, M1)=0 only shows that M0 is favored over M1. We can not say that M0 is true.

3. Compared to LR: posterior odds will be more informative. It will be computed as Posterior odds = prior odds * LR. The **prior odds** of an event E1 and E2 means the ratio of their probabilities such as Pr(zi=1)/Pr(zi=0)

4. **Simple hypothesis** vs **Composite hypothesis**:  the hypotheses completetly specify the probability distributions while the composite one does not. For example, one hypothesis is the mean of a normal distribution is one constant and another hypothesis is the mean of the normal distribution is larger than the constant. That will be the simple verse composite.

5. Maximum likelihood estimation is based on independent and identically distributed (i.i.d) data from a model.
<p align="center">
<img src="https://render.githubusercontent.com/render/math?math=\theta \sim N(\theta_0, I_n(\theta_0)^{-1}">
 </p>
where the precision (inverse variance) or Fisher information is defined as 
<p align="center">
<img src="https://render.githubusercontent.com/render/math?math=I_n(\theta_0)=E_{\theta_0}[-\frac{d^2}{d\theta^2}l(\theta,X_1,..,X_n)]">
  </p>

* The negative second deriviative measures the curvature of a function or how peaked the likelihood function is. The more peaked the likelihood function, the more information it contains, and the more precise the MLE will be. 
* the expectation in the definition of In is with respect to the distribution of X1, X2, Xn, p(x1, x2,..,xn|θ)

For i.i.d. data the Fisher information In(θ)=nI(θ) and so increases linearly with n (see notes above). Consequently the variance decreases linearly with n and the RMSE decreases with n0.5. Thus, for example, to halve the RMSE we need to multiply sample size by 4. The I(θ) is the fisher information for a single observation

6. Bayes stat. is trying to solve the posterior probability.  Here, sometimes, you will find the result is the density of a distribution you recongize. While in the majority cases, we can only use computational methods to compute quantities of interest. Given a posterior distribution,  we can do interval estimates and point estimates. 

* Interval estimates can be obtained by computing quantiles of the posterior distribution.
* Point estimates are typically obtained by computing the mean or median or mode of the posterior distribution. 

<p align="center">
<img src="https://render.githubusercontent.com/render/math?math=\int\theta{p(\theta|x)}d\theta">
  </p>

7. posterior ~ liklihood * prior, or p(q|D) ~ p(D|q)p(q).  For conjugate priors, it means p(q) has the similar form with p(q|D). 

Some examples: 
* Gamma distribution is the conjugate prior for a Poisson mean.
* The Beta distribution is the conjugate prior for a binomial proportion

8. The posterior distribution on θ1 and θ2 factorizes into independent parts p(θ1|D1) and p(θ2|D2). Here, we say θ1 and θ2 are posteriori independent. 

<p align="center">
<img src="https://render.githubusercontent.com/render/math?math=p(\theta_1,\theta_2|D_1, D_2) \sim  p(D_1|\theta_1)p(\theta_1)p(D_2|\theta_2)p(\theta_2)">
  </p>

9.

Expected Loss (Integrated Risk): after applying the decision rule to a series of (X,Y) pairs coming from some prob. distribution P(X,Y).

<p align="center">
<img src="https://render.githubusercontent.com/render/math?math={\int}{\int}L(\tilde{Y}(X), Y)p(X,Y)dXdY">
  </p>

The optimal decision rule: for each X select the prediction that minimizes the conditional expected loss:

<p align="center">
<img src="https://render.githubusercontent.com/render/math?math={argmin}_a{\int}L(a, Y)p(Y|X)dY">
  </p>
  
For squared loss, it will be conditional mean given X: E(Y|X).

For absolute loss, it will be the median of the conditional distribution of P(Y|X)

