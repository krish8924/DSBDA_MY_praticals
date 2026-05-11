# DSBDA Practical No. 6 — Naive Bayes Classification (Iris Dataset)

---

# Practical Aim (Simple Language)

या practical मध्ये आपण:

- Iris flower dataset वापरतो
- Flower ची species predict करतो
- Machine Learning वापरून classification करतो
- Naive Bayes algorithm वापरतो
- Model किती correct आहे ते check करतो

## Main Goal:
Flower च्या measurements वरून तो कोणत्या species चा आहे हे ओळखणे.

---

# Concept First — Simple Understanding

## Iris Dataset म्हणजे काय?

हा famous ML dataset आहे.

त्यात flower चे features आहेत:

| Feature | Meaning |
|---|---|
| sepal_length | बाहेरील पाकळीची लांबी |
| sepal_width | बाहेरील पाकळीची रुंदी |
| petal_length | आतील पाकळीची लांबी |
| petal_width | आतील पाकळीची रुंदी |

Target column:

| Column | Meaning |
|---|---|
| species | Flower type |

---

# Naive Bayes म्हणजे काय?

हा एक Machine Learning Classification Algorithm आहे.

तो probability वापरून prediction करतो.

## Simple idea:
“या measurements असलेलं flower कोणत्या species मध्ये येण्याची शक्यता जास्त आहे?”

---

# Full Code Explanation

---

# 1) Import Libraries

```python
import numpy as np
import pandas as pd
```

---

## काय करते?

Libraries import करते.

---

## Meaning

| Library | Use |
|---|---|
| numpy | Mathematical operations |
| pandas | Data handling |

---

## Why used?

Dataset हाताळण्यासाठी.

---

## Output वर effect

कोणताही direct output नाही.

पण पुढचा code चालण्यासाठी important आहे.

---

## Viva Point ⭐

### ही line विचारू शकतात:

```python
import pandas as pd
```

### Oral Answer:

“Pandas library dataframe handle करण्यासाठी वापरतात.”

---

## Alternative

```python
import pandas
```

पण `pd` short form जास्त वापरतात.

---

# 2) Import ML Functions

```python
from sklearn.model_selection import train_test_split
from sklearn.naive_bayes import GaussianNB
from sklearn.metrics import confusion_matrix, accuracy_score, precision_score, recall_score
```

---

# Explanation

## train_test_split

Dataset दोन भागात divide करतो.

| Part | Use |
|---|---|
| Train Data | Model शिकतो |
| Test Data | Model check करतो |

---

## GaussianNB

Naive Bayes algorithm.

Gaussian म्हणजे normal distribution वापरतो.

---

## confusion_matrix

Prediction किती correct/incorrect ते दाखवतो.

---

## accuracy_score

Overall accuracy.

---

## precision_score

Correct positive predictions.

---

## recall_score

Actual positives किती पकडले.

---

## Viva Question

### Q: sklearn म्हणजे काय?

Answer:
Machine Learning library in Python.

---

# 3) Read Dataset

```python
df = pd.read_csv("Data files/IRIS.csv")
df
```

---

# काय करते?

CSV file load करते.

---

# Important Terms

| Term | Meaning |
|---|---|
| read_csv() | CSV file वाचते |
| df | dataframe variable |

---

# DataFrame म्हणजे काय?

Table format data.

Excel सारखा.

---

# Output

Rows आणि columns दिसतील.

---

# Viva Important ⭐

```python
pd.read_csv()
```

### Oral Answer:
CSV file dataframe मध्ये convert करते.

---

# Possible Error

## Error:

```python
FileNotFoundError
```

## Why?
File path चुकीचा आहे.

## Solution:
Correct path द्या.

---

# 4) Check Null Values

```python
df.isnull().sum()
```

---

# काय करते?

Missing values check करते.

---

# Breakdown

| Part | Meaning |
|---|---|
| isnull() | Null values शोधते |
| sum() | Count करते |

---

# Output Interpretation

जर सर्व values `0` असतील:

