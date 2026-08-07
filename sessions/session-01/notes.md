

---
book: "Becoming a Data Head"
session: 1
date: "8/6/2026"
time: "10 pm"
presenter: "Shayan Najafian"
chapters: "1 and 2"
participants:
  - "Arman Ebrahimi"
  - "Micheal Zamanian"
  - "Sahar Matin"
  - "Nazanin Javadi"
  - "Setayesh Hoseini"
  - "Mohanna Miri"
  - "Alireza Ranjbar"
---

# 1. Chapter Summary


## Chapter 1 — What Is the Problem?

### Main Idea

Chapter 1 emphasizes that a data project should begin with a **clearly defined and meaningful problem**, not with a technology, analytical technique, or desired output.

The central idea of the presentation is:

> **Problem first. Data second.**

Before analyzing data or choosing a tool, the team needs to understand what problem it is actually trying to solve and why solving that problem matters.

### Why Data Projects Fail

Several common reasons for failure were highlighted:

- Starting with technology instead of the problem
- Unclear business value
- Wrong or incomplete data
- No clear definition of when the project is finished
- Producing results that nobody actually uses

A project can therefore be technically successful while still failing to create useful business value.

### The Five Questions

Before starting a data project, five important questions should be asked:

1. **Why is this problem important?**
2. **Who will this problem affect?**
3. **What if the right data does not exist?**
4. **When is the project over?**
5. **What if we do not like the results?**

#### 1. Why is this problem important?

The team should determine whether the problem is genuinely worth solving.

Important questions include:

- Why does this matter?
- What keeps the organization awake at night?
- Is this actually a new problem?
- Has someone already solved it?
- What return on investment is expected?
- What is the potential value or “size of the prize”?

The objective is to connect the data project to a real organizational need.

#### 2. Who will this problem affect?

It is important to identify the people whose work or decisions will change after the project is completed.

A useful thought experiment is to pretend that the project has already been completed and ask:

- **Can we use the answer?**
- **Whose work will change?**

If nobody knows what action they would take after receiving the result, the project may not be solving a useful problem.

#### 3. What if the right data does not exist?

The available data may not be sufficient to answer the intended question.

Possible problems include:

- The necessary data does not exist.
- Available data measures the wrong thing.
- Important groups are missing.
- Data is incomplete or unreliable.
- New data needs to be collected.
- The original problem needs to be narrowed or changed.

Having data does not necessarily mean having the **right data**.

#### 4. When is the project over?

The definition of completion should be clear before the project starts.

The team should establish:

- The final deliverable
- The success metric
- The expected business outcome
- The project deadline
- Whether ongoing maintenance is required
- Who owns the result after delivery

Without a clear definition of success and completion, projects may continue without creating additional value.

#### 5. What if we do not like the results?

Data may produce conclusions that contradict what stakeholders expected or wanted.

Examples include:

- A marketing campaign did not work.
- A popular product is not profitable.
- A leader's preferred strategy performs poorly.
- Data contradicts the original business assumption.

A data project should therefore be designed to discover what the evidence shows, rather than simply confirm an existing belief.

---

### Two Major Warning Signs

Two warning signs may indicate that a project has started from the wrong place.

#### Methodology Focus

This occurs when the team begins with an analytical technique or technology.

Examples:

- “We need artificial intelligence.”
- “Let's use sentiment analysis.”
- “We should build a machine-learning model.”

The problem should determine the methodology, rather than selecting a methodology first and then searching for a problem to apply it to.

#### Deliverable Focus

This occurs when the team begins by deciding what it wants to build.

Examples:

- “We need a dashboard.”
- “We need an app.”
- “We need a real-time reporting system.”

The deliverable is only useful if it helps solve a meaningful problem or improve a decision.

---

### Case Study — Customer Perception Dashboard

The chapter's case study demonstrates both warning signs.

The organization decided to use **sentiment analysis** to understand customer perception and created a dashboard showing positive and negative sentiment over time.

The project successfully produced the dashboard, but the larger question was whether the output actually helped the organization make better decisions.

The case illustrates the difference between:

> **Successfully building something**

and

> **Successfully solving a problem**

The case therefore reinforces the importance of defining the business problem and understanding how the result will actually be used.

---

### Workplace Barriers for Data Scientists

The presentation also highlighted several workplace barriers reported by data scientists:

- Lack of a clear question — **30.4%**
- Results not used by decision-makers — **24.3%**
- Lack of domain-expert input — **19.6%**
- Unrealistic expectations of project impact — **15.8%**
- Difficulty integrating findings into decisions — **13.6%**

These problems show that successful data work is not only a technical challenge. Clear questions, stakeholder involvement, realistic expectations, and integration into decision-making are also important.

### Key Takeaway

> A successful data project begins by defining a meaningful problem, identifying who will use the result, checking whether the appropriate data exists, defining success, and being willing to accept unexpected conclusions.


---

## Chapter 2 — What Is Data?

### Main Idea

Chapter 2 introduces the basic language needed to understand and discuss data.

The chapter focuses on:

- What data represents
- How datasets are organized
- Different types of data
- How data can be structured
- How data is collected
- Basic summary statistics

Understanding these characteristics is important before attempting to analyze or interpret a dataset.

---

### From Data to Wisdom

The presentation uses the following hierarchy:

**Data → Information → Knowledge → Wisdom**

