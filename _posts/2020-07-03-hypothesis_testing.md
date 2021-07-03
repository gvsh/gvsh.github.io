# Hypothesis Testing and p-values

# Hypothesis Testing and p-values


## Introduction

Hypothesis testing is a method of inference.

Definition 1:
A hypothesis is a statement about a population parameter.

Definition 2:
Null and Alternate Hypothesis:
We partition the parameter space $\Theta$ into two disjoint sets $\Theta_0$ and $\Theta_1$ and we wish to test:

$$
\displaystyle H_0 \colon \theta \in \Theta_0 \\ H_1 \colon \theta \in \Theta_1. \ \ \ \ \ (1)
$$



We call $H_0$ the null hypothesis and $H_1$ the alternate hypothesis. 

Definition 3 Rejection Region: Let $X$ be a random variable and let $\mathcal{X}$ be its range. Let $R \subset \mathcal{X}$ be the rejection region.

We accept $H_0$ when $X$ does not belong to $R$ and reject when it does. 

Hypothesis testing is a legal trial. We accept $H_0$ unless the evidence suggests otherwise. Falsely sentencing the accused when he is not guilty is type I error and letting the accused go free when he is infact guilty is a type II error.

Definition 4 
Power Function of a Test: It is the probability of $X$ being in the rejection region, expressed as a function of $\theta$.

$$
\displaystyle \beta(\theta) = \mathbb{P}_{\theta}(X \in R) \ \ \ \ \ (2)
$$

Definition 5 
Size of a Test: It is the maximum of the power function of a test when $\theta$ is restricted to the $\Theta_0$ parameter space.

$$
\displaystyle \alpha = \underset{\theta \in \Theta_0}{\text{sup}}(\beta(\theta)). \ \ \ \ \ (3)
$$

Definition 6 
Level $\alpha$ Test: A test with size less than or equal to $\alpha$ is said to be a level $\alpha$ test. 

Definition 7 
Simple Hypothesis: A hypothesis of the form $\theta = \theta_0$ is called a simple hypothesis. 

Definition 8 
Composite Hypothesis: A hypothesis of the form $\theta < \theta_0$ or $\theta > \theta_0$ is called a composite hypothesis. 

Definition 9 
Two Sided Test: A test of the form

$$
\displaystyle H_0 \colon \theta = \theta_0 \\ H_1 \colon \theta \neq \theta_0. \ \ \ \ \ (4)
$$

is called a two-sided test. 

Definition 10 
One Sided Test: A test of the form

$$
\displaystyle H_0 \colon \theta < \theta_0 \\ H_1 \colon \theta > \theta_0. \ \ \ \ \ (5)
$$

or

$$
\displaystyle H_0 \colon \theta > \theta_0 \\ H_1 \colon \theta < \theta_0. \ \ \ \ \ (6)
$$

is called a one-sided test. 

Example 1 
Hypothesis Testing on Normal Distribution: 
Let $X_1, \dotsc, X_n \sim N(\mu, \sigma^2)$ where $\sigma$ is known. We want to test $H_0 \colon \mu \leq 0$ versus $H_1 \colon \mu > 0$. Hence $\Theta_0 = (- \infty, 0]$ and $\Theta_1 = ( 0, \infty)$.

Consider the test:

$$
\displaystyle \text{reject } H_0 \text{ if } T > c \ \ \ \ \ (7)
$$

where $T = \overline{X}$.

Then the rejection region is

$$
\displaystyle R = \{(x_1, \dotsc, x_n) : \overline{X} > c \} \ \ \ \ \ (8)
$$

The power function of the test is

$$
\displaystyle \beta(\mu) = \mathbb{P}_{\mu}(X \in R) \\ = \mathbb{P}_{\mu}(\overline{X} > c) \\ = \mathbb{P}_{\mu}\left( \frac{\sqrt{n}(\overline{X} - \mu)}{\sigma} > \frac{\sqrt{n}(c - \mu)}{\sigma} \right) \\ = \mathbb{P}_{\mu}\left( Z > \frac{\sqrt{n}(c - \mu)}{\sigma} \right) \\ = 1 - \Phi\left(\frac{\sqrt{n}(c - \mu)}{\sigma}\right). \ \ \ \ \ (9)
$$

The size of the test is

$$
\displaystyle \text{size} = \underset{\mu \leq 0}{\text{sup}}(\beta(\mu)) \\ = \underset{\mu \leq 0}{\text{sup}}\left(1 - \Phi\left(\frac{\sqrt{n}(c - \mu)}{\sigma}\right)\right) \\ = \beta(0) \\ = 1 - \Phi\left(\frac{c\sqrt{n}}{\sigma}\right). \ \ \ \ \ (10)
$$

Equating with $\alpha$ we obtain

$$
\displaystyle \alpha = 1 - \Phi\left(\frac{c\sqrt{n}}{\sigma}\right). \ \ \ \ \ (11)
$$

Hence

$$
\displaystyle c = \frac{\sigma \thinspace \Phi^{-1}(1 - \alpha)}{\sqrt{n}}. \ \ \ \ \ (12)
$$

We reject when $\overline{X} > c$. For a test size of 95%

