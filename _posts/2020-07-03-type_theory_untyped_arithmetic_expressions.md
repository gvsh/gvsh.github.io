

# Type Theory


 The following are present in this first language:

true and false.

conditional expressions.

The numeric constant 0.

The arithmetic operators succ and prec.

A testing operation iszero. 

t = true

false

if t then t else t

0

succ t

prec t

iszero t

Programs

A program in the above language is a term built up from the forms given in the grammar.

if false then 0 else 1

$\triangleright$ 1

1. Syntax

The grammar above is a way to specify the syntax of the language. One other way to do so is to specify it inductively using set theory.

Definition 1 Terms, Inductively: The set of terms is the smallest set $ \mathcal{T} $ such that

$true, false, 0$ $\subseteq \mathcal{T}$.

if $t_1$ $\in \mathcal{T}$ then succ($t_1$), pred($t_1$), iszero($t_1$) $\subseteq \mathcal{T}$


if $t_1$ $\in \mathcal{T}}, $t_2 \in \mathcal{T}$ and $t_3 \in \mathcal{T}$ then if $t_1$ then $t_2$ else $t_3 \in \mathcal{T}}. 

Definition 2 Terms, By Inference Rules: The set of terms is defined by the following rules:

Rules set 1:

$$
\displaystyle true \in \mathcal{T} \ \ \ \ \ (1)
$$


$$
\displaystyle false \in \mathcal{T} \ \ \ \ \ (2)
$$



$$
\displaystyle 0 \in \mathcal{T} \ \ \ \ \ (3)
$$


Rules set 2:

$$
\displaystyle \frac{t_1 \in \mathcal{T}}{succ(t_1) \in \mathcal{T}} \ \ \ \ \ (4)
$$


$$
\displaystyle \frac{t_1 \in \mathcal{T}}{pred(t_1) \in \mathcal{T}} \ \ \ \ \ (5)
$$


$$
\displaystyle \frac{t_1 \in \mathcal{T}}{iszero(t_1) \in \mathcal{T}} \ \ \ \ \ (6)
$$


Rules set 3:

$$
\displaystyle \frac{ t_1 \in \mathcal{T},  t_2 \in \mathcal{T},  t_3 \in \mathcal{T} } {t_1 \quad   then \  t_2 \ else \quad  t_3 \in \mathcal{T}}. \ \ \ \ \ (7)
$$


Each rule is read “If we have established the statements in the premise of the rules above, then the we may derive the conclusions in the lines below”. The rules with no premises are called axioms. 

Definition 3 Terms, Concretely: The set of terms can also be given by constructing sets of successively bigger sizes.

For each natural number $i$ we define a set $\mathcal{S}_i$ as follows:

$$
\displaystyle \mathcal{S}_0 = \emptyset \\ \ \ \ \ \ (8)
$$


$$
\displaystyle \mathcal{S}_{i + 1 } = {true, false, 0\} \\ \cup \quad {succ(t_1), \thickspace pred(t_1), \thickspace iszero(t_1) \thickspace | \thickspace t_1 \thickspace \in \mathcal{S}_i} \\ \cup \quad {if \thickspace t_1 \thickspace then \thickspace t_2 \thickspace else \thickspace t_3 }\thickspace | \thickspace t_1, \thickspace t_2, \thickspace t3 \in \mathcal{S}_i}. \ \ \ \ \ (9)
$$


Finally, let

$$
\displaystyle \mathcal{S} = \bigcup_{i=1}^n \mathcal{S}_i \ \ \ \ \ (10)
$$


Inference rules are just another way of writing the set theoretic definition.

Each inference rule may imply an infinite tree of terms.

Proposition 4 $\mathcal{T} = \mathcal{S}}. 

In definition on page we saw that a term can have one of three forms. This can be used in two ways:

to give inductive definitions of functions over set of terms.
in proving theorems about the properties of terms. 

The consts, size and depth functions can be defined using inductive definition over the set of terms. Relations between sizes and depths, the cardinality of consts and size can be proven using the definition of the set of terms.

2. Semantic Styles

2.1. Operational Semantics

The behaviour of the program is described by specifying an abstract machine for it.

The machine is abstract in the sense that the terms of the program are what form the machine code, instead of some low level language.

The terms are represented by states of an abstract machine. The meaning of a program is represented by the output of the computation of the abstract machine whose starting state is the first term of the program, that is the value in the final state.

It is customary to give two or more different operational semantics for a single language. One closer to the language in question and the other closer to the machine language.

Proving that the above two operational semantics correspond in some suitable sense amounts to proving that the implementation is correct.

