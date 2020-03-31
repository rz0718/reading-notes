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
The negative second deriviative measures the curvature of a function or how peaked the likelihood function is. The more peaked the likelihood function, the more information it contains, and the more precise the MLE will be. 