✅ Dataset clean आहे.

---

# Viva Question

### Q: Null values म्हणजे काय?

Answer:
Missing data.

---

# 5) Display Columns

```python
df.columns
```

---

# काय करते?

सर्व column names दाखवते.

---

# Output

```python
Index(['sepal_length', ...])
```

---

# Why Important?

Features select करताना use होते.

---

# 6) Feature & Target Selection

```python
x=df[['sepal_length', 'sepal_width', 'petal_length', 'petal_width']]
y=df['species']
```

---

# Very Important Concept ⭐

| Variable | Meaning |
|---|---|
| x | Input features |
| y | Output/target |

---

# Why Used?

ML model ला:
- Input data लागतो
- Output label लागतो

---

# Output Effect

Model शिकायला तयार होतो.

---

# Viva Important ⭐

### ही line खूप important:

```python
y=df['species']
```

### Oral Answer:
“Species target variable आहे.”

---

# 7) Train Test Split

```python
x_train, x_test, y_train, y_test = train_test_split(x, y, test_size=0.25, random_state=0)
```

---

# Full Simple Explanation

Dataset split होतो.

| Variable | Meaning |
|---|---|
| x_train | Training input |
| x_test | Testing input |
| y_train | Training output |
| y_test | Testing output |

---

# test_size=0.25

25% testing data.

75% training data.

---

# random_state=0

Same output मिळण्यासाठी.

---

# Viva Question ⭐

### Q: Train-test split का करतात?

Answer:
Model train आणि test separately करण्यासाठी.

---

# Possible Error

## Error:
Shape mismatch

## Reason:
Input/output rows equal नसतील.

---

# 8) Create Model

```python
model = GaussianNB()
```

---

# काय करते?

Naive Bayes model तयार करते.

---

# Object म्हणजे काय?

Model memory मध्ये तयार होतो.

---

# Viva Important ⭐

### Q: GaussianNB का वापरतो?

Answer:
Continuous numeric data साठी.

---

# 9) Train Model

```python
model.fit(x_train, y_train)
```

---

# Very Important ⭐⭐⭐

Model ला training data शिकवतो.

---

# fit() म्हणजे काय?

Learning process.

---

# Theory Connection

Machine learning मध्ये:
Training phase इथे होते.

---

# Viva Question

### Q: fit() function काय करते?

Answer:
Model ला training data वर train करते.

---

# 10) Prediction

```python
y_pred = model.predict(x_test)
```

---

# काय करते?

Test data वर prediction करते.

---

# Output

Predicted species मिळतात.

---

# Important Concept

| Variable | Meaning |
|---|---|
| y_test | Actual output |
| y_pred | Predicted output |

---

# Viva Important ⭐

### Q: predict() function use काय?

Answer:
New data वर prediction करण्यासाठी.

---

# 11) Confusion Matrix

```python
cm = confusion_matrix(y_test, y_pred)
cm
```

---

# काय करते?

Correct आणि wrong predictions दाखवते.

---

# Confusion Matrix Basics

| Term | Meaning |
|---|---|
| TP | True Positive |
| TN | True Negative |
| FP | False Positive |
| FN | False Negative |

---

# Output Interpretation

Diagonal values मोठ्या असतील तर:

✅ Model good आहे.

---

# Viva Question ⭐

### Q: Confusion matrix use काय?

Answer:
Model performance check करण्यासाठी.

---

# 12) Accuracy

```python
a=accuracy_score(y_test,y_pred)
print("accuracy Score:",a)
```

---

# Meaning

Model किती percent correct predict करतो.

---

# Example

Accuracy = 0.97

म्हणजे:
97% predictions correct आहेत.

---

# Viva Important ⭐

### Q: Accuracy म्हणजे काय?

Answer:
Correct predictions चे percentage.

---

# 13) Error Score

```python
e=1-a
print("error Score:",e)
```

---

# Meaning

किती predictions wrong आहेत.

---

# 14) Precision

