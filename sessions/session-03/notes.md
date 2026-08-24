# Journal Club — Session 3

**Book:** Becoming a Data Head  
**Session:** 3  
**Date:** 8/21/2026  
**Time:** 6 pm  
**Presenter:** Shayan Najafian  
**Chapter:** 5  

## Participants

- Arman Ebrahimi
- Sahar Matin
- Micheal Zamanian
- Setayesh Hoseini
- Payam Raisyan
- Alireza Asl Nemati

---

# 1. Chapter Summary

## Chapter 5 — Explore the Data

Chapter 5 introduces **Exploratory Data Analysis (EDA)**, the process of examining and understanding data before moving directly into modeling.

The central message of the presentation was:

> **Explore before you model.**

Before choosing an algorithm or building a predictive model, a data analyst should first ask:

- What is actually in the data?
- What looks unusual?
- What relationships may be hidden inside it?

---

## What Is Exploratory Data Analysis?

EDA was presented as an iterative process:

> **Explore → Question → Learn → Repeat**

It combines **summary statistics and visualizations** to build an understanding of the dataset.

A major point was that real-world analysis rarely follows a perfectly linear sequence. Analysts often discover something unexpected, reconsider an earlier assumption, ask a new question, and return to the data.

The process may therefore look more like:

**Problem → Data → Explore → New Question / New Limitation → Explore Again**

Different analysts may also take different exploratory paths even when they are given the same dataset.

EDA should therefore be understood as a **mindset**, rather than simply a checklist of charts and statistics.

---

## Why Business Context Matters

EDA cannot rely only on statistical techniques.

A pattern may be statistically interesting without being practically useful.

Therefore, good analysis requires a combination of:

> **Domain Knowledge + Business Context**

Data analysts need to understand what variables and patterns mean in the real-world environment from which the data originated.

A data scientist may understand the statistical properties of a dataset, while a domain expert may better understand whether those patterns make sense in practice.

This leads to an important principle:

> **Statistically interesting ≠ Practically useful**

---

## The Three Questions of EDA

The presentation organized exploratory analysis around three important questions:

1. **Can the data answer the question?**
2. **Did you discover any relationships?**
3. **Did you find new opportunities in the data?**

These questions provide a useful framework for deciding whether to continue with a project, modify the original problem, investigate something new, or potentially stop the project.

---

## Ames Housing Case Study

The chapter uses the **Ames Housing dataset** as its primary example.

The goal is to predict home sale prices using historical housing data.

The dataset contains:

- Hundreds of homes
- Approximately 80 variables
- Homes located in Ames, Iowa
- Observations from 2006 to 2011

The basic prediction problem can be thought of as:

**Information about a house → Predicted sale price**

However, before choosing a machine-learning algorithm, the first question should be:

> **Does the dataset contain the information we actually need?**

A model can only learn from the information represented in its data.

If important property types, conditions, or features are absent from the historical observations, the model may not be reliable when asked to predict those cases.

For example, if historical data contains only single-family homes, a model trained on that data may not reliably estimate the prices of condos or other property types it has never observed.

The broader lesson is:

> **A model cannot reliably learn a world that is not represented in its training data.**

---

## Do the Values Make Intuitive Sense?

After understanding which variables are available, analysts should examine their actual values.

An important EDA question is:

> **Does this make sense in the real world?**

Unexpected or impossible values should trigger investigation rather than being accepted simply because they exist in a dataset.

For example:

- A negative home price would be suspicious.
- A house with an impossible number of bedrooms would require investigation.
- A house recorded as having zero square feet may indicate a data-quality problem.

Software can calculate summary statistics automatically, but analysts still need to determine whether those statistics make sense in the context of the problem.

> **Software can calculate statistics. It cannot automatically tell us whether those statistics make sense.**

---

# Visualizations in EDA

Different visualizations answer different questions about the data.

---

## Histograms

A **histogram** helps answer:

> **What does the distribution look like?**

The Ames housing-price distribution is **right-skewed**.

Most homes are concentrated in the lower and middle price ranges, while a smaller number of expensive homes form a long tail on the right side of the distribution.

