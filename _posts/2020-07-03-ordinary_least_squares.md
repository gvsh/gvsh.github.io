# Ordinary Least Squares Under Standard Assumptions


Suppose that a scalar $y_t$ is related to a $(k \times 1)$ vector, $x_t$ and a disturbance term $u_t$ according to the regression model.

$$
\displaystyle y_t = x_t^T \beta + u_t \ \ \ \ \ (1)
$$

In this article, we will study the estimation and hypothesis testing of $\beta$ when $x_t$ is deterministic and $u_t$ is i.i.d. Gaussian.

## The Algebra of Linear Regression

Given a sample of T values of $y_t$ and the vector $x_t$, the ordinary least squares (OLS) estimate of $\beta$, denoted as $b$, is the value of $\beta$ which minimizes the residual sum of squares (RSS).

$$
\displaystyle RSS = \sum_{t=1}^T (y_t - x_t^T b)^2 \ \ \ \ \ (2)
$$

The OLS estimate of $\beta$, $b$, is given by:

$$
\displaystyle b = \bigg(\frac{1}{T}\sum_{t=1}^T x_tx_t^T \bigg)^{\!-1} \!\!\cdot\, \frac{1}{T}\sum_{t=1}^n x_ty_t. \ \ \ \ \ (3)
$$

The model is written in matrix notation as:


$$
\displaystyle y = X\beta + u. \ \ \ \ \ (4)
$$

$$
\displaystyle 
y= \begin{bmatrix} y_1 \\ y_2 \\ \vdots \\ y_T \end{bmatrix},
\quad X= \begin{bmatrix} x_1^T \\ x_2^T \\ \vdots \\ x_T^T \end{bmatrix},
\quad u= \begin{bmatrix} u_1 \\ u_2 \\ \vdots \\ u_T \end{bmatrix}. \ \ \ \ \ (5)
$$

where $y$ is a $T \times 1$ vector, $X$ is a $T \times k$ matrix, $\beta$ is a $k \times 1$ vector and $u$ is a $T \times 1$ vector.

Thus,

$$
\displaystyle b = (X^TX)^{-1}X^Ty. \ \ \ \ \ (6)
$$

Similarly,

$$
\displaystyle \hat u = y - Xb = y - X(X^TX)^{-1}X^Ty = [I_T - X(X^TX)^{-1}X^T]y = M_Xy. \ \ \ \ \ (7)
$$

where $M_X$ is defined as:

$$
\displaystyle M_X = [I_T - X(X^TX)^{-1}X^T]. \ \ \ \ \ (8)
$$

$M_X$ is a projection matrix. Hence it is symmetric and idempotent.

$$
\displaystyle M_X = M_X^T. \ \ \ \ \ (9)
$$

$$
\displaystyle M_XM_X = M_X. \ \ \ \ \ (10)
$$


Since $M_X$ is the projection matrix for the space orthogonal to $X},

$$
\displaystyle M_X^TX = M_XX = 0. \ \ \ \ \ (11)
$$

Thus, we can verify that the sample residuals are orthogonal to $X$.

$$
\displaystyle u^TX = y^TM_X^TX = 0. \ \ \ \ \ (12)
$$

The sample residual is constructed from the sample estimate of $\beta$ which is $b$. The population residual is a hypothetical construct based on the true population value of $\beta$.

$$
\displaystyle u_t = y_t - x_t^T \beta. \ \ \ \ \ (13)
$$

$$
\displaystyle \hat u_t = y_t - x_t^T b. \ \ \ \ \ (14)
$$

$$
\displaystyle \hat u = y - Xb = [I_T - X(X^TX)^{-1}X^T]y = M_Xy = M_XX b + u. \ \ \ \ \ (15)
$$

$$
\displaystyle b = (X^TX)^{-1}X^Ty = (X^TX)^{-1}X^T(X\beta + u) = \beta + (X^TX)^{-1}X^Tu. \ \ \ \ \ (16)
$$


The fit of OLS is described in terms of $R_u^2}, which is defined as the ratio of squares of the fitted values ({x_t^Tb)$ to the observed values of $y$.

$$
\displaystyle R_u^2 = \frac{\sum_{t=1}^T b^Tx_tx_t^Tb}{\sum_{t=1}^T y_t^2} = \frac{b^TX^TXb}{y^Ty}. \ \ \ \ \ (17)
$$


## Assumptions on X and u

We shall assume that

- X will be deterministic

- $u_t$ is i.i.d with mean 0 and variance $\sigma^2}.

- $u_t$ is Gaussian.

