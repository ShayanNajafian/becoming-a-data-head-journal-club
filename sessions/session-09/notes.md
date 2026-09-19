---
book: "Becoming a Data Head"
session: 9
date: "9/18/2026"
time: "10 pm"
presenter: "Shayan Najafian"
chapters: "13 & 14 & 15"

---

# Participants

- Sahar Matin
- Arman Ebrahimmi
- Alireza Ranjbar
- Yalda Tavakoli

---

# Session Summary

## Chapter 13 — Pitfalls and Biases

Chapter 13 focused on an important idea:

> **Even when the data is real, we can still reach the wrong conclusion.**

Sometimes the problem comes from the data itself, and sometimes it comes from the way humans interpret it. :contentReference[oaicite:0]{index=0}

---

### Survivorship Bias

**Survivorship bias** happens when we only study the cases that survived or remained visible and ignore the cases that disappeared.

For example, if we evaluate investment funds only by looking at the funds that still exist, performance may appear much better because poorly performing funds may already have closed. :contentReference[oaicite:1]{index=1}

The classic airplane example demonstrates the same idea.

Bullet holes on returning aircraft show where planes could be hit and still survive. The more important information may be the areas without bullet holes, because aircraft hit there may never have returned. :contentReference[oaicite:2]{index=2}

A useful question is:

> **Who is missing from this dataset?** :contentReference[oaicite:3]{index=3}

---

### Regression to the Mean

**Regression to the mean** describes the tendency for unusually extreme observations to be followed by more typical observations.

A very good or very bad result may partly contain random variation:

`Observed Performance = Underlying Ability + Noise`

Therefore, an extreme result should not automatically be treated as a permanent change. :contentReference[oaicite:4]{index=4}

The Madden Curse was used as an example.

An athlete may have an exceptional season, appear on the Madden cover, and then perform worse the following year. This does not necessarily require a "curse." The original season may simply have been unusually extreme and difficult to repeat. :contentReference[oaicite:5]{index=5}

This is also important when evaluating interventions.

If performance is unusually poor, a manager intervenes, and performance later improves, we should ask:

- Did the intervention really cause the improvement?
- Was the original result simply unusually bad?
- Is there a comparison group?

:contentReference[oaicite:6]{index=6}

---

### Simpson's Paradox

**Simpson's paradox** occurs when an overall trend tells one story while the trends inside meaningful subgroups tell the opposite story.

A hidden variable changes the interpretation. :contentReference[oaicite:7]{index=7}

The chapter used a medical-treatment example.

Overall:

- Traditional treatment → 78% success
- New treatment → 83% success

At first, the new treatment appears better. :contentReference[oaicite:8]{index=8}

But when patients are separated by stone size:

| Treatment | Small Stones | Large Stones | Overall |
|---|---:|---:|---:|
| Traditional | **93%** | **73%** | 78% |
| New | 87% | 69% | **83%** |

The traditional treatment performs better for both small and large stones, yet looks worse overall. :contentReference[oaicite:9]{index=9}

The reason is that the new procedure treated more easy cases, while the traditional procedure treated more difficult cases. :contentReference[oaicite:10]{index=10}

A useful question is:

> **What happens if we break the average into meaningful groups?** :contentReference[oaicite:11]{index=11}

---

### Effort Bias and the Sunk Cost Fallacy

The **sunk cost fallacy** occurs when people continue a bad project because they have already invested a large amount of:

- Time
- Money
- Resources
- Effort

For example:

> "We already spent six months and $500,000. We cannot stop now."

But past effort cannot be recovered, so it should not by itself determine the next decision. :contentReference[oaicite:12]{index=12}

A better checkpoint question is:

> **Knowing what we know today, would we start this project?** :contentReference[oaicite:13]{index=13}

---

### p-Hacking

**p-hacking** happens when many statistical tests are performed until one happens to produce a statistically significant result.

For example:

- Test 1 → p = .41
- Test 2 → p = .72
- Test 3 → p = .19
- Test 4 → p = .048
- Test 5 → p = .63

If only the `p = .048` result is reported, the evidence looks much stronger than it really is. :contentReference[oaicite:14]{index=14}