$$
\displaystyle c = \frac{1.96 \sigma}{\sqrt{n}}. \ \ \ \ \ (13)
$$

or we reject when

$$
\displaystyle \overline{X} > \frac{1.96 \sigma}{\sqrt{n}}. \ \ \ \ \ (14)
$$

2. The Wald Test

Let $X_1, \dotsc, X_n$ be \textsc{iid} random variables with $\theta$ as a parameter of their distribution function $F_X(x; \theta)$. Let $\hat{\theta}$ be the estimate of $\theta$ and let $\widehat{\textsf{se}}$ be the standard deviation of the distribution of $\hat{\theta}$.

Definition 11 (The Wald Test)

Consider testing a two-sided hypothesis:

$$
\displaystyle H_0 \colon \theta = \theta_0 \\ H_1 \colon \theta \neq \theta_0. \ \ \ \ \ (15)
$$

Assume that $\hat{\theta}$ has an asymptotically normal distribution.

$$
\displaystyle \frac{\hat { \theta } - \theta }{\widehat{\textsf{se}} } \rightsquigarrow N(0, 1). \ \ \ \ \ (16)
$$

Then, the size $\alpha$ the Wald Test is: reject $H_0$ if $|W| > z_{\alpha/2}$ where

$$
\displaystyle W = \frac{\hat { \theta } - \theta_0 }{\widehat{\textsf{se}}}. \ \ \ \ \ (17)
$$

Theorem 12 Asymptotically, the Wald test has size $\alpha$.

$$
\displaystyle size \\ = \underset{\theta \in \Theta_0}{\text{sup}}(\beta(\theta)) \\ = \underset{\theta \in \Theta_0}{\text{sup}}\mathbb{P}_{\theta}(X \in R) \\ = \mathbb{P}_{\theta_0}(X \in R) \\ = \mathbb{P}_{\theta_0}(|W| > z_{\alpha/2}) \\ = \mathbb{P}_{\theta_0}\left(\left| \frac{\hat { \theta } - \theta_0 }{\widehat{\textsf{se}}}\right| > z_{\alpha/2}\right) \\ \rightarrow \mathbb{P}(|Z| > z_{\alpha/2}) \\ = \alpha. \ \ \ \ \ (18)
$$

Example 2 Two experiments are conducted to test two prediction algorithms.

The prediction algorithms are used to predict the outcomes {n} and {m} times, respectively, and have a probability of predicting with success as {p_1} and {p_2}, respectively.

Let $\delta = p_1 - p_2$.

Consider testing a two-sided hypothesis:

$$
\displaystyle H_0 \colon \delta = 0 \\ H_1 \colon \delta \neq 0. \ \ \ \ \ (19)
$$

3. The Likelihood Ratio Test

This test can be used to test vector valued parameters as well.

Definition 13 The likelihood ratio test statistic for testing $H_0 \colon \theta \in \Theta_0$ versus $H_1 \colon \theta \in \Theta_1$ is

$$
\displaystyle \lambda(x) = \frac{ \underset{\theta \in \Theta_0}{\text{sup}} (L( \theta|\mathbf{x} )) }{ \underset{\theta \in \Theta}{\text{sup}} (L( \theta|\mathbf{x} )) }. \ \ \ \ \ (20)
$$

$$
\displaystyle W = \frac{\hat { \theta } - \theta_0 }{\widehat{\textsf{se}}}. \ \ \ \ \ (17)
$$

Theorem 12 Asymptotically, the Wald test has size $\alpha$.

$$
\displaystyle size \\ = \underset{\theta \in \Theta_0}{\text{sup}}(\beta(\theta)) \\ = \underset{\theta \in \Theta_0}{\text{sup}}\mathbb{P}_{\theta}(X \in R) \\ = \mathbb{P}_{\theta_0}(X \in R) \\ = \mathbb{P}_{\theta_0}(|W| > z_{\alpha/2}) \\ = \mathbb{P}_{\theta_0}\left(\left| \frac{\hat { \theta } - \theta_0 }{\widehat{\textsf{se}}}\right| > z_{\alpha/2}\right) \\ \rightarrow \mathbb{P}(|Z| > z_{\alpha/2}) \\ = \alpha. \ \ \ \ \ (18)
$$

Example 2 Two experiments are conducted to test two prediction algorithms.

The prediction algorithms are used to predict the outcomes $n$ and $m$ times, respectively, and have a probability of predicting with success as $p_1$ and $p_2$, respectively.

Let $\delta = p_1 - p_2$.

Consider testing a two-sided hypothesis:

$$
\displaystyle H_0 \colon \delta = 0 \\ H_1 \colon \delta \neq 0. \ \ \ \ \ (19)
$$

3. The Likelihood Ratio Test

This test can be used to test vector valued parameters as well.

Definition 13 The likelihood ratio test statistic for testing $H_0 \colon \theta \in \Theta_0$ versus $H_1 \colon \theta \in \Theta_1$ is

$$
\displaystyle \lambda(x) = \frac{ \underset{\theta \in \Theta_0}{\text{sup}} (L( \theta|\mathbf{x} )) }{ \underset{\theta \in \Theta}{\text{sup}} (L( \theta|\mathbf{x} )) }. \ \ \ \ \ (20)
$$

