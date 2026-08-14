---

book: "Becoming a Data Head"

session: 2

date: "8/13/2026"

time: "10 pm"

presenter: "Shayan Najafian"

chapters: "3 and 4"

participants:

  - "Arman Ebrahimi"

  - "Micheal Zamanian"

  - "Sahar Matin"

  - "Mahdi Eshaghzadeh"

  - "Soroush Hosseini"

  - "Amir Batoulzadeh"

  - "Alireza Ranjbar"

---

  

# 1. Chapter Summary

  

## Chapter 3 — Prepare to Think Statistically

  

Chapter 3 introduces **statistical thinking** as a way of approaching data with curiosity and skepticism. A number should be treated as evidence rather than automatically accepted as truth. Important questions include where a number came from, how certain it is, and what assumptions were used to produce it.

  

A central idea is that **variation exists everywhere**. Sales, surveys, markets, and other measurements naturally fluctuate over time. Therefore, seeing a different value does not necessarily mean that the underlying process has changed.

  

The chapter distinguishes between two important sources of variation:

  

- **Measurement variation:** variation introduced by the way something is measured.

- **Random variation:** variation that naturally exists in the process itself.

  

Both sources create uncertainty and must be considered before interpreting changes in data.

  

Another useful way to think about variation is through **signal vs. noise**:

  

- **Signal** represents a meaningful underlying change.

- **Noise** represents variation that happens even when the underlying process has not meaningfully changed.

  

Because of this, we should **not explain every peak and valley** in a graph. The fact that a value changed does not automatically mean that something caused the change. Before creating a story around a rise or fall, we should first ask whether ordinary variation could explain it.

  

### Small Samples and Extreme Results

  

Small samples tend to show **more variation**, while larger samples tend to be more stable. This means extreme percentages or rates are more likely to appear when the denominator is small.

  

The **kidney-cancer example** demonstrates this idea. Some small rural counties appeared among those with the highest kidney-cancer rates, but small rural counties also appeared among those with the lowest rates. The main reason was that small populations make rates much more sensitive to individual cases.

  

This connects to Daniel Kahneman and Amos Tversky's idea of the **law of small numbers**. People tend to expect small samples to behave like accurate miniature versions of the full population, even though small samples are much noisier than our intuition expects.

  

### Probability vs. Statistics

  

The chapter also distinguishes probability from statistics:

  

- **Probability:** starts with knowledge about a population or process and predicts what a sample may look like.

- **Statistics:** starts with a sample and uses it to learn about the larger population.

  

A useful summary is:

  

> **Probability drills down. Statistics drills up.**

  

### Probability vs. Intuition

  

Human intuition about probability is often unreliable.

  

For example, if **80% of dentists agree** with a statement and five dentists are randomly selected, the probability that **exactly four of the five agree** is approximately **41%**, not 80%.

  

The population probability does not guarantee that every small sample will have the same proportion.

  

This reinforces the broader message of the chapter:

  

> **Randomness in small samples is usually greater than our intuition expects.**

  

### Descriptive vs. Inferential Statistics

  

The chapter also introduces the distinction between:

  

- **Descriptive statistics:** summarize the data that has already been observed.

- **Inferential statistics:** use a sample to make conclusions or estimates about a larger population.

  

Inferential statistics therefore requires careful attention to uncertainty, sample size, representativeness, and assumptions.

  

### Chapter 3 Takeaway

  

The main lesson of Chapter 3 is to avoid immediately creating explanations for every pattern in data.

  

Before asking:

  

> **Why did this happen?**

  

first ask:

  

> **Is this pattern actually meaningful, or could normal variation explain it?**

  

---

  

## Chapter 4 — Argue with the Data

  

Chapter 4 shifts the focus from interpreting variation to questioning the **quality and origin of the underlying data**.

  

The main principle is:

  

> **Garbage in → Garbage out**

  

No statistical technique, machine-learning model, or sophisticated algorithm can fully rescue data that is fundamentally inappropriate or misleading.

  

### Tell Me the Data Origin Story

  

Before analyzing a dataset, we should understand how it came into existence.

  

Important questions include:

  

- Who collected the data?

- How was it collected?

