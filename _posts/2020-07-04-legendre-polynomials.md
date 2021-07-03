# Legendre Polynomials – Gram Schmidt for Function Spaces

If you are not familiar with function spaces, please read Function Spaces post before reading this.

Sines and cosines form an orthonormal basis for the function space.

If we want to use other functions as basis, we encounter the problem of their not being orthogonal to each other. For example, if we choose the simplest functions, the powers of x as a basis, then we cannot find any interval on which 1 and {x^2$ are orthogonal to each other.

Not being orthogonal makes it hard to find projections or coefficients of the decomposition. The computational effort increases as the number of functions is increased.

However, this problem can be solved if we can create other orthonormal basis for function space by using Gram Schmidt orthogonalization over any set of independent functions.

Legendre polynomials are obtained by this orthogonalization carried while starting with powers of $x$ as the initial basis.

We chose the interval $-1 \leq x \leq 1$ so as to make even powers of $x$ orthogonal to the odd powers of $x$. Thus 1 and $x$ become orthogonal.

We need to orthogonalize $x^2$ with respect to 1 and $x$.

Thus the third orthogonal polynomials is

$$
\displaystyle v_3 = x^2 - \frac{(1, x^2)}{(1,1)}1 - \frac{(x, x^2)}{(x,x)}x = x^2 - \frac{\int_{-1}^1x^2dx}{\int_{-1}^11dx} = x^2 - \frac{1}{3}.\ \ \ \ \ (1)
$$

The polynomials thus constructed by carrying out this process are called Legendre polynomials and they are orthogonal to each other over the interval $-1 \leq x \leq 1$.

The first few Legendre polynomials are:

0: $ 1$

1: $ x $

2: $ \frac12 (3x^2-1) $

3: $ \frac12 (5x^3-3x) $

4: $ \frac18 (35x^4-30x^2+3) $

5: $ \frac18 (63x^5-70x^3+15x) $

6: $ \frac1{16} (231x^6-315x^4+105x^2-5) $

7: $ \frac1{16} (429x^7-693x^5+315x^3-35x) $

8: $ \frac1{128} (6435x^8-12012x^6+6930x^4-1260x^2+35) $

9: $ \frac 1 {128} (12155x^9-25740x^7+18018x^5-4620x^3+315x) $

10: $ \frac1{256} (46189x^{10}-109395x^8+90090x^6-30030x^4+3465x^2-63)$

A more complicated definition of these polynomials is that they are the solution to the following differential equation (Legendre’s differential equation):

$$
\displaystyle {d \over dx} \left[ (1-x^2) {d \over dx} P_n(x) \right] + n(n+1)P_n(x) = 0.\ \ \ \ \ (2)
$$

The solution is given by Rodrigues’ formula:

$$
\displaystyle P_n(x) = {1 \over 2^n n!} {d^n \over dx^n } \left[ (x^2 -1)^n \right].\ \ \ \ \ (3)
$$