```python
print("precision Score:",precision_score(y_test,y_pred,average='micro'))
```

---

# Precision Meaning

Positive prediction किती correct आहेत.

---

# average='micro'

Overall total calculation.

---

# Viva Question

### Q: Precision use कधी important?

Answer:
False positives कमी ठेवायचे असतील तेव्हा.

---

# 15) Recall

```python
print("Recall Score:",recall_score(y_test,y_pred,average='micro'))
```

---

# Recall Meaning

Actual positives पैकी किती correctly पकडले.

---

# Viva Question

### Q: Recall use कधी important?

Answer:
Maximum positive cases detect करायचे असतील तेव्हा.

---

# Important ML Flow (Very Important)

| Step | Work |
|---|---|
| 1 | Import libraries |
| 2 | Load dataset |
| 3 | Clean/check data |
| 4 | Select features |
| 5 | Split dataset |
| 6 | Create model |
| 7 | Train model |
| 8 | Predict |
| 9 | Evaluate accuracy |

---

# Important Variables Explanation

| Variable | Meaning |
|---|---|
| df | Full dataset |
| x | Input data |
| y | Output label |
| x_train | Training features |
| y_train | Training output |
| x_test | Testing features |
| y_test | Actual answers |
| y_pred | Predicted answers |

---

# Important Viva Questions + Answers

## Q1: Naive Bayes म्हणजे काय?
Probability based classification algorithm.

---

## Q2: Iris dataset कशासाठी famous आहे?
Machine learning practice साठी.

---

## Q3: Training data म्हणजे काय?
Model शिकण्यासाठी वापरलेला data.

---

## Q4: Testing data म्हणजे काय?
Model check करण्यासाठी data.

---

## Q5: Accuracy formula?
Correct predictions / total predictions.

---

## Q6: Confusion matrix use?
Performance evaluation.

---

## Q7: GaussianNB continuous data साठी का?
कारण Gaussian distribution assume करतो.

---

# Teacher ला Impress करणारे Points ⭐

- “Naive Bayes probability वर काम करतो.”
- “Training आणि testing split overfitting कमी करतो.”
- “Confusion matrix detailed evaluation देते.”
- “GaussianNB numeric continuous data साठी suitable आहे.”

---

# Common Errors & Solutions

| Error | Reason | Solution |
|---|---|---|
| FileNotFoundError | Wrong path | Correct path |
| ModuleNotFoundError | sklearn install नाही | pip install sklearn |
| ValueError | Wrong shape | Proper input format |
| KeyError | Wrong column name | Correct column |

---

# Theory + Practical Connection

| Theory | Practical |
|---|---|
| Classification | Flower species prediction |
| Training | fit() |
| Prediction | predict() |
| Evaluation | accuracy/confusion matrix |

---

# 2 Minute Revision

## Full Flow

1. Dataset load केला
2. Null values check केल्या
3. Features आणि target वेगळे केले
4. Train-test split केला
5. GaussianNB model तयार केला
6. fit() वापरून training केली
7. predict() वापरून output घेतला
8. Accuracy आणि confusion matrix check केली

---

# Important Keywords

- Naive Bayes
- Classification
- Iris Dataset
- Train-Test Split
- GaussianNB
- Accuracy
- Precision
- Recall
- Confusion Matrix

---

# Shortcut Memory Tricks

| Concept | Trick |
|---|---|
| fit() | “Model शिकतो” |
| predict() | “Model उत्तर देतो” |
| Accuracy | “किती correct” |
| Error | “किती wrong” |
| Precision | “Positive मध्ये किती correct” |
| Recall | “Actual positive किती पकडले” |

---

# Most Important Viva Lines ⭐⭐⭐

```python
model.fit(x_train, y_train)
```
➡️ Training line

```python
y_pred = model.predict(x_test)
```
➡️ Prediction line

```python
confusion_matrix(y_test, y_pred)
```
➡️ Performance checking

```python
accuracy_score(y_test,y_pred)
```
➡️ Accuracy calculation