- Why was it collected?

  

Understanding the origin of the data can reveal limitations, biases, measurement problems, or differences between the data that was collected and the question we actually want to answer.

  

### Representative Data and Sampling Bias

  

A **large sample is not automatically a representative sample**.

  

Increasing the amount of data can reduce random variation, but it does not automatically eliminate systematic bias.

  

Therefore, it is important to ask whether the observations in the dataset resemble the population about which we want to make conclusions.

  

### Outliers

  

Outliers should not automatically be removed simply because they are unusual or because they change the result of an analysis.

  

An extreme value may represent:

  

- a data-entry or measurement error,

- a real but unusual observation,

- or an observation from a different population.

  

Any decision to remove an outlier should have a defensible reason.

  

### What Data Am I Not Seeing?

  

One of the most important questions in Chapter 4 is:

  

> **What data am I not seeing?**

  

Sometimes the missing observations are more important than the observations being shown.

  

Missing values can also contain useful information. A value may be missing for a systematic reason rather than purely by accident.

  

### Proxy Measures

  

Data frequently measures difficult concepts indirectly.

  

For example, concepts such as customer loyalty, reputation, satisfaction, or performance may not be directly observable. Instead, analysts use measurable variables as **proxies**.

  

This creates another important question:

  

> **Are we really measuring the concept we care about, or only an imperfect substitute for it?**

  

### Challenger Case Study

  

The Challenger example demonstrates the danger of analyzing only part of the relevant data.

  

The analysis emphasized shuttle flights in which O-ring distress occurred, while many flights where **no O-ring distress occurred** were not included in the comparison.

  

Those zero-failure flights were important because they provided the denominator needed to understand how the risk of O-ring distress changed with temperature.

  

When the complete set of observations is considered, the relationship between colder temperatures and O-ring problems becomes much clearer.

  

The main statistical lesson is:

  

> **Failures alone cannot tell us the probability of failure. We also need to know how many opportunities there were for failure.**

  

This leads to a broader data-science principle:

  

> **Zero is data.**

  

Customers who did not churn, loans that did not default, machines that did not fail, and patients who did not develop a disease can be just as informative as the cases where the event occurred.

  

### Chapter 4 Takeaway

  

Chapter 4 teaches us not to passively accept a dataset simply because it exists.

  

Before trusting an analysis, ask:

  

- Where did the data come from?

- Is the sample representative?

- Could there be sampling bias?

- How were outliers handled?

- What observations or values are missing?

- Are we measuring the actual concept of interest?

- What data are we not being shown?

  

---

  

## Overall Takeaway — Chapters 3 & 4

  

Together, the chapters teach two complementary habits:

  

> **Chapter 3:** Question the pattern.  

> **Chapter 4:** Question the data.

  

The presentation concludes with three reminders:

  

- **Question the pattern.**

- **Question the sample.**

- **Question the data.**

  

> **Good analysis starts before the model.**

  

---

  

# Meeting Discussion

  

## Discussion Topic 1 — Daniel Kahneman's Work on Human Judgment and Decision-Making

  

### Question / Topic

  

How do Daniel Kahneman's ideas explain the limitations of human intuition when interpreting data and making decisions?

  

### Main Points Discussed

  

We introduced the work of **Daniel Kahneman** and discussed how his research connects to the statistical-thinking concepts presented in Chapter 3.

  

We discussed his book **_Thinking, Fast and Slow_**, particularly the distinction between two modes of thinking:

  

- **System 1:** fast, automatic, and intuitive thinking.

- **System 2:** slower, more analytical, and deliberate thinking.

  

The discussion focused on how System 1 allows people to make quick judgments but can also lead to errors when reasoning about probability, randomness, sample size, and uncertainty. Statistical reasoning often requires the more deliberate style associated with System 2.

  

We connected this idea to the chapter's discussion of the **law of small numbers**. People often expect a small sample to closely resemble the population from which it was drawn, even though small samples naturally produce much greater variation.

  

The kidney-cancer example provided a practical illustration. When people hear that some rural counties have unusually high cancer rates, it is natural to immediately search for causal explanations such as healthcare access, lifestyle, or environmental factors. However, the fact that small rural counties also appear among those with the lowest rates suggests that much of the extremity can be explained by the increased variability associated with small populations.

  

