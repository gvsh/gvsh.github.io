# Ordinary Least Squares Under Standard Assumptions


Suppose that a scalar $y_t$ is related to a $(k \times 1)$ vector, $x_t$ and a disturbance term $u_t$ according to the regression model.

$$
\displaystyle y_t = x_t^T \beta + u_t \ \ \ \ \ (1)
$$

In this article, we will study the estimation and hypothesis testing of $\beta$ when $x_t$ is deterministic and $u_t$ is i.i.d. Gaussian.

1. The Algebra of Linear Regression

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