- **Data** represents the raw recorded facts.
- **Information** comes from organizing and putting data into context.
- **Knowledge** develops when information is interpreted and patterns are understood.
- **Wisdom** involves using that understanding to make appropriate decisions.

The important idea is that collecting data is only the beginning. The ultimate value comes from transforming data into understanding and using that understanding to support decisions.

---

### Understanding a Dataset

Datasets usually contain rows and columns, but different professional groups may use different terminology.

#### Rows may be called:

- Observations
- Records
- Tuples
- Trials

#### Columns may be called:

- Features
- Variables
- Fields
- Attributes
- Predictors

Understanding these different terms helps people from different technical backgrounds communicate with one another.

---

### Know Your Audience's Language

Different disciplines may use different words for the same concept.

For example:

- A statistician may say **variable**.
- A machine-learning professional may say **feature**.
- A database professional may say **field**.

Effective data communication therefore requires understanding the terminology used by the audience rather than assuming everyone uses the same vocabulary.

---

### Data Types

The presentation divides data into two main categories:

1. **Numeric data**
2. **Categorical data**

#### Numeric Data

Numeric data represents quantities.

##### Continuous Data

Continuous data can take values across a range.

Examples:

- Temperature
- Height
- Weight
- Time
- Distance

##### Discrete Data

Discrete data generally represents countable quantities.

Examples:

- Number of customers
- Number of cars
- Number of complaints
- Number of purchases

---

### Categorical Data

Categorical data represents membership in a group or category.

#### Ordered / Ordinal Data

The categories have a meaningful order.

Examples:

- Small, medium, large
- Poor, fair, good, excellent
- Satisfaction ratings from 1 to 10

#### Unordered / Nominal Data

The categories do not have an inherent ranking.

Examples:

- Online, television, print
- Yes, no
- Country
- Department
- Product type

---

### Structured and Unstructured Data

#### Structured Data

Structured data follows a predefined organization.

Examples:

- Spreadsheets
- Database tables
- Transaction records
- Customer lists

#### Unstructured Data

Unstructured data does not naturally follow the traditional rows-and-columns format.

Examples:

- Written reviews
- Emails
- Photographs
- Videos
- Audio recordings
- Social-media posts

The distinction is important because different types of data require different approaches to storage and analysis.

---

### How Data Is Collected Changes the Claim

An important distinction is made between **observational** and **experimental** data.

#### Observational Data

> Records what happens.

The researcher or organization observes events without deliberately changing the situation.

#### Experimental Data

> Tests what causes it.

An experiment deliberately changes something in order to investigate its effect.

This distinction is important because the way data is collected affects the conclusions that can reasonably be made from it.

---

### Mean, Median, and Mode

The presentation introduces three common measures used to summarize data.

#### Mean

The arithmetic average of the values.

It is affected by unusually large or small observations.

#### Median

The middle observation after the values have been ordered.

It is less sensitive to extreme observations than the mean.

#### Mode

The value that occurs most frequently.

Comparing these measures can provide intuition about the distribution of the data and whether extreme observations may be influencing the mean.

### Key Takeaway

> Before analyzing data, understand what kind of data you have, how it is organized, how it was collected, and what its summary statistics actually tell you.




---

# Meeting Discussion

## Discussion Topic 1 — How Should ID Numbers Be Classified?

### Question / Topic

Is an **ID number** a numeric data type or a categorical data type?

### Main Points Discussed

- An ID may consist entirely of digits, but this does not necessarily make it **numeric data** in the statistical sense.
- The important question is whether arithmetic operations on the values have a meaningful interpretation.
- If the numbers are used only as labels to distinguish individuals or objects, they behave like **nominal categorical data**.
- Sometimes an ID contains meaningful information, such as the year of entry. In that case, the meaningful component can be extracted and analyzed separately.

### Different Views

- **View 1 — Numeric:**  
  Since an ID is represented using numbers, it could be considered numeric from a storage or programming perspective.

- **View 2 — Categorical:**  
  If the ID is only used to identify an individual or object, it should be treated as categorical data because the numerical magnitude has no meaningful interpretation.

- **View 3 — A special identifier:**  
  An ID can also be considered an identifier rather than an ordinary numeric or categorical variable. Its purpose is primarily to uniquely distinguish records.

### Example Discussed

Consider a student ID.

If part of the student ID represents the student's **entry year**, that component contains meaningful information.

For example:

`2023-14582`

Here:

- `2023` may represent the **entry year** and can be extracted as a meaningful variable.
- `14582` may simply be a unique identifier and may have no quantitative meaning.

On the other hand, if students are simply assigned IDs such as:

`1, 2, 3, 4, ...`

the numbers usually indicate only identity. Student `400` is not meaningfully "twice as much" as student `200`, and calculating the average student ID would normally have no useful interpretation.

### Group Conclusion

> **An ID should generally not be treated as numeric data simply because it is written using numbers. Its classification depends on what the number represents.**

If the value is used only to identify records, it is best treated as a **nominal categorical identifier**. If some part of the ID encodes meaningful information, such as an entry year, that information should preferably be **extracted into a separate variable** and analyzed according to its own meaning.

> [!important]
> **Key intuition:**  
> Ask whether arithmetic on the numbers makes sense.  
> If adding, averaging, or comparing their magnitude has no meaningful interpretation, the variable is probably not truly numeric.
> 


