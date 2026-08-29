

book: "Becoming a Data Head"

session: 4

date: "8/27/2026"

time: "10 pm"

presenter: "Soroush Hosseini"

chapters: "6"

participants:

  - Sahar Matin
  - Arman Ebrahimi
  - Shayan Najafian


  

# 1. Chapter Summary

  

## Chapter 6 — Examine the Probabilities

  

Chapter 6 focuses on **probability as the language of uncertainty**. Because variation exists everywhere, uncertainty is unavoidable, and probability gives us a structured way to reason about it rather than relying only on intuition.

  

A major theme of the presentation was that **probability is often counter-intuitive**. People frequently confuse related probabilities, assume independence when events are actually connected, or create stories that feel reasonable but violate basic probability rules.

  

---

  

## Conditional Probability

  

Conditional probability describes the probability of one event occurring **given that another event has already occurred**.

  

It is written as:

  

**P(A | B)**

  

and read as:

  

> **The probability of A given B.**

  

The presentation emphasized that probabilities can change significantly when new information becomes available.

  

---

  

## Independent Events

  

Two events are independent when knowing the result of one does not change the probability of the other.

  

For independent events:

  

**P(A | B) = P(A)**

  

For example, the result of a coin flip does not affect the probability of drawing a spade from a deck of cards.

  

However, assuming independence when events are actually dependent can seriously underestimate risk.

  

The presentation used mortgage defaults and risky business projects to show how shared economic conditions can cause supposedly separate events to fail together.

  

---

  

## Multiplicative and Additive Rules

  

When considering two events happening together:

  

**P(A and B) = P(B) × P(A | B)**

  

For independent events:

  

**P(A and B) = P(A) × P(B)**

  

The probability of two events occurring together cannot be greater than the probability of either event occurring individually.

  

For one event **or** another:

  

**P(A or B) = P(A) + P(B) - P(A and B)**

  

The overlap must be subtracted to avoid counting the same outcomes twice.

  

---

  

## The Conjunction Fallacy

  

The presentation introduced a variation of the famous **Linda Problem**.

  

Participants were asked which statement was more probable:

  

1. Sam lives in Ohio.

2. Sam lives in Ohio **and** works as a data scientist.

  

Even if the second description seems more consistent with Sam's personality, it cannot be more probable because it adds another condition.

  

> **More "and" conditions mean fewer possible outcomes.**

  

---

  

## The Gambler's Fallacy

  

The **gambler's fallacy** is the mistaken belief that previous independent outcomes change the probability of the next event.

  

For example:

  

> "Heads appeared 10 times, so tails must be more likely next."

  

For a fair coin, the next flip is still:

  

**50% heads / 50% tails**

  

Past independent outcomes do not make one result "due."

  

---

  

## Confusion of the Inverse

  

One of the most important concepts in the chapter is:

  

**P(A | B) ≠ P(B | A)**

  

Knowing the probability of a positive test given that someone has a disease is not the same as knowing the probability that someone has the disease given a positive test.

  

This mistake is called the **confusion of the inverse**.

  

---

  

## The Virus-Test Example

  

The presentation illustrated this with a virus-detection example:

  

- 1% of laptops have a virus.

- The test is 99% accurate.

- A laptop receives a positive result.

  

The intuitive answer may be that there is a **99% probability** the laptop is infected.

  

However, because the virus itself is rare, false positives matter. In the example, the probability of actually having the virus after receiving a positive result is only about:

  

> **50%**

  

This demonstrates why **base rates matter**.

  

---

  

## Bayes' Theorem

  

Bayes' theorem allows us to relate inverse conditional probabilities.

  

It is useful when we know something such as:

  

**P(Positive Test | Disease)**

  

but want to determine:

  

**P(Disease | Positive Test)**

  

The presentation showed applications in:

  

- Medical screening

- Legal evidence

- Spam filtering

  

Using Bayes' theorem in the virus example leads to the 50% result rather than the intuitive 99% answer.

  

---

  

## Calibration

  

Probability estimates should also be **calibrated**.

  

If someone repeatedly says they are 70% confident, then over many similar predictions they should be correct roughly 70% of the time.

  

Someone who regularly claims 90% confidence but is correct only 60% of the time is poorly calibrated and overconfident.

  

---

  

## Rare Events

  

A very small probability does not mean an event is impossible.

  

When there are millions or billions of opportunities for an event to occur, even very unlikely events will sometimes happen.

  

The chapter therefore warns against both:

  

- Treating rare events as impossible

- Multiplying many probabilities unnecessarily to make ordinary events appear extraordinarily unlikely

  

---

  

## Overall Takeaway — Chapter 6

  

The presentation concluded with three major lessons:

  

1. **Be careful when assuming independence.**

2. **Remember that probabilities depend on conditions and assumptions.**

3. **Make sure probability estimates are meaningful and calibrated.**

  

It also reinforced that:

  

> **P(A | B) is not the same as P(B | A).**

  

Probability is difficult partly because human intuition is not naturally good at reasoning about uncertainty. The goal is therefore not to trust our first instinct, but to slow down, identify the conditions, and apply the correct probability structure.

  