We also introduced Kahneman's later book **_Noise_**, which examines unwanted variability in human judgment. While bias refers to a systematic tendency to be wrong in a particular direction, noise refers to inconsistency in decisions or judgments that ideally should be similar.

  

For example, two professionals may evaluate the same case and reach very different conclusions, or the same person may make different judgments depending on timing, context, or circumstances.

  

### Different Views

  

- **View 1:** Human intuition is useful and necessary for quick decisions, but statistical evidence should be used to check intuitive conclusions when uncertainty is important.

- **View 2:** Statistical reasoning can reduce certain judgment errors, but numbers alone are not sufficient; domain knowledge and context are also necessary for good decisions.

  

### Example Discussed

  

The **kidney-cancer rates** example was connected to Kahneman and Tversky's work on the law of small numbers. The group discussed how people naturally try to create causal explanations for extreme results even when those results may largely arise from random variation in small samples.

  

### Group Conclusion

  

The discussion highlighted that becoming more data-driven does not mean eliminating human judgment. Instead, statistical thinking provides tools for recognizing when intuition may be misleading.

  

A useful principle is:

  

> **Use intuition to generate questions, but use evidence and statistical reasoning to evaluate the answers.**

  

---

  

## Discussion Topic 2 — Challenger Case Study and Survivorship Bias

  

### Question / Topic

  

How is the Challenger example related to survivorship bias, and what does it teach us about analyzing incomplete data?

  

### Main Points Discussed

  

During the Challenger section, we discussed the broader concept of **survivorship bias** and its similarity to the problem demonstrated in the case study.

  

Survivorship bias occurs when an analysis focuses mainly on the observations that remain visible or satisfy some selection condition while overlooking observations that were excluded, disappeared, failed, or were otherwise not represented.

  

The Challenger example is not a textbook case of survivorship bias in the strictest sense, but it reflects a closely related statistical problem: **reasoning from a selected subset of the available data**.

  

The analysis emphasized shuttle flights in which O-ring distress had occurred. However, the flights in which no O-ring distress occurred were also essential because they provided information about how frequently failures occurred at different temperatures.

  

Looking only at failures answers a question such as:

  

> **At what temperatures have failures occurred?**

  

But it does not properly answer:

  

> **How does the probability of failure change with temperature?**

  

To answer the second question, both failures and non-failures are required.

  

The discussion emphasized the importance of the **denominator**. Observing several failures is not enough to evaluate risk unless we also know the total number of opportunities for failure.

  

We related this idea to survivorship bias because both problems involve asking:

  

> **What observations are missing from the story I am being shown?**

  

The same reasoning can occur in many data-science and business settings.

  

For example:

  

- Studying only successful startups while ignoring thousands of failed startups can make certain business strategies appear more effective than they really are.

- Studying only investment funds that still exist can overestimate historical investment performance if poorly performing funds disappeared.

- Analyzing only customers who remain with a company can hide important information contained in customers who churned.

- Studying only patients who completed a treatment can produce misleading results if people who discontinued treatment had systematically different outcomes.

  

### Different Views

  

- **View 1:** Visible or successful cases can still contain useful information, but conclusions drawn from them must acknowledge the missing observations.

- **View 2:** When the missing observations are systematically different from those included in the analysis, the resulting conclusions may be seriously biased.

  

### Example Discussed

  

The Challenger case showed that focusing mainly on flights where O-ring distress occurred could hide important information about the relationship between temperature and failure risk.

  

Once the flights with **zero incidents** were considered, the comparison became much more informative because the analysis could distinguish between temperatures associated with failures and temperatures associated with successful operation.

  

### Group Conclusion

  

The discussion reinforced one of the most important questions from Chapter 4:

  

> **What data am I not seeing?**

  

An observation in which nothing happened is still an observation. Successful cases, failures, zeros, missing cases, and excluded observations may all be necessary to understand the true data-generating process.

  

The broader takeaway was:

  

> **Before trusting the story told by the available data, investigate how observations entered the dataset—and which observations did not.**