---
book: "Becoming a Data Head"
session: 8
date: "9/17/2026"
time: "10 pm"
presenter: "Shayan Najafian"
chapters: "12"

---

# Participants

- Alireza Ranjbar
- Arman Ebrahimi
- Soroush Hosseini
- Rosita Jamalzade
- Sahar Matin
- Alireza Asl Nemati

---

# Session Summary

## Chapter 12 — Deep Learning

Chapter 12 introduced **deep learning** and explained how neural networks learn patterns from data.

The main idea is that neural networks are inspired loosely by biological neurons, but they should not be thought of as actual artificial brains.

They are mathematical models that learn relationships between inputs and outputs by adjusting numerical parameters. :contentReference[oaicite:0]{index=0}

---

### The Basic Neuron

A simple artificial neuron receives several inputs.

For example, when predicting whether an internship applicant receives an offer, the inputs might include:

- GPA
- Year
- Major
- Extracurricular activities

These inputs are combined to produce an output such as:

`P(Offer) = 0.82`

This creates a connection between neural networks and ideas such as logistic regression. :contentReference[oaicite:1]{index=1}

Inside the neuron, each input is multiplied by a **weight**:

`z = w₁x₁ + w₂x₂ + ... + b`

where:

- `x` → input
- `w` → weight
- `b` → bias
- `z` → weighted sum / pre-activation value

The result is then passed through an **activation function** to produce the neuron's output. :contentReference[oaicite:2]{index=2}

The weights determine how strongly different inputs influence the prediction, while the bias shifts the neuron's output.

Training a neural network therefore means finding useful values for these weights and biases. :contentReference[oaicite:3]{index=3}

---

### Backpropagation

Neural networks learn by comparing their predictions with the correct answers.

A simplified training cycle is:

Prediction  
↓  
Calculate Error  
↓  
Send Error Backward  
↓  
Adjust Parameters  
↓  
Make a Better Prediction

This process is called **backpropagation**. :contentReference[oaicite:4]{index=4}

More precisely, backpropagation calculates how much each parameter contributed to the prediction error.

An optimization algorithm such as **gradient descent** can then use this information to update the weights.

So:

**Backpropagation → calculates the gradients**

**Optimizer → uses those gradients to update the parameters**

This process is repeated many times during training.

---

### Hidden Layers and Representation Learning

A neural network can contain layers between its input and output layers called **hidden layers**.

These layers combine simpler inputs into more useful internal representations.

For example:

`GPA + Major + Extracurriculars → Achievement`

`Year + Extracurriculars → Experience`

`Major + Skills → Skillset`

The important idea is that the network can learn useful intermediate representations instead of requiring humans to manually design every feature. :contentReference[oaicite:5]{index=5}

This is called **representation learning**.

In traditional machine learning:

**Humans often create useful features → Model learns from them**

In deep learning:

**The model can learn useful features itself**

This is one reason deep learning works particularly well with complex data such as images, audio, video, and text. :contentReference[oaicite:6]{index=6}

A neural network becomes **deep** when it contains multiple hidden layers stacked together. :contentReference[oaicite:7]{index=7}

---

### Why Deep Learning Became Successful

Neural networks are not a new idea.

They existed long before the recent AI boom, but earlier systems were limited by insufficient data and computing power. :contentReference[oaicite:8]{index=8}

Modern deep learning became much more successful when three things came together:

- Large amounts of data
- Better algorithms
- Powerful computing hardware, especially GPUs

The modern deep-learning revolution was therefore largely about **scale**. :contentReference[oaicite:9]{index=9}

More data can help large neural networks continue improving, but more data is only useful when the data actually contains meaningful signal. :contentReference[oaicite:10]{index=10}

---

### Images as Numbers

Computers do not see images the same way humans do.

A grayscale image can be represented as a matrix of pixel values.

For example:

`8 × 8 image = 64 numerical values`

The neural network learns patterns from these numbers rather than directly understanding the visual object in the human sense. :contentReference[oaicite:11]{index=11}

Color images become even larger because each pixel usually contains three channels:

- Red
- Green
- Blue

A 10-megapixel image therefore contains roughly **30 million numerical values**. :contentReference[oaicite:12]{index=12}

This makes specialized architectures useful for image processing.

---

### Convolutional Neural Networks

**Convolutional Neural Networks (CNNs)** are designed particularly well for images.

Instead of connecting every pixel directly to every neuron, CNNs use filters that scan small local regions of an image.

These filters can learn patterns such as:

- Edges
- Corners
- Curves
- Textures

Later layers combine simpler patterns into increasingly complex representations.

For example:

`Edges → Shapes → Parts → Objects`

This hierarchical feature learning is one reason CNNs became very successful in computer vision. :contentReference[oaicite:13]{index=13}

---

### Pooling

CNNs often produce large **feature maps**.

Pooling reduces their size while trying to preserve useful information.

A common technique is **max pooling**, where the model examines a small region and keeps its largest value.

The intuition is:

**Convolution finds local patterns.**

**Pooling summarizes those patterns.**

This reduces the amount of information that later layers need to process. :contentReference[oaicite:14]{index=14}

---

### Sequence Data and RNNs

Images are not the only type of complex data.

For language, the order of information matters.

For example:

`At breakfast, I drink orange ____`

and

`My cousin lives in Orange ____`

require previous words to determine whether the missing word might be **juice** or **County**. :contentReference[oaicite:15]{index=15}

**Recurrent Neural Networks (RNNs)** were designed to handle this type of sequential information.

They allow previous information in a sequence to influence later predictions.

