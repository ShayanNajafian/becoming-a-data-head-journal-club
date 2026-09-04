book: "Becoming a Data Head"

session: 5

date: "9/3/2026"

time: "9 pm"

presenter: "Soroush Hosseini"

chapters: "7"

participants:

- "Sahar Matin"
- "Shayan Najafian"
- "Alireza Ranjbar"

# 1. Chapter Summary

## Chapter 7 — Challenge the Statistics

Chapter 7 focuses on **statistical inference** and how to critically evaluate statistical claims instead of accepting numbers at face value.

The central idea is that we usually cannot observe an entire population, so we collect a **sample** and use it to make informed conclusions about the larger population.

Because samples contain variation and uncertainty, statistical results should be interpreted carefully and challenged with the right questions.

---

## Statistical Inference — From Sample to Population

**Statistical inference** allows us to use information from a sample to learn about a larger population.

For example, instead of asking every student in a country whether they support something, we might survey 1,000 students and use that sample to estimate the opinion of the larger population.

The important point is:

> **A sample gives us evidence about the population, not perfect certainty.**

---

## Point Estimates and Confidence Intervals

Suppose a poll asks 1,000 students a question and:

**655 students answer "yes."**

The sample estimate is:

**65.5%**

But we should not assume that exactly 65.5% of the entire population would answer yes.

A confidence interval gives us some **wiggle room** around the estimate.

For example:

**65.5% ± 3%**

gives a range of approximately:

**62.5% to 68.5%**

The general idea is:

> **Confidence intervals help communicate uncertainty around an estimate.**

Larger samples generally produce narrower intervals and therefore more precise estimates.

---

## Sample Size Matters

The presentation used a simple product-review example.

A product with a one-star rating based on:

**1 review**

is much less convincing than the same one-star rating based on:

**300 reviews**

More observations generally provide more evidence and reduce random variation.

However:

> **Big data does not necessarily mean complete or representative data.**

A dataset can contain millions of observations while still excluding important groups of people.

---

## Null and Alternative Hypotheses

Hypothesis testing starts with two competing statements.

### Null Hypothesis — H₀

The **null hypothesis** represents the status quo or the assumption that no meaningful effect or change exists.

### Alternative Hypothesis — Hₐ

The **alternative hypothesis** represents the new effect or difference we are looking for evidence to support.

For example:

**Question:** Has customer satisfaction improved?

**H₀:** Customer satisfaction has not improved.

**Hₐ:** Customer satisfaction has improved.

The data must provide enough evidence before we reject the null hypothesis.

A useful analogy is:

> **Innocent until proven guilty.**

The null hypothesis is assumed first, and the evidence must be strong enough to challenge it.

---

## Understanding the p-Value

A **p-value** asks:

> **If the null hypothesis were true, how unusual would the result we observed be?**

A small p-value means that the observed result would be relatively unusual if the null hypothesis were true.

A commonly used significance level is:

**α = 0.05**

If:

**p-value < 0.05**

the result is commonly described as **statistically significant**, and the null hypothesis is rejected under that decision rule.

---

## The Basketball Intern Example

The presentation illustrated p-values with a basketball example.

Suppose an intern claims that he makes at least:

**50% of his shots.**

He then misses:

**10 shots in a row.**

If his probability of missing each shot were 50%, the probability of 10 consecutive misses would be:

**0.5¹⁰ ≈ 0.00098**

which is approximately:

**1 in 1,000**

Such an unusual result provides strong evidence against the original claim.

---

## Type I and Type II Errors

Even when we use statistical testing, we can still make incorrect decisions.

### Type I Error — False Positive

A Type I error occurs when we reject a null hypothesis that is actually true.

Analogy:

> **Sending an innocent person to jail.**

### Type II Error — False Negative

A Type II error occurs when we fail to reject a null hypothesis that is actually false.

Analogy:

> **Letting a guilty person go free.**

There is often a tradeoff between these two types of errors.

For example, a disease-screening system designed to catch almost every real case may also generate more false positives.

---

## Statistical Significance ≠ Practical Significance

One of the most important lessons of Chapter 7 is:

> **Statistical significance does not automatically mean practical importance.**

With a very large sample, even extremely small differences can become statistically significant.

For example, a difference may be statistically detectable but too small to matter to a business or to change a real-world decision.

Therefore, we should also ask:

- How large is the effect?
- Is the difference meaningful?
- Does it matter to the business?
- Would this result change our decision?

The magnitude of the effect is just as important as whether a p-value crosses a threshold.