This creates a connection between p-hacking and survivorship bias:

**Many tests are performed → insignificant results disappear → significant result survives**

Therefore, an important question is:

> **How many tests were actually performed?** :contentReference[oaicite:15]{index=15}

---

### Confirmation Bias

**Confirmation bias** is the tendency to search for evidence that supports what we already believe while discounting evidence that challenges our beliefs.

This can become especially dangerous in data science when analysis is used to justify a decision that has already been made. :contentReference[oaicite:16]{index=16}

The movie *Pressure* was used to connect this idea to decision-making under uncertainty.

The example emphasized how pressure and incomplete information can make people more tempted to prefer evidence supporting the decision they already want. :contentReference[oaicite:17]{index=17}

---

### Algorithmic Bias

Machine-learning models learn patterns from historical data.

If historical data contains unfair or biased patterns, the model may reproduce those patterns.

Automation can then scale those existing problems.

The important lesson is:

> **Predictions are products of data and assumptions, not unquestionable truth.** :contentReference[oaicite:18]{index=18}

---

### Five Pitfalls, One Pattern

The major pitfalls can be summarized as:

| Pitfall | What might be missing? |
|---|---|
| Survivorship Bias | Missing cases |
| Regression to the Mean | Random variation |
| Simpson's Paradox | Hidden groups |
| Sunk Cost Fallacy | Future vs. past |
| p-hacking | Failed tests |

The common pattern is that we often see only part of the story and then construct a convincing explanation from incomplete information. :contentReference[oaicite:19]{index=19}

---

# Chapter 14 — Communication and People

Chapter 14 shifts attention away from algorithms.

Its main message is:

> **A technically correct model can still fail because of poor communication, poor collaboration, or poor implementation.**

The mathematics can be right while the final decision still goes wrong because context is lost or the message is unclear. :contentReference[oaicite:20]{index=20}

---

### Seven Communication Breakdowns

The chapter presents seven common situations.

**Postmortem — Expert called too late**

The team asks for technical expertise only after the project has already gone wrong.

**Storytime — Nuance removed**

The result is simplified so much that important uncertainty or context disappears.

**Telephone Game — Statistic loses context**

A statistical result passes through several people and gradually changes meaning.

**Into the Weeds — Technical but unclear**

The explanation contains lots of technical detail but does not help the audience understand what decision to make.

**Reality Check — Perfect but impossible**

A solution may be theoretically excellent but impossible to implement in the real organization.

**Takeover — Trust ignored**

A technical expert enters a project while ignoring domain knowledge, relationships, or existing expertise.

**Blowhard — Smart but unusable**

Someone may be technically brilliant but so difficult to communicate or collaborate with that their knowledge becomes much less useful.

:contentReference[oaicite:21]{index=21}

---

### Data Enthusiast, Data Cynic, or Data Head?

The chapter describes two extremes:

**Data Enthusiast**

> Data can solve everything.

**Data Cynic**

> Experience is more important than data.

Both positions miss something.

A **Data Head** takes a more balanced approach:

- Uses data where it is useful
- Questions the data carefully
- Combines analysis with domain knowledge
- Communicates with empathy

:contentReference[oaicite:22]{index=22}

---

# Main Takeaways

### Chapter 13

Good data analysis requires more than calculating statistics.

We need to ask:

- Who or what is missing?
- Could random variation explain the result?
- Are averages hiding important subgroups?
- Are we continuing because of past investment?
- How many statistical tests were performed?
- Are we looking for evidence that confirms what we already believe?
- Could historical bias be entering the model?

---

### Chapter 14

A good model is not enough.

Data scientists also need to think about:

- Communication
- Context
- Practical implementation
- Domain expertise
- Trust
- Collaboration
- The audience receiving the analysis

---

# Final Takeaway

The main idea connecting Chapters 13 and 14 is:

> **Do not let the data fool you.  
> Do not let yourself fool you.  
> Do not let communication destroy the analysis.**

Good data work requires **skepticism, humility, and clear communication**. :contentReference[oaicite:23]{index=23}