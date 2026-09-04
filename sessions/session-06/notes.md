book: "Becoming a Data Head"

session: 6

date: "9/4/2026"

time: "6 pm"

presenter: "Shayan Najafian"

chapters: "8 and 9"

participants:

- "Sahar Matin"
- "Alireza Ranjbar"
- "Alireza Asl Nemati"

# 1. Chapter Summary

## Chapter 8 — Search for Hidden Groups

Chapter 8 introduces **unsupervised learning**, where we try to discover useful patterns or groups in data without having predefined labels or known answers.

The presentation focused on two main ideas:

- **Dimensionality Reduction**
- **Clustering**

The main intuition is that unsupervised learning helps us explore structure that may already exist inside a dataset.

---

## Customer Segmentation Without Labels

The presentation used a customer-segmentation example.

Imagine we have information about 10,000 customers, including:

- Age
- Income
- Purchase frequency
- Average spending
- Product preferences

However, we do not already have customer labels such as:

- Premium customers
- Discount seekers
- Occasional shoppers

Instead, an unsupervised-learning algorithm can search for groups based on similarities in customer behavior.

An important point is:

> **The algorithm finds mathematical groups; humans usually interpret and name those groups afterward.**

:contentReference[oaicite:0]{index=0}

---

## Rows, Columns, and Dimensionality

In a dataset:

- **Rows = observations**
- **Columns = features**
- **Number of features = dimensionality**

For example, a customer dataset may contain age, income, purchases, and spending as different dimensions.

As the number of features increases, the dataset becomes more difficult to visualize and analyze.

---

## The Curse of Dimensionality

More features do not always make a dataset easier to understand.

As dimensionality increases:

- Data becomes more sparse
- Distance between observations can become less informative
- More data is required
- Models may overfit more easily

A useful way to summarize this is:

> **The space grows faster than our data.**

This motivates the use of dimensionality reduction.

:contentReference[oaicite:1]{index=1}

---

## Dimensionality Reduction

Dimensionality reduction means:

> **Many original features → fewer new features**

while trying to preserve most of the useful information.

For example, several customer-related variables such as:

- Purchase frequency
- Average order value
- Loyalty years

could potentially be summarized into a broader dimension such as:

**Customer Value**

The goal is to simplify the dataset without losing too much important structure.

---

## Principal Component Analysis — PCA

The presentation introduced **Principal Component Analysis (PCA)** as a dimensionality-reduction technique.

PCA creates new dimensions called **principal components**.

The main intuition is:

- **PC1 captures the largest amount of variance**
- **PC2 captures the next largest amount**
- Later components capture progressively less

The principal components are created from **weighted combinations of the original features**.

:contentReference[oaicite:2]{index=2}

---

## PCA as a Camera Rotation

A useful intuition for PCA is to imagine looking at the same object from different angles.

Different views preserve different amounts of useful information.

PCA searches for a useful mathematical "view" of the dataset where important variation becomes easier to represent.

---

## PCA Example — Athletic Ability

The presentation used an example with approximately 30 athletic measurements.

These measurements could contain broader hidden dimensions such as:

- Strength
- Speed
- Stamina
- Health

For example, a component interpreted as **Strength** might be created from:

**Strength ≈ 0.6(Push-ups) + 0.5(Deadlifts) + 0.4(Sit-ups) + ...**

The weights represent how strongly each original feature contributes to the new component.

:contentReference[oaicite:3]{index=3}

---

## Explained Variance

PCA also tells us how much variation each principal component captures.

In the athlete example:

- PC1 → 33%
- PC2 → 28%
- PC3 → 21%
- PC4 → 9%

Together, the first four components preserve approximately:

**91%**

of the information represented by the original 30 features.

:contentReference[oaicite:4]{index=4}

---

## PCA Can Mislead

PCA is useful, but it should not be interpreted blindly.

Important warnings include:

- **High variance ≠ important**
- Components may not have simple meanings
- Scaling matters
- Humans decide how many components to keep

A variable can vary greatly without being important to the real-world problem.

Therefore:

> **PCA finds what varies most, not necessarily what matters most.**

:contentReference[oaicite:5]{index=5}

---

## Clustering

While PCA focuses mainly on reducing or combining **columns**, clustering focuses on grouping **rows**.

Examples include:

- Customers → Customer segments
- Stores → Geographic regions
- Athletes → Athlete types

Clustering asks:

> **Which observations are similar to each other?**

---

## What Does "Similar" Mean?

Similarity must be defined mathematically.

Depending on the problem, similarity might depend on:

- Age
- Income
- Behavior
- Location
- Spending patterns

Different definitions of similarity can produce different clusters.

This means clustering is not completely objective.

:contentReference[oaicite:6]{index=6}

---

## Distance

Clustering algorithms need a numerical definition of how close two observations are.

One common choice is **Euclidean distance**, which represents straight-line distance between points.

Another possible distance measure introduced in the presentation was **Manhattan distance**, which measures distance by adding differences across dimensions.