This gives the network a simple form of memory and makes it useful for language and other sequential data. :contentReference[oaicite:16]{index=16}

---

### Data Comes First

Before choosing a complicated deep-learning architecture, an important question is:

> **Do we actually have the right data?**

Deep-learning models often require large amounts of labeled examples.

The labels must also represent the actual task we want the model to learn.

Poor labels produce poor models, and no model can learn a relationship that does not exist in the data. :contentReference[oaicite:17]{index=17}

---

### Transfer Learning

Sometimes we do not need to train a neural network completely from scratch.

With **transfer learning**, we can start from a model that was already trained on another large dataset.

For image models, for example, early layers may already know how to detect generic features such as:

- Edges
- Curves
- Shapes

We can keep some of those learned representations and retrain later layers for our own task.

This can be particularly useful when labeled data is limited. :contentReference[oaicite:18]{index=18}

---

### Deep Learning Is Not Always the Best Model

Using deep learning simply because it is powerful or popular is not a good model-selection strategy.

Deep learning is particularly strong with complex perceptual data such as:

- Images
- Text
- Audio
- Video

But for smaller structured datasets, models such as decision trees or other traditional machine-learning techniques may perform just as well or better. :contentReference[oaicite:19]{index=19}

The correct question is therefore not:

> "Can we use deep learning?"

but:

> **"Is deep learning appropriate for this data and problem?"**

---

### Architecture Choices

Building a neural network involves many decisions.

Examples include:

- How many layers?
- How many neurons?
- Which activation functions?
- How should overfitting be controlled?
- How should performance be validated?

Deep learning is therefore not simply a matter of pressing a "train" button. :contentReference[oaicite:20]{index=20}

---

### The Black Box Problem

As neural networks become larger and more complex, they also become harder to interpret.

Modern networks can contain millions or even billions of parameters.

Although they may make accurate predictions, explaining exactly **why** a particular prediction occurred can become difficult.

This becomes especially important when models are used for high-stakes decisions. :contentReference[oaicite:21]{index=21}

---

### AI, Machine Learning, and Deep Learning

The chapter also clarified the relationship between several commonly confused terms.

A useful hierarchy is:

**Artificial Intelligence**

↓  

**Machine Learning**

↓  

**Deep Learning**

Deep learning is therefore a subset of machine learning, while machine learning itself is part of the broader field of artificial intelligence. :contentReference[oaicite:22]{index=22}

---

### Big Tech's Data Advantage

Large technology companies have another major advantage besides powerful algorithms:

**Data.**

Years of collecting:

- Images
- Search behavior
- Clicks
- Speech
- Text
- User interactions

can produce enormous datasets for training machine-learning systems.

In some situations, better data can be more valuable than a more sophisticated algorithm. :contentReference[oaicite:23]{index=23}

---

# Discussion Notes

## Discussion 1 — What Is `z` Inside a Neuron?

During the session, we discussed the equation:

`z = w₁x₁ + w₂x₂ + ... + b`

`z` is usually called the **weighted sum** or **pre-activation value**.

The process can be understood as:

Inputs  
↓  
Weighted Sum (`z`)  
↓  
Activation Function  
↓  
Output

The weights determine how strongly each input contributes to `z`, while the bias shifts the value before it reaches the activation function.

---

## Discussion 2 — Is Backpropagation an Algorithm?

We also discussed how to categorize backpropagation.

Backpropagation is an **algorithm used during neural-network training**.

Its job is to efficiently calculate how the model's error changes with respect to each parameter.

An important distinction is:

**Backpropagation calculates gradients.**

**Gradient descent or another optimizer updates the parameters.**

So the complete training process is roughly:

Forward Pass  
↓  
Calculate Loss  
↓  
Backpropagation  
↓  
Optimizer Updates Weights  
↓  
Repeat

---

## Discussion 3 — Pooling

We discussed pooling in more detail using **max pooling** as an example.

Pooling divides a feature map into small regions and summarizes each region.

With max pooling, the largest value is retained.

For example:

`2 × 2 region → keep the maximum value`

This reduces the size of the representation while preserving strong detected features.

A useful way to remember the difference is:

> **Convolution asks: "What feature is here?"**

> **Pooling asks: "Can I summarize this region?"**

---

# Main Takeaways

### Neural Networks

A neuron combines:

**Inputs + Weights + Bias → Activation → Output**

Training means learning useful values for the parameters.

---

### Deep Learning

Adding multiple hidden layers allows neural networks to learn increasingly useful representations directly from data.

This ability to perform **representation learning** is one of deep learning's most important strengths.

---

### Different Data, Different Architectures

Different types of data require different approaches.

**Images → CNNs**

**Sequential data → RNNs**

Deep learning architecture should match the structure of the problem.

---

### Data Still Matters

A complicated model cannot compensate for:

- Poor labels
- Irrelevant data
- Missing signal
- Bad experimental design

Deep learning still depends heavily on the quality of the data.

---

### Complexity Has a Cost

More complicated models can provide powerful predictions, but they can also create:

- Higher computational requirements
- Greater risk of overfitting
- More difficult architecture decisions
- Lower interpretability

Therefore, deep learning should not automatically be the first solution to every machine-learning problem.

---

# Final Takeaway

The central idea of Chapter 12 is:

> **Deep learning allows machines to learn complex representations from data, but powerful models do not remove the need for good data, careful model selection, human judgment, and responsibility.**

Deep learning is powerful because it can automatically learn useful representations from complex data.

But the model is still only one part of the complete system.

The final questions remain:

> **Who does this result affect?**

> **Am I OK with that?**