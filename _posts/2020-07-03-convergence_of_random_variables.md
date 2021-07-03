# Convergence of Random Variables


## Introduction

There are two main ideas in this article.

Law of Large Numbers:
This states that the mean of the sample {\overline{X}_n} converges in probability to the distribution mean {\mu} as {n} increases.

Central Limit Theorem:
This states that the distribution of the sample mean converges in distribution to a normal distribution as {n} increases.

## Types of Convergence

Let {X_1, \dotsc, X_n} be a sequence of random variables with distributions {F_n} and let {X} be a random variable with distribution {F}.

Definition 1 Convergence in Probability: {X_n} converges to {X} in probability, written as {X_n \overset{P}{\longrightarrow} X}, if for every {\epsilon > 0}, we have

\displaystyle \mathbb{P}(|X_n - X| > \epsilon) \rightarrow 0 \ \ \ \ \ (1)

as {n \rightarrow \infty}.

    Definition 2 Convergence in Distribution: {X_n} converges to {X} in distribution, written as {X_n \rightsquigarrow X}, if

    \displaystyle \underset{n \rightarrow \infty}{\text{lim}} F_n(t) = F(t) \ \ \ \ \ (2)

    at all {t} for which {F} is continuous. 

3. The Law of Large Numbers

Let {X_1, X_2, \dotsc} be \textsc{iid} with mean {\mu = \mathbb{E}(X_1)} and variance {\sigma^2 = \mathbb{V}(X_1)}. Let sample mean be defined as {\overline{X}_n = (1/n)\sum_{i=1}^n X_i}. It can be shown that {\mathbb{E}(\overline{X}_n) = \mu} and {\mathbb{V}(\overline{X}_n) = \sigma^2/n}.

    Theorem 3 Weak Law of Large Numbers: If {X_1, \dotsc, X_n} are \textsc{iid} random variables, then {\overline{X}_n \overset{P}{\longrightarrow} \mu}. 

4. The Central Limit Theorem

The law of large numbers says that the distribution of the sample mean, {\overline{X}_n}, piles up near the true distribution mean, {\mu}. The central limit theorem further adds that the distribution of the sample mean approaches a Normal distribution as n gets large. It even gives the mean and the variance of the normal distribution.

    Theorem 4 The Central Limit Theorem: Let {X_1, \dotsc, X_n} be \textsc{iid} random variables with mean {\mu} and standard deviation {\sigma}. Let sample mean be defined as {\overline{X}_n = (1/n)\sum_{i=1}^n X_i}. Then the asymptotic behaviour of the distribution of the sample mean is given by

    \displaystyle Z_n = \frac{ (\overline{X}_n - \mu) } { \sqrt{ \mathbb{V}( \overline{X}_n ) } } = \frac{ \sqrt{n}(\overline{X}_n - \mu) } { \sigma } \rightsquigarrow N(0,1) \ \ \ \ \ (3)

The other ways of expressing the above equation are

\displaystyle Z_n \approx N(0, 1) \\ \overline{X}_n \approx N\left(\mu, \frac{\sigma^2}{n}\right) \\ (\overline{X}_n - \mu) \approx N(0, \sigma^2/n) \\ \sqrt{n}(\overline{X}_n - \mu) \approx N(0,\sigma^2) \\ \frac{\sqrt{n}(\overline{X}_n - \mu)}{\sigma} \approx N(0,1). \ \ \ \ \ (4)

    Definition 5 As has been defined in the Expectation chapter, if {X_1, \dotsc, X_n} are random variables, then we define the sample variance as

    \displaystyle S_n^2 = \frac{1}{n - 1}\left(\sum_{i=1}^n (\overline{X}_n - X_i)^2\right). \ \ \ \ \ (5)

    Theorem 6 Assuming the conditions of the CLT,

    \displaystyle \frac{\sqrt{n}(\overline{X}_n - \mu)}{S_n} \approx N(0,1). \ \ \ \ \ (6)

# The Delta Method

    Theorem 7 Let {Y_n} be a random variable with conditions of CLT met, and let {g(x)} be a differentiable function with {g'(\mu) \neq 0}. Then,

    \displaystyle Y_n \approx N\left(\mu, \frac{\sigma^2}{n}\right) \\ \Longrightarrow \quad g(Y_n) \approx N\left(g(\mu), (g'(\mu))^2\frac{\sigma^2}{n}\right). \ \ \ \ \ (7)