---

## The Process of Statistical Inference

The presentation summarized the process as:

1. Ask a meaningful question.
2. Define the null and alternative hypotheses.
3. Establish a significance level.
4. Calculate the p-value.
5. Examine confidence intervals.
6. Decide whether there is enough evidence to reject the null hypothesis.

The important point is not only performing these calculations, but understanding what question each step is trying to answer.

---

# How to Challenge Statistics

Chapter 7 also provides a practical framework for questioning statistical claims.

A Data Head should not simply hear a number and accept it.

Instead, ask questions about the context, data, assumptions, and interpretation.

---

## Context — Compared to What?

Suppose someone says:

> **"Our click-through rate increased by 50%."**

That sounds impressive.

But perhaps the actual change was:

**0.10% → 0.15%**

The relative increase is:

**50%**

but the absolute increase is only:

**0.05 percentage points**

Therefore, whenever we hear a claim such as:

> **"Sales increased by 10%."**

we should immediately ask:

> **Compared to what?**

Context can completely change how impressive a statistic appears.

---

## What Are You Testing?

Every statistical result should have a clear question behind it.

We should not accept a table of p-values or statistics without first understanding:

> **What question is this analysis actually trying to answer?**

The question should ideally be understandable in plain language before moving into technical statistical details.

---

## Significance Level

A commonly used significance level is:

**α = 0.05**

A lower significance level creates a higher standard of evidence before rejecting the null hypothesis.

However, changing the threshold also affects the balance between false positives and false negatives.

An important warning from the presentation is:

> **Do not choose the significance level after seeing the result.**

Doing so is similar to throwing a dart and moving the target afterward.

---

## Multiple Testing

Another problem appears when many statistical tests are performed.

Suppose we test:

**100 different foods**

for a relationship with cancer using:

**α = 0.05**

Even if none of those foods have a real effect, some may appear statistically significant simply because of random variation.

This demonstrates why we should ask:

> **How many different tests were performed before this significant result was found?**

A single impressive p-value can be misleading when it comes from a very large number of tests.

---

## Confidence Intervals

A confidence interval provides additional information that a p-value alone does not show.

It helps us understand:

- The uncertainty around an estimate
- The plausible range of the effect
- How precise the estimate is

A narrow confidence interval generally indicates greater precision, while a wide interval indicates greater uncertainty.

Therefore:

> **Do not look only at p-values. Look at the estimated effect and its uncertainty as well.**

---

## Practical Significance

A result may pass a statistical significance threshold but still have very little real-world value.

For example, a difference of:

**0.5 inches**

between the average heights of two groups might be statistically detectable with enough observations.

But the important question is:

> **Does that difference actually matter?**

A Data Head should therefore ask about both:

**Statistical significance**

and:

**Practical significance**

---

## Correlation and Causality

The presentation again emphasized:

> **Correlation ≠ Causation**

Suppose customer satisfaction improves after an intern joins a company.

The intern may claim:

> "My work caused customer satisfaction to improve."

But many other factors may have changed during the same period.

Without an appropriate experimental design, the observed relationship alone does not establish that the intern caused the improvement.

Therefore, whenever someone makes a causal claim, ask:

> **What evidence allows us to move from association to causation?**

---

# The Data Head's Challenge Checklist

When presented with a statistical result, ask:

1. **Context:** Compared to what?
2. **Sample Size:** How many observations are behind the result?
3. **Testing:** What question is being answered?
4. **Null Hypothesis:** What is the status quo?
5. **Significance Level:** What threshold was chosen?
6. **Multiple Tests:** How many tests were performed?
7. **Confidence Intervals:** What is the uncertainty around the estimate?
8. **Practical Significance:** Does the result actually matter?
9. **Causality:** Is someone assuming cause and effect?

---

## Overall Takeaway — Chapter 7

Chapter 7 teaches us to become **critical consumers of statistics**.

The main lessons are:

1. **Samples contain uncertainty and variation.**
2. **Sample size and context matter.**
3. **A small p-value is evidence against a null hypothesis, not absolute proof.**
4. **Statistical significance does not automatically mean practical importance.**
5. **Running many tests increases the chance of misleading significant results.**
6. **Confidence intervals help us understand uncertainty and effect size.**
7. **Correlation should not automatically be interpreted as causation.**
8. **Statistical claims should always be challenged with meaningful questions.**

The overall message of the presentation was:

> **Statistical inference helps us use limited data to make better decisions, but it does not give us absolute truth.**