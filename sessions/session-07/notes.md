book: "Becoming a Data Head"

session: 7

date: "9/11/2026"

time: "10 pm"

presenter: "Shayan Najafian"

chapters: "10 and 11"

---

## Participants

- Alireza Ranjbar
- Arman Ebrahimi
- Michael Zamanian
- Rosita Jamalzade
- Sahar Matin

---

# Session Summary

## Chapter 10 — Classification Models

Chapter 10 focused on **classification**, where the goal is to predict a category rather than a numerical value.

We discussed the difference between:

- Regression → predicts numbers
- Classification → predicts known categories
- Clustering → discovers groups without predefined labels

The main classification example was predicting whether an internship applicant should receive an interview.

### Logistic Regression

Logistic regression produces a probability between 0 and 1.

For example:

`P(Interview) = 0.82`

The logistic or sigmoid function converts the model's score into a probability.

However, probability is not yet a final decision.

A threshold is required:

- Probability ≥ threshold → Positive
- Probability < threshold → Negative

A threshold of 0.5 is common, but it is not a universal rule.

Changing the threshold changes the balance between:

- False Positives
- False Negatives

Therefore, choosing a threshold depends on the real-world cost of different mistakes.

---

### Decision Trees and Ensemble Models

Decision trees make predictions through a sequence of rules.

They are relatively easy to interpret but can easily **overfit** the training data.

The chapter also introduced ensemble models:

- **Random Forest:** combines predictions from many different trees.
- **Gradient Boosting:** builds trees sequentially, with each new tree trying to improve previous errors.

These methods can improve predictive performance but are usually harder to interpret than a single decision tree.

---

### Evaluating Classification Models

Accuracy alone can be misleading.

For example, if 99.5% of users do not click an advertisement, a model that always predicts "No Click" would still achieve 99.5% accuracy.

Therefore, classification models should also be evaluated using tools such as:

- Baseline models
- Confusion matrices
- False Positives
- False Negatives
- Recall / Sensitivity
- Specificity

The main lesson was:

> **The important question is not only how often the model is correct, but also what kinds of mistakes it makes.**

---

# Chapter 11 — Text Analytics

Chapter 11 introduced **text analytics** and the challenge of converting human language into numerical representations that machine-learning algorithms can process.

The basic pipeline is:

Raw Text  
↓  
Preprocessing  
↓  
Numerical Representation  
↓  
Machine-Learning Model  
↓  
Prediction or Insight

---

### Bag of Words

Bag of Words represents text using word counts.

For example:

`"Data science is fun"`

might become:

- data → 1
- science → 1
- is → 1
- fun → 1

The problem is that Bag of Words ignores word order and much of the context.

For example:

> Jordan loves hotdogs but hates hamburgers.

and

> Jordan hates hotdogs but loves hamburgers.

contain nearly the same words but communicate opposite meanings.

---

### N-Grams

N-grams preserve some local word order.

Instead of using only individual words:

- loves
- hotdogs

we can use:

- loves hotdogs
- hates hotdogs

This adds context, although it also increases the number of features.

---

### Word Embeddings

Word embeddings represent words as numerical vectors.

Words appearing in similar contexts tend to receive similar representations.

This allows models to capture relationships between words better than simple word counts.

The chapter gives the intuitive example:

`Beef - Cow + Pig ≈ Pork`

The important idea is that embeddings learn patterns of word usage from data.

Their meaning therefore depends strongly on the context and corpus used for training.

---

### Topic Modeling

Topic modeling is an unsupervised technique used to discover hidden themes in documents.

Unlike simple clustering, a document can belong partly to multiple topics.

For example:

- 60% Defense
- 40% Space

The algorithm discovers patterns of words that frequently appear together, but humans still need to interpret and name the resulting topics.

---

### Text Classification

Once text has been converted into numerical features, classification algorithms can be applied.

Examples include:

- Spam / Not Spam
- Positive / Negative sentiment
- News categories

This creates a direct connection between Chapters 10 and 11:

**Text → Numerical Features → Classification Model → Predicted Category**

---

# Discussion Notes

## Discussion 1 — Recall vs. Precision

During the meeting, we expanded the discussion of classification metrics and talked about **Recall** and **Precision**.

### Recall

Recall asks:

> **Of all the actual positive cases, how many did we successfully identify?**

\[
Recall = \frac{TP}{TP + FN}
\]

Recall is especially important when missing a positive case is costly.

Examples:

- Disease screening
- Fraud detection
- Safety-system failures

For example, in medical screening, a false negative may mean missing a patient who actually has the disease.

A useful way to remember recall is:

> **Don't miss the positives.**

---

### Precision

Precision asks:

> **Of everything predicted as positive, how many predictions were actually correct?**

\[
Precision = \frac{TP}{TP + FP}
\]

