# Ordinary Least Squares Under Standard Assumptions


Suppose that a scalar $y_t$ is related to a $(k \times 1)$ vector, $x_t$ and a disturbance term $u_t$ according to the regression model.

\displaystyle y_t = x_t^T \beta + u_t \ \ \ \ \ (1)

In this article, we will study the estimation and hypothesis testing of $\beta$ when $x_t$ is deterministic and $u_t$ is i.i.d. Gaussian.

1. The Algebra of Linear Regression

Given a sample of T values of $y_t$ and the vector $x_t}, the ordinary least squares (OLS) estimate of $\beta}, denoted as $b}, is the value of $\beta$ which minimizes the residual sum of squares (RSS).

\displaystyle RSS = \sum_{t=1}^T (y_t - x_t^T b)^2 \ \ \ \ \ (2)

The OLS estimate of $\beta}, b, is given by:

\displaystyle b = \bigg(\frac{1}{T}\sum_{t=1}^T x_tx_t^T \bigg)^{\!-1} \!\!\cdot\, \frac{1}{T}\sum_{t=1}^n x_ty_t. \ \ \ \ \ (3)

The model is written in matrix notation as:

\displaystyle y = X\beta + u. \ \ \ \ \ (4)

\displaystyle \bold{y}= \begin{bmatrix} y_1 \\ y_2 \\ \vdots \\ y_T \end{bmatrix},\quad \bold{x}= \begin{bmatrix} x_1^T \\ x_2^T \\ \vdots \\ x_T^T \end{bmatrix},\quad \bold{u}= \begin{bmatrix} u_1 \\ u_2 \\ \vdots \\ u_T \end{bmatrix}. \ \ \ \ \ (5)

where $y$ is a $T \times 1$ vector, $X$ is a $T \times k$ matrix, $\beta$ is a $k \times 1$ vector and $u$ is a $T \times 1$ vector.

Thus,

\displaystyle b = (X^TX)^{-1}X^Ty. \ \ \ \ \ (6)

Similarly,

\displaystyle \hat u = y - Xb = y - X(X^TX)^{-1}X^Ty = [I_T - X(X^TX)^{-1}X^T]y = M_Xy. \ \ \ \ \ (7)

where $M_X$ is defined as:
