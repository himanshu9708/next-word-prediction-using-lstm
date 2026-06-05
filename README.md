# next-word-prediction-using-lstm
# FAQ Text Generation using LSTM

## Overview

This project implements a word-level text generation model using TensorFlow and Keras. The model is trained on a dataset of frequently asked questions (FAQs) related to the CampusX Data Science Mentorship Program and can generate text continuations based on a user-provided prompt.

The project demonstrates the complete NLP pipeline:

* Text preprocessing
* Tokenization
* Sequence generation
* Padding
* LSTM-based language modeling
* Text generation
* Training visualization

---

## Features

* Converts FAQ text into training sequences.
* Creates next-word prediction samples.
* Uses an Embedding layer for word representations.
* Trains an LSTM neural network for language modeling.
* Generates text word-by-word from a given prompt.
* Visualizes training accuracy and loss.

---

## Tech Stack

* Python
* TensorFlow / Keras
* NumPy
* Matplotlib

---

## Dataset

The dataset consists of FAQ content related to the CampusX Data Science Mentorship Program, including:

* Course fee information
* Course duration
* Curriculum details
* Session recordings
* Placement assistance
* Eligibility criteria

---

## Model Architecture

```text
Input Layer (56 tokens)

Embedding Layer
- Vocabulary Size: 283
- Embedding Dimension: 150

LSTM Layer
- Units: 150
- Dropout: 0.2

Dense Output Layer
- Units: 283
- Activation: Softmax
```

---

## Training

### Loss Function

```python
categorical_crossentropy
```

### Optimizer

```python
adam
```

### Metric

```python
accuracy
```

### Epochs

```python
50
```

---

## Workflow

### 1. Text Preprocessing

* Tokenize FAQ text.
* Build vocabulary.
* Convert text into numerical sequences.

### 2. Sequence Creation

Generate training samples for next-word prediction.

Example:

```text
What is the course fee

Input: What
Target: is

Input: What is
Target: the

Input: What is the
Target: course
```

### 3. Padding

All sequences are padded to a fixed length of 57 tokens.

### 4. Model Training

Train the LSTM model on generated input-target pairs.

### 5. Text Generation

Provide a seed sentence and predict the next word repeatedly.

Example:

```python
text = "what is the fee"
```

Generated output:

```text
what is the fee for the data science mentorship program
```

---

## Results

The notebook plots:

* Training Accuracy vs Epochs
* Training Loss vs Epochs

These visualizations help monitor model learning behavior and convergence.

---

## Future Improvements

* Add Bidirectional LSTM layers.
* Use validation data during training.
* Implement Early Stopping.
* Train on a larger FAQ dataset.
* Replace one-hot encoding with sparse labels.
* Experiment with GRU and Transformer architectures.

---

## Installation

```bash
pip install tensorflow numpy matplotlib
```

---

## Run the Project

```bash
jupyter notebook
```

Open the notebook and execute all cells sequentially.

---

## Learning Outcomes

This project demonstrates:

* NLP preprocessing
* Tokenization
* Sequence modeling
* Word embeddings
* LSTM networks
* Text generation
* Model evaluation and visualization

```
```