Precision becomes important when false alarms are expensive.

Examples:

- Blocking legitimate financial transactions
- Marking legitimate emails as spam
- Sending too many cases to human investigators

A useful way to remember precision is:

> **When the model says positive, how often is it right?**

---

### Choosing Between Them

There is no universally best metric.

The appropriate metric depends on the consequences of the errors.

For example:

| Problem | Metric that may receive more attention |
|---|---|
| Cancer screening | Recall |
| Spam filtering | Precision may be important |
| Fraud detection | Both can matter |
| Search systems | Balance of Precision and Recall |

This discussion connected directly to the classification threshold.

Changing the threshold affects:

- False Positives
- False Negatives
- Precision
- Recall

Therefore, choosing a metric should start with the real-world question:

> **Which mistake is more expensive?**

---

## Discussion 2 — Structured and Unstructured Data

While discussing text analytics, we talked about different types of unstructured data.

Examples included:

- Text
- Images
- Video
- Audio / Voice

Then we asked whether there were other types of data that we had not mentioned.

One participant brought up **signals**, which led to an interesting discussion about whether signals should always be considered structured or unstructured.

---

### Structured Signals

Some signals naturally have a clear numerical and temporal structure.

Examples:

#### ECG Signals

An electrocardiogram records numerical measurements at known times.

#### EEG Signals

Brain-wave measurements are recorded numerically from known channels and timestamps.

#### Temperature Sensors

A sensor may record one temperature value every few seconds.

#### Vehicle Speed

Vehicle speed can be recorded at predefined time intervals.

These can often be represented as time-series tables:

| Time | Value |
|---|---:|
| t1 | 72 |
| t2 | 74 |
| t3 | 71 |

Because the measurements have known variables, timestamps, and numerical values, they can often be treated as **structured time-series data**.

---

### Unstructured Signals

Audio and voice recordings are commonly treated as unstructured data.

Examples:

- Audio files
- Recorded human speech
- Environmental sound recordings

Although digital audio is technically stored as numerical samples, the useful semantic information is not directly available as predefined fields.

For example, an audio waveform does not immediately give us:

- Spoken words
- Speaker identity
- Emotion
- Intent
- Topic

Some kind of feature extraction or representation is required first.

A typical pipeline might be:

Raw Audio  
↓  
Waveform / Spectrogram  
↓  
Features or Embeddings  
↓  
Machine-Learning Model

---

### Representation Matters

An important conclusion from this discussion was that the distinction between **structured and unstructured data is not always absolute**.

An image is technically a structured matrix of pixel values.

Audio is technically a sequence of numerical samples.

Video is technically a sequence of image frames.

However, these are generally called unstructured because the **semantic information we actually care about is not already represented as explicit analytical fields**.

For example, pixels do not automatically provide columns such as:

- Person
- Car
- Emotion
- Object type

Similarly, audio samples do not automatically provide:

- Words
- Speaker
- Meaning
- Emotion

Therefore, a useful distinction is:

> **Structured data already has an explicit schema describing the variables we want to analyze.**

while:

> **Unstructured data usually requires another representation or feature-extraction step before its meaning can be used by traditional analytical models.**

---

### Other Data Types Mentioned

The discussion can also be extended to several other categories.

#### Time-Series Data

Examples:

- Stock prices
- Weather measurements
- IoT sensors
- Heart rate
- Server monitoring

These are generally structured because variables and timestamps are clearly defined.

#### Graph / Network Data

Examples:

- Social networks
- Transportation networks
- Communication networks
- Citation networks

Graph data is organized around:

- Nodes
- Edges
- Relationships

It does not naturally fit into ordinary row-column tables.

#### Semi-Structured Data

Examples:

- JSON
- XML
- Web logs
- Emails

An email is a particularly good example because it contains both structured and unstructured information.

Structured:

- Sender
- Receiver
- Timestamp
- Subject

Unstructured:

- Email body

So one dataset can contain several different types of information simultaneously.

---

# Main Takeaways

### Chapter 10

Classification is not simply about predicting a category.

We also need to understand:

- Probabilities
- Thresholds
- False Positives
- False Negatives
- Evaluation metrics
- Baselines
- Real-world costs of mistakes

---

### Chapter 11

Text analytics begins with representation.

Before applying machine-learning algorithms, language must first be converted into numerical features.

Different representations preserve different amounts of information:

**Bag of Words → word frequency**

**N-Grams → some word order**

**Word Embeddings → relationships between words**

**Topic Modeling → hidden themes across documents**

---

# Final Takeaway

The main idea connecting both chapters is:

> **Models calculate, but humans decide what the numbers mean and what counts as a good decision.**

Classification requires human decisions about thresholds and error costs.

Text analytics requires human decisions about representation, preprocessing, context, and interpretation.

The algorithm is only one part of the complete data-science process.
