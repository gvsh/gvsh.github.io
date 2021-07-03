# Function Spaces and Fourier Series





Function Spaces and Fourier Series


We started with natural numbers to count discrete objects. Then we extended them to integers to have the closure property satisfied for the subtraction operator (or less formally, to be able to use numbers to describe profit and loss statements).

Then we extended them to rationals to talk about ratios, then to reals to include square and other roots and sums of infinite series (transcendental numbers). Then we extended them to complex numbers to have the closure property satisfied for the square roots and thus to exponentiation by rationals.

We also extend it to vectors, numbers that have two, three or n dimentions and to Hamiltonions (quaternions) which are a generalization of complex numbers etc.

This extension of the concept of numbers is driven partially by the need to model the world efficiently, many of the extensions have come from physics.

When we look back at the new theories that resulted while extending the concept of numbers of we can extract out common patterns in the number systems and their spaces and this gives rise to mathematical structures such as groups, rings, fields etc.

Function spaces is essentially extending the concept of numbers to include functions.

To understand function spaces, we first need to understand Hilbert space. To create a Hilbert space, we start with $R^n$ and extend it to $R^{\infty}$.

Thus our space contains vectors with an infinite sequence of components. The length of vectors in this space can be defined analogously to the way it is defined in $R^n$, that is by sums of squares of the individual components with $n \rightarrow \infty$.

Length squared:

\displaystyle \lVert v \rVert^2 = v_1^2 + $v_2}^2 + \dots \ \ \ \ \ (1)

Inner products and orthogonality are defined just be letting $n \rightarrow \infty$ in the $R^n$ definitions of these quantities.

\displaystyle v^Tw = v_1w_1 + v_2w_2 + v_3w_3 + \dots \ \ \ \ \ (2)

Now we are ready to extend Hilbert space to a function space. Since function space includes continuous functions on the real line, the number of values is uncountably infinite and cannot be listed. So instead of summing the square of components we use the integral of the square of the function over some interval as our definition of length of the vector which is here a continuous function.

Length definition for function space:

\displaystyle \lVert f \rVert^2 = \int_0^{2 \pi}(f(x))^2 dx \ \ \ \ \ (3)

We can use the same idea of replacing infinite summation by integration to define inner products of two vectors, or here as we are in a function space, to two functions.

\displaystyle (f, g) = \int_0^{2 \pi}f(x)g(x) dx \ \ \ \ \ (4)

Sines and cosines, that is $sin \thinspace nx$ and $cos \thinspace nx$, form an orthonormal basis for this space (after dividing by their length which is $\sqrt{\pi}}).

\displaystyle \lVert sin \thinspace x \rVert^2 = \int_0^{2 \pi}(sin \thinspace x)^2 dx = \pi \ \ \ \ \ (5)

and

\displaystyle (sin, cos) = \int_0^{2 \pi}sin \thinspace x \thinspace cos \thinspace x \thinspace dx = 0 \ \ \ \ \ (6)

Just as we can write any vector as a linear combination of the basis vectors for a space, we can write any function as a linear combination of the sines and cosines.

This decomposition of a function into a series of sines and cosines is called the Fourier Series of that function.

\displaystyle f(x) = a_0 + a_1cos \thinspace x + b_1sin \thinspace x + a_2cos \thinspace 2x + b_2sin \thinspace 2x + \dots \ \ \ \ \ (7)

The coefficients $a_is$ and $b_is$ can be calculated in the same way we calculate them in finite dimensional vector spaces. We multiply both sides by a basis vector. All term but one on the right hand side then become zero (due to orthogonality of the basis vectors). Thus the coefficients can be calculated in terms of the norms and the inner products of the basis vectors with the given vector that is to be written as a linear combination.

As an example, to find $b_1$, we multiply both sides by the corresponding function $sin \thinspace x$ and integrate over the interval 0 to $2\pi$.

\displaystyle \int_0^{2 \pi}f(x)sin \thinspace x \thinspace dx = a_0\int_0^{2 \pi}sin \thinspace x \thinspace dx + a_1 \int_0^{2 \pi}cos \thinspace x \thinspace sin \thinspace x \thinspace dx + b_1\int_0^{2 \pi}(sin \thinspace x)^2 dx + \dots \ \ \ \ \ (8)

As has already been mentioned, all integrals on the right hand side except the one in which sin multiplies itself are zero. Thus $b_1$ is:

\displaystyle b_1 = \frac{\int_0^{2 \pi}f(x)sin \thinspace x \thinspace dx}{\int_0^{2 \pi}(sin \thinspace x)^2 dx} \ \ \ \ \ (9)

To see the analogy with projections, $p$, the component of vector $b$, along the line spanned by $a$ is

\displaystyle p = \frac{b^Ta}{a^Ta} \ \ \ \ \ (10)

It is helpful to see equation 9 as analogous to equation 10 for function spaces.

Here we are projecting the vector $f(x)$ onto $sin \thinspace x$ vector (they are ofcourse not truly vectors, but it is easier to see the analogy if they are thought of as vectors).


