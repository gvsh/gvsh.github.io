# Quotient Groups




## Motivation

Consider the set ${\mathbb Q}$ of rational numbers. We say that a rational number is of the form $a/b$ where $b \ne 0$. But all numbers of the form, $m a / m b$ where $m \ne 0$ are also the same rational number. Thus, the elements of ${\mathbb Q}$ are not really numbers of the form $a/b$ where $b \ne 0$, but “equivalence classes” of numbers, where two numbers $a/b$ and $c/d$ are said to belong to the same equivalence class if $ad = bc$.

This method of treating two elements of a set as equal to create a new set can be used in other settings and on other structures, like groups and fields.

## Using Quotients to Create a Field from a Ring

Consider the set of all polynomials ${\mathbb Q}[x]$ in variable $x$ with coefficients in ${\mathbb Q}$ (For example, $2x^3 + \frac{1}{2} x^2 - x - 1$ is an element of this set.). Any two polynomials in this set can be added, subtracted or multiplied together to give another polynomial from the same set. Thus ${\mathbb Q}[x]$ is a commutative ring. But it is not a field because dividing one polynomial by another does not give another polynomial.

We can however convert this to a field by using the concept of equivalence classes.

Let us chose any polynomial (say $x^3 - x - 1$) which does not have roots in ${\mathbb Q}$ and thus cannot be factorized in it. We create an equivalence class from this polynomial such that all multiples of this this polynomial belong to the class and this class would stand for zero in the new field that we are creating.

Any polynomial $P$, which is not a multiple of $x^3 - x - 1$ can then be written as $PQ + R(x^3 - x - 1) = 1$. Then, since we regard $x^3 - x - 1$ as zero, $Q$ is the inverse of $P$ in this new field. Thus all $P$s have inverses and we have turned the commutative ring into a field which is called the quotient of $\mathbb Q[x]$ by $x^3 - x - 1$, written as $ {\mathbb Q} [x] / (x^3 - x - 1) $.

In creating quotient fields the operation on fields and the equivalence relation are defined such that if $P$ and $P^\prime$ belong to the same equivalence class and so do $Q$ and $Q^\prime$, with $P \ne Q$, then $P + Q$ and $P^\prime + Q^\prime$ belong to the same equivalence class as does $PQ$ and $P^\prime Q^\prime$.

## Quotient Groups

We want to extend what we did while creating a field from the ring of polynomials to create a new group from two given groups.

Let $G$ be a group and $H$ be a subgroup of G. We will define two elements of $G$, $g_1$ and $g_2$ to be equivalent with respect to the group $H$ if $g_1^{-1}g_2 \in H$. The equivalence class of an element $g \in G$ is then $g h$ such that $h \in H$. This set of the equivalence class of $g$ is written as $gH$ and is called the left coset of $H$.

We want to turn the set of left cosets into a group. The natural choice for the composition operation would be using the group multiplication already defined. Thus, $g_1 H \ast g_2 H = g_1 g_2 H$.

However, this does not always work. It only works under the condition that $H$ should be a normal subgroup of $G$. Under this condition, different elements from the original cosets map to the same coset $g_1 g_2 H$.

If $H$ is a normal subgroup, then the set of left cosets forms a group written as $G/H$ and called the quotient of $G$ by $H$. Conversely, we regard $G$ as the product of $H$ and $G/H$. Thus, if we understand $H$ and $G/H$ we understand $G$.

The groups that do not have normal subgroups are called “simple groups” and have a special role, in that they act the way prime numbers do in number theory. 