This also explains why the mean sale price is greater than the median sale price.

Approximately:

- **Mean sale price: $181,000**
- **Median sale price: $163,000**

The relatively small number of expensive homes pulls the mean upward.

This reinforces an earlier statistical idea:

> **The mean is more sensitive to extreme values than the median.**

Histograms can also reveal suspicious values, unusual clusters, or artificial limits in the data.

For example, if a large number of observations are recorded at exactly $500,000, it may indicate that values above $500,000 were capped during data collection.

---

## Box Plots

A **box plot** is useful for comparing numerical distributions across different groups.

In the Ames Housing example, sale prices were compared across different overall home-quality ratings.

The general pattern is clear:

> **Higher-quality homes tend to have higher sale prices.**

The main parts of a box plot include:

- The **line inside the box** represents the median.
- The **box** represents the middle 50% of observations.
- The **whiskers** extend toward the typical lower and upper values.
- The **dots outside the whiskers** represent potential outliers.

An important point is:

> **Outlier ≠ Error**

An unusually expensive home may be a legitimate observation.

It could have:

- A better location
- A larger lot
- Special architecture
- Additional features
- Other characteristics not fully represented by the quality score

Therefore, outliers should be investigated rather than automatically deleted.

---

## Bar Charts

A **bar chart** is useful for examining categorical variables and comparing category counts.

The Ames Housing example examined different types of electrical systems in homes.

Most homes belonged to the same electrical-system category.

At first, this might appear to be an uninteresting result.

However, it tells us something useful:

> **If almost every observation has the same value for a feature, that feature may provide little information for distinguishing between observations.**

In other words:

> **Lack of variation is itself information.**

---

## Line Charts

A **line chart** is useful when observations are ordered over time.

The presentation showed the number of homes sold over different months and years.

A repeating pattern appeared:

- Home sales increased during certain parts of the year.
- Sales decreased during other parts of the year.
- Similar patterns appeared repeatedly.

This is an example of **seasonality**.

Seasonality refers to patterns that regularly repeat according to time.

Examples include:

- Higher retail sales around holidays
- Increased ice-cream sales during summer
- Different electricity usage during summer and winter
- Differences in website traffic between weekdays and weekends

Identifying seasonality can be important when building models involving time.

---

## Scatter Plots

A **scatter plot** helps examine the relationship between two numerical variables.

In the housing example:

**X = First-floor square footage**

**Y = Sale price**

The scatter plot shows a general positive relationship:

> **Larger homes tend to sell for higher prices.**

However, the relationship is not perfect.

Some smaller homes sell for relatively high prices, while some larger homes sell for less than expected.

This demonstrates an important idea:

> **A relationship does not need to be a perfect rule to still be useful.**

Real-world data almost always contains variation around an overall pattern.

---

# Outliers and Missing Values

The presentation emphasized two important warnings:

> **Outlier ≠ Error**

> **Missing ≠ Zero**

Context determines what these values actually mean.

---

## Outliers

Outliers should not automatically be removed simply because they are different from most observations.

An unusual observation could represent:

- A data-entry error
- A measurement error
- A legitimate but unusual case
- A different subgroup within the population
- An important piece of information that the current model does not explain

The correct response to an outlier is usually:

> **Investigate first.**

---

## Missing Values

Missing values can also have different meanings.

Consider:

**Basement Size = Missing**

This could mean:

1. The house has a basement, but its size was not recorded.

or:

2. The house has no basement.

These situations are completely different.

If the second interpretation is correct, replacing the missing value with zero might make sense.

If the first interpretation is correct, replacing it with zero would introduce incorrect information into the dataset.

Therefore:

> **Data cleaning requires reasoning and domain knowledge, not only code.**

Many small cleaning decisions can accumulate and significantly affect the final dataset.

---

# Did You Discover Any Relationships?

The second major EDA question is:

> **Did you discover any relationships?**

Relationships can help analysts:

- Understand the data
- Choose useful predictors
- Identify redundant variables
- Generate new hypotheses
- Discover unexpected patterns