2.2. Denotational Semantics

It takes a more abstract view of meaning and instead of defining the meaning of terms in terms of a sequence of machine states, the meaning of term is defined to be some mathematical object – a function or a number.

3. Evaluation

Consider a language with grammar as below:

Syntax:

$$
\displaystyle t = \thickspace \text{terms} \\ = true \thickspace \text{constant true} \\ = false \thickspace \text{constant false} \\ = if \thickspace t \thickspace then \thickspace t \thickspace else \thickspace t \thickspace \text{conditional} \\ \text{v} = \thickspace \text{values} \\ = true \thickspace \text{true value} \\ = false \thickspace \text{false value} \ \ \ \ \ (11)
$$


Values, a subset of terms, are the possible final outcomes of evaluation.

The evaluation relation is a binary relation on the set of terms.

Evaluation: t $\rightarrow$ t‘

$$
\displaystyle if \thickspace true \thickspace then \thickspace t \thickspace else \thickspace u \thickspace \rightarrow \thickspace t \thickspace \text{E-IfTrue} \\ if \thickspace false \thickspace then \thickspace t \thickspace else \thickspace u \thickspace \rightarrow u \thickspace \text{E-IfFalse} \\ \frac{t \rightarrow u} $ if \thickspace t \thickspace then \thickspace v \thickspace else \thickspace w \thickspace \rightarrow \thickspace if \thickspace u \thickspace then \thickspace v \thickspace else \thickspace w } \text{\textsc{E-If}} \ \ \ \ \ (12)
$$


Definition 5 Evaluation Strategy: The interplay between the rules determines a particular order of evaluation. 

Definition 6 Computation Rules: 

Definition 7 Congruence Rules: 

Definition 8 An instance of an inference rule is obtained by replacing the metavariables in the premises and conclusions of the rule. 

Definition 9 A rule is satisfied by a relation if each instance of the rule the conclusion is in the rule or one of the premises is not. 

Definition 10 A one-step evaluation relation $\rightarrow$ is the smallest binary relation on the set of terms which satisfies all the evaluation inference rules for the set of terms. 

Definition 11 When a pair (t, t’) is in the one-step evaluation relation we say that the evaluation statement t $\rightarrow$ t’ is derivable . 

Theorem 12 (Determinacy of One-Step Evaluation) If t $\rightarrow$ t’ and t $\rightarrow$ t”, then t’ $=$ t”. 

Definition 13 A term t is in normal form if no evaluation rule applies to it, i.e.\, if there is no t’ such that t $\rightarrow$ t’. 

Theorem 14 Every value is in normal form. 

Theorem 15 If t is in normal form, then t is a value. 

Definition 16 The multi-step evaluation relation $\rightarrow^{*}$ is the reflexive, transitive closure of the one-step evaluation relation. If t $\rightarrow$ t’ and t’ $\rightarrow$ t”, then t $\rightarrow$ t”. 

Consider a language with grammar as below:

Syntax:

$$
\displaystyle t = \text{terms} \\ = 0 \thickspace \text{constant 0} \\ = succ \thickspace t \thickspace \text{successor} \\ = pred \thickspace t \thickspace \text{predecessor} \\ = iszero \thickspace t \thickspace \text{zero test} \\ = true \thickspace \text{constant true} \\ = false \thickspace \text{constant false} \\ = if \thickspace t \thickspace then \thickspace t \thickspace else \thickspace t \thickspace \text{conditional} \\ \text{v} = \text{values} \\ = true \thickspace \text{true value} \\ = false \thickspace \text{false value} \\ = nv \text{numeric value} \\ \text{nv} = \text{numeric values} \\ = 0 \thickspace \text{0 value} \\ = succ \thickspace nv \thickspace \text{successor value} \ \ \ \ \ (13)
$$


Values, a subset of terms, are the possible final outcomes of evaluation.

The evaluation relation is a binary relation on the set of terms.

Evaluation: t $\rightarrow$ t‘

$$
\displaystyle if \thickspace true \thickspace then \thickspace t \thickspace else \thickspace u \thickspace \rightarrow \thickspace t \thickspace \text{E-IfTrue$ \\ if \thickspace false \thickspace then \thickspace t \thickspace else \thickspace u \thickspace \rightarrow \thickspace u \thickspace \text{E-IfFalse} \\ \frac{t \thickspace \rightarrow \thickspace u}{if \thickspace t \thickspace then \thickspace v \thickspace else \thickspace w} \rightarrow if \thickspace u \thickspace then \thickspace v \thickspace else \thickspace w \text{\textsc{E-If}} \ \ \ \ \ (14)
$$