## Properties of Estimated $b$ Under Above Assumptions

Since,

$$
\displaystyle b = (X^TX)^{-1}X^Ty = (X^TX)^{-1}X^T(X\beta + u) = \beta + (X^TX)^{-1}X^Tu. \ \ \ \ \ (18)
$$

Taking expectations of both sides, we have,


$$
\displaystyle \mathop{\mathbb E}(b) = \beta + (X^TX)^{-1}X^T\mathop{\mathbb E}(u) = \beta. \ \ \ \ \ (19)
$$

And the variance covariance matrix is given by,

$$
\displaystyle \mathop{\mathbb E}[(b - \beta)(b - \beta)^T] = \mathop{\mathbb E}[((X^TX)^{-1}X^Tu)((X^TX)^{-1}X^Tu)^T] = \sigma^2(X^TX)^{-1}. \ \ \ \ \ (20)
$$

Thus b is unbiased and is a linear function of y.

## Distribution of Estimated b Under Above Assumptions

As u is Gaussian,

$$
\displaystyle b = \beta + (X^TX)^{-1}X^Tu. \ \ \ \ \ (21)
$$

implies that b is also Gaussian.

$$
\displaystyle b \sim N(\beta, \sigma^2(X^TX)^{-1}). \ \ \ \ \ (22)
$$

## Properties of Estimated Sample Variance Under Above Assumptions

The OLS estimate of variance of u, $\sigma^2$ is given by:

$$
\displaystyle s^2 = RSS / (T - k) = {\hat u}^T\hat u / (T - k) = u^TM_X^TM_Xu / (T - k) = u^TM_Xu / (T - k). \ \ \ \ \ (23)
$$

Since {M_X$ is a projection matrix and is symmetric and idempotent, it can be written as:

$$
\displaystyle M_X = P\Lambda P^T. \ \ \ \ \ (24)
$$

where

$$
\displaystyle P P^T = I_T. \ \ \ \ \ (25)
$$

and $\Lambda$ is a diagonal matrix with eigenvalues of $M_X$ on the diagonal.

Since,

$$
\displaystyle M_XX = 0. \ \ \ \ \ (26)
$$

that is, since the two spaces that they represent are orthogonal to each other, it follows that:

$$
\displaystyle M_Xv = 0. \ \ \ \ \ (27)
$$

whenever v is a column of X. Since we assume X to be of full rank, there are k such vectors and their eigenvalue is the right hand side, which is 0.

Also since

$$
\displaystyle M_X = I_T - X(X^TX)^{-1}X^T. \ \ \ \ \ (28)
$$

Thus, it follows that

$$
\displaystyle M_Xv = v. \ \ \ \ \ (29)
$$

whenever v is orthogonal to X. Since there are (T – k) such vectors, $M_X$ has (T – k) eigenvectors with eigenvalue 1.

Thus $\Lambda$ has k zeroes and (T – k) 1s on the diagonal.

$$
\displaystyle u^TM_Xu = u^TP\Lambda P^Tu. \ \ \ \ \ (30)
$$

Let

$$
\displaystyle w = P^Tu \ \ \ \ \ (31)
$$

Then,

$$
\displaystyle u^TM_Xu = u^TP\Lambda P^Tu = w^T\Lambda w = w_1^2 \lambda_1 + w_2^2 \lambda_2 + \dots + w_T^2 \lambda_T. \ \ \ \ \ (32)
$$

$$
\displaystyle u^TM_Xu = w_1^2 \lambda_1 + w_2^2 \lambda_2 + \dots + w_{T - k}^2 \lambda_{T - k}. \ \ \ \ \ (33)
$$

As these $\lambda}s are all unity, we have:

$$
\displaystyle u^TM_Xu = w_1^2 + w_2^2 + \dots + w_{T - k}^2 . \ \ \ \ \ (34)
$$

Also,

$$
\displaystyle \mathop{\mathbb E}(w^Tw) = \mathop{\mathbb E}(P^Tu u^T P) = \sigma^2I_T. \ \ \ \ \ (35)
$$

Thus, elements of w are uncorrelated with each other, have mean 0 and variance $\sigma^2$.

Since each w has expectation of $\sigma^2},

$$
\displaystyle \mathop{\mathbb E}(u^TM_Xu) = (T - k)\sigma^2. \ \ \ \ \ (36)
$$

Hence,

$$
\displaystyle \mathop{\mathbb E}(s^2) = \sigma^2. \ \ \ \ \ (37)
$$





## Distribution of Estimated Sample Variance Under Above Assumptions

Since

