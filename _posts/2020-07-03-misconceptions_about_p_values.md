# Misconceptions about p-values


## Introduction

The misconceptions surrounding p values are an example where knowing the history of the field and the mathematical and philosophical principles behind it can greatly help in understanding.

The classical statistical testing of today is a hybrid of the approaches taken by R. A. Fisher on the one hand and Jerzy Neyman and Egon Pearson on the other.

P-value is often confused with the Type I error rate – {\alpha} of the Neyman-Pearson approach.

In statistics journals and research, the Neyman-Pearson approach replaced the significance testing paradigm 60 years ago, but in empirical work the Fisher approach is pervasive.

The statistical testing approach found in the textbooks on statistics is a hybrid

## Fisher’s Significance Testing

Fisher held the belief that statistics could be used for inductive inference, that “it is possible to argue from consequences to causes, from observations to hypothesis” and that it it possible to draw inferences from the particular to the general.

Hence he rejected the methods in which probability of a hypothesis given the data, {\mathop{\mathbb P}(H \vert x)}, are used in favour of ones in which probability of data, {\mathop{\mathbb P}(H \vert x)}, given a particular hypothesis are used.

In his approach, the discrepancies in the data are used to reject the null hypothesis. This is done as follows:

The researcher sets up a null hypothesis, which is the status quo belief.

The sampling distribution under the null hypothesis is known.

If the observed data deviates from the mean of the sampling distribution by more than a specified level, called the level of significance, then we reject the null hypothesis. Otherwise, we “fail to reject” the null hypothesis.

The p-value in this approach is the probability of observing data at least as favorable to the alternative hypothesis as our current data set, if the null hypothesis is true.

There is a common misconception that if {p = .05}, then the null hypothesis has only a 5% chance of being true.

This is clearly false, and can be seen from the definition as the P value is calculated under the assumption that the null hypothesis is true. It therefore cannot be a probability of the null hypothesis being false.

Conversely, a p value being high merely means that a null effect is statistically consistent with the observed results.

It does not mean that the null hypothesis is true. We only fail to reject, if we adopt the data based inductive approach.

We need to consider the Type I and Type II error probabilities to draw such conclusions, which is done in the Neyman-Pearson approach.

## Neyman-Pearson Theory

The main contribution of Neyman-Pearson hypothesis testing framework (they named it to distinguish it from the inductive approach of Fisher’s significance testing) is the introduction of the

    probabilities of committing two kinds of errors, false rejection (Type I error), called {\alpha}, and false acceptance (Type II error), called {\beta}, of the null hypothesis.
    power of a statistical test. It is defined as the probability of rejecting a false null hypothesis. It is equal to {1 - \beta}. 

Fisher’s theory relied on the rejection of null hypothesis based on the data, assuming null hypothesis to be true. In contrast, the Neyman-Pearson approach provides rules to make decisions to choose the between the two hypothesis.

Neyman–Pearson theory, then, replaces the idea of inductive reasoning with that of, what they called, inductive behavior.

In his own words, inductive behaviour was meant to imply: “The term ‘inductive behavior’ means simply the habit of humans and other animals (Pavlov’s dog, etc.) to adjust their actions to noticed frequencies of events, so as to avoid undesirable consequences”.

Then, in this approach, the costs associated with Type I and Type II behaviour determine the decision to accpet or reject. These costs vary from experiment to experiment and this thus is the main advantage of the Neyman-Pearson approach over Fisher’s approach.

Thus while designing the experiment the researcher has to control the probabilities of Type I and Type II errors. The best test is the one that minimizes the Type II error given an upper bound on the Type I error.

And what adds to the source of confusion is the fact that Neyman called the Type I error the level of significance, a term that Fisher used to denote the p values.