The choice of distance metric can influence the final clustering.

---

## k-Means Clustering

**k-means** is a popular clustering algorithm.

The value:

**k**

represents the number of clusters we want to create.

For example:

**200 stores + k = 6 → 6 geographic clusters**

The basic process is:

1. Choose k starting centers.
2. Assign each point to its nearest center.
3. Move each center to the average position of the points assigned to it.
4. Reassign the observations.
5. Repeat until the clusters stabilize.

:contentReference[oaicite:7]{index=7}

---

## Scaling Matters

Suppose our features are:

- Age = 36
- Number of children = 3
- Income = 100,000

If we calculate distances directly, income may dominate simply because its numerical scale is much larger.

Therefore, features often need to be standardized before clustering.

> **The scale of variables can change the clusters that the algorithm discovers.**

:contentReference[oaicite:8]{index=8}

---

## Hierarchical Clustering

The presentation also introduced **hierarchical clustering**.

Instead of immediately deciding on final groups, hierarchical clustering gradually combines similar observations into larger and larger groups.

For example:

**Contemporary Jazz + Classic Jazz → Jazz**

The result can be visualized using a **dendrogram**, which shows the hierarchy of clusters.

:contentReference[oaicite:9]{index=9}

---

## Overall Takeaway — Chapter 8

The most important message of Chapter 8 is:

> **"Unsupervised" learning still requires supervision.**

Humans still make important decisions about:

- Which features to include
- How features should be scaled
- Which distance metric to use
- How many clusters to create
- How many principal components to keep
- How the results should be interpreted

The algorithm can find patterns, but humans must decide whether those patterns are useful and meaningful.

:contentReference[oaicite:10]{index=10}

---

# Chapter 9 — Understand the Regression Model

Chapter 9 moves from **unsupervised learning** to **supervised learning**.

In supervised learning, historical examples already contain known answers.

The goal is to learn relationships between features and a known target and then use those relationships to make predictions for new observations.

---

## Supervised Learning

The basic process is:

**Features + Known Target → Algorithm → Model → Prediction**

For example, historical housing data may contain:

- Square footage
- Number of bedrooms
- Year built
- Sale price

The model learns from houses whose sale prices are already known and then predicts prices for new houses.

:contentReference[oaicite:11]{index=11}

---

## Regression vs. Classification

The presentation distinguished two common supervised-learning problems.

### Regression

The target is numerical.

Examples:

- House → $350,000
- Predict future sales

### Classification

The target is categorical.

Examples:

- Email → Spam / Not Spam
- Transaction → Fraud / Not Fraud

:contentReference[oaicite:12]{index=12}

---

## Linear Regression

Linear regression models the relationship between a feature and a numerical target.

A simple regression equation can be written as:

**ŷ = b₀ + b₁x**

where:

- **x** = input feature
- **ŷ** = predicted value
- **b₀** = intercept
- **b₁** = slope or coefficient

The main goal is to find a line that describes the relationship between the input and the target.

---

## Which Line Is Best?

Many different lines might appear to fit a scatter plot reasonably well.

Linear regression uses a systematic approach rather than simply drawing a line by eye.

The chosen line attempts to minimize the prediction errors between:

**Actual values**

and:

**Predicted values**

:contentReference[oaicite:13]{index=13}

---

## Residuals and Least Squares

A **residual** is the difference between the observed value and the model's prediction.

**Residual = Actual - Predicted**

Linear regression minimizes the total squared residuals:

**SSE = sum((Actual - Predicted)²)**

Errors are squared partly because positive and negative errors would otherwise cancel each other.

For example:

**+4 + (-4) = 0**

even though both predictions were wrong.

After squaring:

**4² + (-4)² = 32**

:contentReference[oaicite:14]{index=14}

---

## Understanding Regression Coefficients

The lemonade example used:

**Sales = 1.03 × Temperature - 71.07**

The coefficient:

**1.03**

means that a one-unit increase in temperature is associated with approximately:

**$1.03 higher predicted sales.**

However:

> **Associated with ≠ caused by**

A regression relationship does not automatically establish causality.

:contentReference[oaicite:15]{index=15}

---

## R-Squared

**R²** describes how much variation in the target the regression model explains relative to a simple baseline.

For example:

**R² ≈ 0.788**

means that the model explains approximately:

**78.8% of the observed variation**

relative to the baseline model.

However:

> **High R² does not automatically mean the model is correct, causal, or good at predicting new observations.**

:contentReference[oaicite:16]{index=16}

---

## Multiple Regression

Real-world outcomes usually depend on several variables.

A multiple regression model may look like:

**House Price = b₀ + b₁(Lot Area) + b₂(Year Built) + b₃(Floor Area) + ...**

An important phrase when interpreting multiple regression is:

> **Holding the other included variables constant.**

This means we try to estimate the relationship of one feature with the target while accounting for the other features included in the model.

:contentReference[oaicite:17]{index=17}