In the Ames Housing dataset, both home quality and square footage appear to have meaningful relationships with sale price.

When a dataset contains many numerical variables, one useful summary measure for identifying relationships is **correlation**.

---

# Understanding Correlation

Correlation measures how two numerical variables move together.

The Pearson correlation coefficient is commonly represented by **r**.

Its range is:

**-1 ≤ r ≤ 1**

### Positive Correlation

If:

**r > 0**

then as X increases, Y tends to increase.

Example:

**Home size ↑ → Sale price tends to ↑**

---

### Negative Correlation

If:

**r < 0**

then as X increases, Y tends to decrease.

Example:

**Vehicle weight ↑ → Fuel efficiency tends to ↓**

---

### Near-Zero Correlation

If:

**r ≈ 0**

there is little **linear** relationship between the variables.

The word **linear** is important.

A near-zero correlation does not necessarily mean that there is no relationship at all.

The relationship could be:

- Curved
- U-shaped
- Clustered
- Different across subgroups
- Influenced by another variable

---

## Correlation in the Ames Housing Data

The relationship between first-floor square footage and sale price has a correlation of approximately:

**r = 0.62**

This indicates a moderately strong positive linear relationship.

However, this does **not** mean:

- 62% of home price is caused by square footage.
- Increasing square footage by 1% causes price to increase by 62%.
- 62% of homes follow the relationship.

Correlation is not a percentage of causation.

---

## Correlation Is Not Slope

Another important distinction is:

> **Correlation does not measure how steep a relationship is.**

Two perfectly straight relationships can have completely different slopes while both having a correlation close to:

**r = 1**

Correlation measures how closely observations follow a linear pattern, not how steep that pattern is.

---

## Correlation and Redundant Variables

Correlation can also identify variables containing nearly the same information.

For example:

- Area in square feet
- Area in square meters

These two variables describe the same physical property using different units.

They would therefore be almost perfectly correlated.

Keeping both may add little new information.

---

# Correlation Can Mislead

Correlation compresses a large amount of information into a single number.

That is useful, but it also means information is lost.

Two datasets can have similar or even identical summary statistics while having completely different visual structures.

This is why analysts should not rely only on correlation coefficients.

> **Always visualize important relationships.**

A correlation value alone cannot reveal:

- Curved relationships
- Strange clusters
- Outliers
- Different subgroups
- Hidden structures

A near-zero correlation also does not automatically mean there is no interesting relationship.

---

## Anscombe's Quartet

**Anscombe's Quartet** is a famous example demonstrating the limitations of summary statistics.

Several datasets can have almost identical:

- Means
- Variances
- Correlations
- Regression lines

while looking dramatically different when visualized.

The lesson is simple:

> **Summary statistics are useful summaries, not replacements for looking at the data.**

---

## Datasaurus

The **Datasaurus** provides an even more memorable example.

The data points can literally form the shape of a dinosaur while having summary statistics similar to datasets with completely different patterns.

This reinforces the same principle:

> **Never let a summary statistic prevent you from looking at the actual data.**

---

# Correlation Does Not Imply Causation

One of the most important warnings in statistical analysis is:

> **If X moves with Y, it does not automatically mean X causes Y.**

A correlation tells us that two variables are associated.

It does not automatically tell us:

- Which variable causes the other
- Whether either variable causes the other
- Whether a third variable causes both
- Whether several variables interact together

---

## Confounding Variables

A **confounder** is another variable that may influence both variables being studied.

A classic example is the relationship between ice-cream sales and shark attacks.

We may observe:

**Ice-cream sales ↑**

and:

**Shark attacks ↑**

during the same periods.

But this does not mean:

**Ice-cream sales → Shark attacks**

A more reasonable explanation is:

**Hot weather → More ice-cream sales**

and:

**Hot weather → More swimming → More opportunities for shark attacks**

Therefore:

**Hot weather** acts as a confounding variable.

The correlation between ice-cream sales and shark attacks exists, but the obvious causal interpretation is wrong.

---

# Kissing and Self-Esteem Example

As an additional example of correlation and causation, the presentation introduced an example discussed in:

*Calling Bullshit: The Art of Skepticism in a Data-Driven World*  
by **Carl Bergstrom and Jevin West**.

The example was introduced by first asking:

> **What do you think is the average age of a first kiss?**

The reported average in the example was approximately:

> **15.5 years old**

The discussion was then connected to a relationship between **self-esteem and kissing**.

Suppose we observe that teenagers with higher self-esteem are more likely to have experienced a first kiss.

It may be tempting to conclude:

**Higher self-esteem → First kiss**

A possible explanation is:

**Higher self-esteem → More social confidence → Romantic relationship → Kissing**

However, this is not the only possible explanation.

---

## Reverse Causality

Perhaps the direction goes the other way:

**Kissing → Higher self-esteem**

Experiencing a romantic milestone might increase someone's confidence or feelings of social acceptance.

Therefore, the observed relationship could potentially involve reverse causality.

---

## A Third Variable

Another possibility is that a third variable influences both.

For example:

**Romantic relationship → Self-esteem**

and:

**Romantic relationship → Kissing**

In this case, the relationship between self-esteem and kissing may partly result from both being related to romantic involvement.

---

## Feedback Loop

The relationship may even form a feedback loop:

**Higher self-esteem**  
↓  
**More social confidence**  
↓  
**Romantic relationship**  
↓  
**Kissing**  
↓  
**Higher self-esteem**  
↺

Reality may therefore be more complicated than a single causal arrow.

The main lesson is:

> **Correlation can reveal that variables are related, but it does not automatically tell us which causal mechanism produced that relationship.**

A useful summary is:

> **Correlation reveals the relationship. Causality requires a stronger argument.**

---

# Did You Find New Opportunities in the Data?

The third major EDA question is:

> **Did you find new opportunities in the data?**

EDA does not only help answer the original question.

While exploring a dataset, an analyst may discover:

- A new business problem
- A previously unknown customer segment
- An unexpected pattern
- A new prediction opportunity
- A limitation that changes the original problem

This can cause the project to move in a completely new direction.

However, discovering an interesting pattern does not automatically mean it is worth pursuing.

The analyst should return to the original business question:

> **Is this problem actually valuable to solve?**

---

# EDA Can Change the Original Problem

Sometimes exploration reveals that the original goal is too broad.

For example, suppose the original goal is:

> Predict the sale price of every type of property.

But EDA reveals that the dataset contains only a limited group of residential homes from Ames, Iowa.

The project may need to be redefined.

Instead of pretending the original goal is still possible, a better question may be:

> Predict sale prices for homes similar to those represented in the available dataset.

Changing the original problem based on what the data reveals is not failure.

It is part of good data analysis.

---

# EDA Can Stop a Bad Project

EDA may reveal that the available data simply cannot answer the original question.

In that situation, the correct decision may be:

> **Do not build the model.**

Although this may appear disappointing, stopping an unreliable project early can save significant time, money, and effort.

Therefore:

> **A successful data project does not always end with a model.**

Sometimes the most valuable conclusion is:

> **We should not build this model with the data we currently have.**

---

# Overall Takeaway — Chapter 5

Chapter 5 teaches that analysts should understand their data **before trying to model it**.

The three central questions are:

1. **Can the data answer the question?**
2. **Did you discover any relationships?**
3. **Did you find new opportunities in the data?**

EDA helps reveal:

- What the data contains
- What the data is missing
- Whether values make sense
- How variables are distributed
- Which observations are unusual
- Which variables are related
- Whether correlations may be misleading
- Whether the original business problem needs to change
- Whether the project should continue at all

The final message of the presentation was:

> **Explore before you model.**

And sometimes:

> **The best model is no model at all.**

---

# Meeting Discussion

## Discussion Topic 1 — Understanding Box Plots

### Question / Topic

How should we interpret the different elements of a box plot, especially the box, median line, whiskers, and individual dots?

### Main Points Discussed

During the presentation, we spent additional time discussing the structure and interpretation of **box plots**.

Some participants searched for more information during the session and helped explain the different components of the visualization to the group.

