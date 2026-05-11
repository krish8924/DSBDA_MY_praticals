# DSBDA Practical No. 5 — Simple Explanation

# Practical Topic
## Classification Using Naive Bayes Algorithm

---

# 1. Practical Cha Aim

Ya practical madhye aplyala:
- machine learning classification karaychi
- data train karaycha
- prediction karaycha
- accuracy check karaychi

Simple language madhe:

"Data la categories madhye classify karne using machine learning."

Example:
- Email spam aahe ka normal?
- Flower kontya species madhye aahe?
- Student pass/fail?

---

# 2. Main Concepts

| Term | Meaning | Simple Explanation |
|---|---|---|
| Classification | Category prediction | Label predict karne |
| Naive Bayes | ML algorithm | Probability based algorithm |
| Training Data | Learning data | Model shiknyasathi data |
| Testing Data | Checking data | Model test karayla |
| Prediction | Future result | Output guess |
| Accuracy | Correct predictions | Model kiti correct aahe |
| Feature | Input column | Input data |
| Target | Output column | Final result |

---

# 3. Libraries Used

---

## Code 1

```python
import pandas as pd
```

## Kay karte?
Pandas library import karte.

## Ka use keli?
Dataset handle karayla.

---

## Viva Question

### Q. Pandas ka use karto?
Data analysis sathi.

---

# Code 2

```python
from sklearn.model_selection import train_test_split
```

---

# Most Important Line ⭐

⚠️ Viva madhe frequently vichartat.

---

## Kay karte?
Dataset training ani testing madhye divide karte.

---

## Meaning

| Part | Meaning |
|---|---|
| train | Learning data |
| test | Checking data |
| split | Divide |

---

## Ka use keli?
Model performance check karayla.

---

## Viva Question

### Q. train_test_split ka use karto?
Training ani testing data separate karayla.

---

# Code 3

```python
from sklearn.naive_bayes import GaussianNB
```

---

# Most Important Algorithm ⭐

---

## Kay karte?
Naive Bayes algorithm import karte.

---

## Meaning

| Part | Meaning |
|---|---|
| sklearn | ML library |
| naive_bayes | Classification algorithms |
| GaussianNB | Naive Bayes model |

---

## Naive Bayes Meaning

Probability based classification algorithm.

---

## Ka use keli?
Classification problems solve karayla.

---

## Viva Question

### Q. Naive Bayes algorithm kay aahe?
Probability based classification algorithm.

---

# Code 4

```python
from sklearn.metrics import accuracy_score
```

---

## Kay karte?
Model chi accuracy calculate karte.

---

## Ka use keli?
Prediction kiti correct aahe te baghayla.

---

## Viva Question

### Q. accuracy_score ka use karto?
Model performance check karayla.

---

# Code 5

```python
df = pd.read_csv("data.csv")
```

---

## Kay karte?
Dataset load karte.

---

## Output

Data dataframe madhye store hoto.

---

# Code 6

```python
df.head()
```

---

## Kay karte?
First 5 rows display karte.

---

## Ka use keli?
Dataset preview baghayla.

---

# Code 7

```python
X = df.drop('target', axis=1)
```

---

# Important ML Concept ⭐

---

## Kay karte?
Input features select karte.

---

## Breakdown

| Part | Meaning |
|---|---|
| drop() | Column remove |
| target | Output column |
| axis=1 | Column operation |

---

## Meaning

Target sodun baki sagle columns inputs hotat.

---

## Viva Question

### Q. axis=1 meaning?
Column operation.

---

# Code 8

```python
y = df['target']
```

---

## Kay karte?
Target/output column select karte.

---

## Meaning

He actual result aahe.

---

## Viva Question

### Q. Target variable mhanje kay?
Final output column.

---

# Code 9

```python
X_train, X_test, y_train, y_test = train_test_split(X, y, test_size=0.2)
```

---

# Most Important ML Line ⭐

⚠️ Viva madhe nakkich vichartat.

---

## Kay karte?
Dataset training ani testing madhye divide karte.

---

## Breakdown

| Variable | Meaning |
|---|---|
| X_train | Training input |
| X_test | Testing input |
| y_train | Training output |
| y_test | Testing output |

---

## Meaning of test_size=0.2

20% data testing sathi.

80% data training sathi.

---

## Ka use keli?
Model properly evaluate karayla.

---

## Viva Question

### Q. test_size=0.2 meaning?
20% testing data.

---

# Code 10

```python
model = GaussianNB()
```