---

# Common Regression Failures

The presentation emphasized that regression can produce misleading results when the model or data is poorly constructed.

---

## Failure #1 — Omitted Variables

Suppose a model finds:

**Shoe Size → Reading Ability**

It might appear that people with larger shoes read better.

However, **age** affects both:

- Older children tend to have larger feet.
- Older children also tend to read better.

If age is omitted from the model, shoe size may incorrectly appear important.

The key lesson is:

> **A model cannot learn from an important variable that was never included.**

:contentReference[oaicite:18]{index=18}

---

## Failure #2 — Multicollinearity

Suppose a regression model contains:

- Temperature in Celsius
- Temperature in Fahrenheit

These two variables contain almost exactly the same information.

Regression may struggle to separate their individual relationships with the target.

This problem is called **multicollinearity**.

It makes individual coefficients difficult to interpret.

:contentReference[oaicite:19]{index=19}

---

## Failure #3 — Data Leakage

Suppose we want to predict the selling price of a house **before it sells**.

The dataset contains:

**Initial Offer**

This variable may strongly predict the final sale price.

However, if that information is unavailable when we actually need to make the prediction, using it during training creates **data leakage**.

The model may appear extremely accurate during development because it effectively had access to future information.

:contentReference[oaicite:20]{index=20}

---

## Failure #4 — Extrapolation

Suppose a lemonade model was trained using temperatures between:

**80°F and 86°F**

Then we ask it to predict sales at:

**0°F**

The linear equation may predict negative sales.

This is mathematically possible but practically meaningless.

The lesson is:

> **Models do mathematics. They do not have common sense.**

Predictions far outside the range represented in the training data should be treated cautiously.

:contentReference[oaicite:21]{index=21}

---

## Failure #5 — Not Everything Is Linear

Linear regression assumes that a straight-line relationship provides a useful approximation.

However, real relationships may be:

- Curved
- Exponential
- Seasonal
- Threshold-based

Sometimes linear regression is simply the wrong tool.

The memorable rule from the presentation was:

> **Don't fit a straight line through a banana.**

:contentReference[oaicite:22]{index=22}

---

## Failure #6 — Overfitting

A model can perform extremely well on its training data and still perform poorly on new observations.

This is called **overfitting**.

An overfit model learns the noise and specific details of the training dataset instead of learning a general pattern.

Therefore:

> **Perfect training performance ≠ good prediction.**

:contentReference[oaicite:23]{index=23}

---

## Training Set vs. Test Set

To evaluate whether a model generalizes, the dataset can be divided into:

### Training Set

Used to build the model.

### Test Set

Used to evaluate the model on observations it has never seen.

The real question is not:

> **How well did the model memorize the training data?**

but:

> **How well does it perform on new data?**

:contentReference[oaicite:24]{index=24}

---

## Actual vs. Predicted

Another useful way to evaluate regression models is to compare:

**Actual values**

with:

**Predicted values**

If the predictions are good, observations should generally lie close to the diagonal in an actual-vs.-predicted plot.

The presentation emphasized:

> **Do not trust R² alone. Look at the prediction errors and visualizations as well.**

:contentReference[oaicite:25]{index=25}

---

## Explaining or Predicting?

Regression models can be used for two different goals.

### Explanation

> **Why does X relate to Y?**

Here, interpretation of coefficients, omitted variables, and multicollinearity becomes very important.

### Prediction

> **How accurately can we predict Y for new observations?**

Here, performance on unseen data and avoiding overfitting become more important.

These goals are related, but they are not identical.

A model may predict well without being easy to explain, and a highly interpretable model may not always be the most accurate predictor.

:contentReference[oaicite:26]{index=26}

---

## Connection Between Chapters 8 and 9

The two chapters provide the basic conceptual map of machine learning.

### Chapter 8

**No known answers → Find structure**

### Chapter 9

**Known answers → Learn relationships**

Together, they introduce the two major learning paradigms:

- **Unsupervised learning**
- **Supervised learning**

:contentReference[oaicite:27]{index=27}

---

## Overall Takeaway — Chapters 8 & 9

The presentation concluded with an important idea:

> **Algorithms calculate, humans judge.**

The main lessons were:

1. **Unsupervised learning searches for structure without predefined labels.**
2. **Dimensionality reduction simplifies high-dimensional data.**
3. **PCA creates new components that capture important variation.**
4. **Clustering groups similar observations together.**
5. **Scaling, distance metrics, and human choices affect clustering results.**
6. **Supervised learning learns from historical examples with known targets.**
7. **Regression predicts numerical outcomes by learning relationships between variables.**
8. **High R² or good training performance does not guarantee a good model.**
9. **Omitted variables, multicollinearity, leakage, extrapolation, and overfitting can create misleading results.**
10. **Prediction does not imply causation.**

The final message was:

> **Machine learning does not remove human judgment. It moves human judgment to different parts of the process.**

:contentReference[oaicite:28]{index=28}