We discussed that:

- The **line inside the box** represents the median.
- The **box** represents the middle 50% of the observations, between the first and third quartiles.
- The **whiskers** extend toward the lower and upper range of the typical observations.
- The **individual dots beyond the whiskers** usually represent potential outliers.

An important part of the discussion was that a point being identified as an outlier does **not** automatically mean that it is an error.

For example, in the Ames Housing dataset, an unusually expensive house may appear as a dot outside the whiskers while still being a completely valid observation.

### Group Conclusion

Box plots provide a compact way to understand the distribution of numerical data and compare groups, but their elements should always be interpreted in the context of the underlying data.

The main takeaway was:

> **An outlier is something to investigate, not something to automatically remove.**

---

## Discussion Topic 2 — Introducing *Calling Bullshit*

### Question / Topic

How does *Calling Bullshit: The Art of Skepticism in a Data-Driven World* relate to the ideas discussed in *Becoming a Data Head*?

### Main Points Discussed

I introduced the book *Calling Bullshit: The Art of Skepticism in a Data-Driven World* by **Carl Bergstrom and Jevin West** and briefly discussed its overall structure and chapters.

The book focuses on developing skepticism when evaluating quantitative claims, statistics, visualizations, algorithms, and other forms of evidence presented as data-driven.

We connected its themes to Chapter 5 of *Becoming a Data Head*, particularly the idea that analysts should not accept numbers, correlations, or visualizations at face value.

The discussion also connected the two books through topics such as:

- Correlation and causation
- Misleading visualizations
- The importance of context
- Questioning how evidence is presented
- Looking for alternative explanations

The **kissing and self-esteem example** was introduced as an illustration of how an observed association can be compatible with several different causal explanations.

### Group Conclusion

Both books encourage a similar habit of mind:

> **Do not simply consume data — question the story being constructed from it.**

Statistical results and visualizations can provide useful evidence, but interpreting them correctly requires skepticism, context, and awareness of alternative explanations.

---

## Discussion Topic 3 — How Data Visualizations Can Mislead Without Context

### Question / Topic

Can a visualization present real data and still lead us toward the wrong conclusion when important context is missing?

### Main Points Discussed

We discussed an example comparing the **average age at death of musicians across different musical genres**.

In the visualization, musicians associated with genres such as **hip-hop and jazz appeared to have a lower average age at death** than musicians from some older musical traditions.

At first glance, the graph could encourage a simple causal interpretation:

> **Perhaps these musical genres are somehow more dangerous, or their lifestyles cause musicians to die younger.**

However, this interpretation ignores an important piece of context: **the historical age of the genres themselves**.

Hip-hop, for example, is a relatively young musical genre compared with many older genres. Because it emerged much more recently, its earliest generations of musicians have simply had less calendar time in which to reach very old ages.

This creates an important problem when comparing the average age at death across genres. If a genre has existed for a shorter period, there are naturally fewer musicians from that genre who could already have died at ages such as 80 or 90.

Therefore, a lower observed average age at death does not automatically mean:

> **The genre causes musicians to die younger.**

It may instead reflect differences in the **historical period, age of the genre, and generations of musicians represented in the available data**.

We discussed how the visualization itself may contain technically correct numbers while still encouraging a misleading interpretation if the viewer does not know how the dataset was constructed or understand the historical context behind the categories.

This example connects directly to the themes of Chapter 5:

- Visualize the data, but do not stop at the visualization.
- Ask whether the comparison itself is fair.
- Consider alternative explanations for observed patterns.
- Investigate the population represented by each category.
- Avoid turning an association into a causal explanation without sufficient evidence.

### Group Conclusion

The discussion demonstrated that a visually striking difference between groups does not automatically reveal the reason for that difference.

The key lesson was:

> **A visualization can accurately display the data while still encouraging an inaccurate story about why the pattern exists.**

Before interpreting a graph, we should therefore ask:

> **What additional information do I need before I can explain this pattern?**

In this example, understanding the **historical age of the musical genres and the generations represented in the dataset** substantially changes how the visualization should be interpreted.