---

# Important Model Creation ⭐

---

## Kay karte?
Naive Bayes model create karte.

---

## Ka use keli?
Training ani prediction sathi.

---

## Viva Question

### Q. GaussianNB() kay create karte?
Naive Bayes model.

---

# Code 11

```python
model.fit(X_train, y_train)
```

---

# Most Important Line ⭐

⚠️ fit() viva madhe favourite question aahe.

---

## Kay karte?
Model ला training dete.

---

## Meaning

Model training data madhun patterns shikte.

---

## Viva Question

### Q. fit() function kay karte?
Model train karte.

---

# Code 12

```python
y_pred = model.predict(X_test)
```

---

# Prediction Step ⭐

---

## Kay karte?
Testing data sathi prediction karte.

---

## Meaning

Model guess karte ki output kay asel.

---

## Output

Predicted values.

---

## Viva Question

### Q. predict() kay karte?
New data sathi output predict karte.

---

# Code 13

```python
accuracy_score(y_test, y_pred)
```

---

# Most Important Evaluation Line ⭐

---

## Kay karte?
Model chi accuracy calculate karte.

---

## Accuracy Formula

genui{"math_block_widget_always_prefetch_v2":{"content":"Accuracy = \\frac{Correct\\ Predictions}{Total\\ Predictions}"}}

---

## Output Interpretation

Example:

```python
0.95
```

Mhanje 95% predictions correct aahet.

---

## Viva Question

### Q. Accuracy mhanje kay?
Correct predictions percentage.

---

# 4. Machine Learning Workflow

## Full Process

1. Dataset load
2. Features and target select
3. Train-test split
4. Model create
5. Model train
6. Prediction
7. Accuracy evaluation

---

# 5. Theory + Practical Connection

| Theory | Practical madhe use |
|---|---|
| Classification | Categories predict kelya |
| Naive Bayes | ML algorithm use kela |
| Training | Model shikavla |
| Testing | Model check kela |
| Accuracy | Performance measure keli |

---

# 6. Important Terms

## Feature
Input column.

Example:
- age
- marks
- sepal length

---

## Target
Output/result.

Example:
- pass/fail
- species
- spam/not spam

---

## Training
Model learning process.

---

## Testing
Model checking process.

---

# 7. Common Errors And Solutions

## Error 1

```python
ModuleNotFoundError
```

## Ka yeto?
scikit-learn install nahi.

## Solution

```python
pip install scikit-learn
```

---

## Error 2

```python
KeyError
```

## Ka yeto?
Wrong column name.

---

## Error 3

```python
ValueError
```

## Ka yeto?
Missing values kiwa wrong data shape.

---

# 8. Output Interpretation

| Output | Meaning |
|---|---|
| 0.95 | 95% accuracy |
| y_pred | Predicted values |
| X_train | Training inputs |
| X_test | Testing inputs |

---

# 9. Important Viva Questions

### Q. Classification mhanje kay?
Data categories madhye predict karne.

---

### Q. Naive Bayes algorithm kasha var based aahe?
Probability var.

---

### Q. fit() function kay karte?
Model training.

---

### Q. predict() function kay karte?
Prediction karte.

---

### Q. Accuracy ka important aahe?
Model performance measure karayla.

---

### Q. train_test_split ka use karto?
Training ani testing divide karayla.

---

# 10. Teacher Impress Points ⭐

- “Naive Bayes is a probability based classifier.”
- “Training data helps the model learn patterns.”
- “Testing data checks model performance.”
- “Accuracy measures prediction correctness.”
- “Machine learning models require training before prediction.”

---

# 11. Important Keywords

| Keyword | Meaning |
|---|---|
| Classification | Category prediction |
| Accuracy | Correctness |
| Feature | Input |
| Target | Output |
| Training | Learning |
| Prediction | Future guess |

---

# 12. Shortcut Memory Tricks

| Topic | Trick |
|---|---|
| fit() | Train |
| predict() | Predict |
| Accuracy | Correctness |
| X | Input |
| y | Output |
| Split | Divide data |

---

# 13. 2 Minute Revision

## Fast Revision

- Dataset load kela.
- Features ani target select kele.
- train_test_split ne data divide kela.
- GaussianNB model create kela.
- fit() ne training keli.
- predict() ne prediction keli.
- accuracy_score ne performance check keli.

---

# Final One Line Summary

"Ya practical madhye Naive Bayes classification algorithm वापरून data classify karun prediction ani accuracy analyze keli."