$$
\displaystyle w = P^Tu \ \ \ \ \ (38)
$$

when u is Gaussian, w is also Gaussian.

Then,

$$
\displaystyle u^TM_Xu = w_1^2 \lambda_1 + w_2^2 \lambda_2 + \dots + w_{T - k}^2 \lambda_{T - k}. \ \ \ \ \ (39)
$$

implies that $u^TM_Xu$ is the sum of squares of (T – k) independent $N(0, \sigma^2)$ random variables.

Thus,

$$
\displaystyle RSS^2 / \sigma^2 = u^TM_Xu / \sigma^2 \sim \chi^2 ( T - k). \ \ \ \ \ (40)
$$

Also, b and $\hat u$ are uncorrelated, since,




$$
\displaystyle 
\mathop{\mathbb E}[\hat u(b - \beta)^T] = \mathop{\mathbb E}[M_Xu u^T X (X^TX)^{-1} = 0. \ \ \ \ \ (41)
$$



Since b and $\hat u$ are independent, b and $s^2$ are also independent.

2.5. t Tests about $\beta$ Under Above Assumptions

We wish to test the hypothesis that the ith element of $\beta}, $\beta_i}, is some particular value $\beta_i^0$.

The t-statistic for testing this null hypothesis is

$$
\displaystyle t = \frac{b_i - \beta_i^0}{\hat \sigma_{b_i}} = \frac{b_i - \beta_i^0}{s (\xi^{ii})^2} \ \ \ \ \ (42)
$$

where $ \xi^{ii}$ denotes the ith column and ith row element of $(X^TX)^{-1}$ and $\hat \sigma_{b_i}$ is the standard error of the OLS estimate of the ith coefficient.

Under the null hypothesis,

$$
\displaystyle b_i \sim N(\beta_i^0, \sigma^2 \xi^{ii}). \ \ \ \ \ (43)
$$


Thus,

$$
\displaystyle \frac{b_i - \beta_i^0}{\sqrt{\sigma^2 \xi^{ii}}} \sim N(0, 1). \ \ \ \ \ (44)
$$


$$
\displaystyle 
t = \frac{
			{
				(b_i - \beta_i^0)
			} 
			/ 
			{
				\sqrt{
						\sigma^2 \xi^{ii}
					}
			}
		}
		{
			\sqrt{
					s^2 
					/ 
					\sigma^2 }
				}
					\ \ \ \ \ (45)
$$



Thus the numerator is N(0, 1) and the denominator is the square root of a chi-square distribution with (T – k) degrees of freedom. This gives a t-distribution to the variable on the left side.

## F Tests about $\beta$ Under Above Assumptions

To generalize what we did for t tests, consider that we have a matrix $R$ that represents the restrictions we want to impose on $\beta$, that is $R\beta$ gives a vector of the hypothesis that we want to test. Thus,

$$
\displaystyle H_0 \colon R\beta = r \ \ \ \ \ (46)
$$

Since,

$$
\displaystyle b \sim N(\beta, \sigma^2(X^TX)^{-1}). \ \ \ \ \ (47)
$$

Thus, under $H_0},

$$
\displaystyle Rb \sim N(r, \sigma^2R(X^TX)^{-1}R^T). \ \ \ \ \ (48)
$$

Theorem 1 If $z$ is a $(n \times 1)$ vector with $z \sim N(0, \Sigma^2)$ and non singular $\Sigma}, then $z^T\Sigma^{-1} z \sim \chi^2(n)$.

Applying the above theorem to the $Rb - r$ vector, we have,

$$
\displaystyle (Rb - r)^T (\sigma^2R(X^TX)^{-1}R^T)^{-1}(Rb - r) \sim \chi^2 (m). \ \ \ \ \ (49)
$$

Now consider,

$$
\displaystyle F = (Rb - r)^T (s^2R(X^TX)^{-1}R^T)^{-1}(Rb - r) / m. \ \ \ \ \ (50)
$$

where sigma has been replaced with the sample estimate s.

Thus,

$$
\displaystyle F = \frac{[(Rb - r)^T (\sigma^2R(X^TX)^{-1}R^T)^{-1}(Rb - r)] / m}{[RSS / (T - k)]/ \sigma^2} \ \ \ \ \ (51)
$$

In the above, the numerator is a $\chi^2(m)$ distribution divided by its degree of freedom and the denominator is a $\chi^2(T - k)$ distribution divided by its degree of freedom. Since b and $\hat u$ are independent, the numerator and denominator are also independent of each other.

Hence, the variable on the left hand side has an exact $F(m , T - k)$ distribution under $H_0$.


