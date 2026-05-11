# DSBDA Practical No. 2 — Simple Explanation

# Practical Topic
## Data Visualization Using Python

---

# 1. Practical Cha Aim

Ya practical madhye aplyala:
- data visualize karaycha
- graphs plot karayche
- patterns samjun ghayche
- comparison karaycha

Simple language madhe:
"Data la graph/charts madhe convert karne."

---

# 2. Main Concepts

| Term | Meaning | Simple Explanation |
|---|---|---|
| Visualization | Graphical representation | Data picture form madhye |
| Graph | Visual chart | Data visually show karto |
| Plot | Graph draw karne | Visualization create |
| Histogram | Frequency graph | Data distribution |
| Scatter Plot | Dot graph | Relation show karto |
| Bar Graph | Comparison graph | Values compare |
| Pie Chart | Percentage graph | Share show karto |

---

# 3. Libraries Used

---

## Code 1

```python
import pandas as pd
```

## Kay karte?
Pandas import karte.

## Ka use keli?
Dataset handle karayla.

---

## Viva Question

### Q. Pandas ka use karto?
Data analysis sathi.

---

# Code 2

```python
import matplotlib.pyplot as plt
```

---

# Very Important Line ⭐

⚠️ Viva madhe frequently vichartat.

---

## Kay karte?
Matplotlib graph plotting library import karte.

---

## Meaning

| Part | Meaning |
|---|---|
| matplotlib | Visualization library |
| pyplot | Graph functions |
| plt | Short alias |

---

## Ka use keli?
Graphs create karayla.

---

## Syntax

```python
import matplotlib.pyplot as plt
```

---

## Alternative

```python
import seaborn as sns
```

Seaborn more attractive graphs dete.

---

## Viva Question

### Q. Matplotlib ka use karto?
Graphs ani charts create karayla.

---

# Code 3

```python
import seaborn as sns
```

---

## Kay karte?
Seaborn library import karte.

---

## Ka use keli?
Advanced ani attractive visualization sathi.

---

## Important Point

Seaborn internally matplotlib use karte.

---

## Viva Question

### Q. Seaborn advantage kay?
Beautiful ani easy graphs.

---

# Code 4

```python
df = pd.read_csv("IRIS.csv")
```

---

## Kay karte?
Dataset load karte.

---

## Output

Data dataframe madhye store hoto.

---

## Viva Question

### Q. read_csv() kay return karte?
DataFrame.

---

# Code 5

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

# Code 6

```python
sns.scatterplot(x='sepal_length', y='sepal_width', data=df)
```

---

# Most Important Line ⭐

⚠️ Scatter plot viva madhe nakkich vichartat.

---

## Kay karte?
Scatter plot draw karte.

---

## Scatter Plot Meaning

Dots cha graph.

2 variables madhla relationship show karto.

---

## Breakdown

| Part | Meaning |
|---|---|
| x | X-axis variable |
| y | Y-axis variable |
| data=df | dataframe source |

---

## Ka use keli?
2 columns madhla relation baghayla.

---

## Output Interpretation

- dots close → relation strong
- dots spread → weak relation

---

## Syntax

```python
sns.scatterplot(x='col1', y='col2', data=df)
```

---

## Alternative

```python
plt.scatter()
```

---

## Viva Question

### Q. Scatter plot ka use karto?
Relationship analyze karayla.

---

# Code 7

```python
plt.show()
```

---

## Kay karte?
Graph display karte.

---

## Ka use keli?
Final graph screen var show karayla.

---

## Viva Question

### Q. show() function kay karte?
Graph display karte.

---

# Code 8

```python
sns.histplot(df['sepal_length'])
```

---

# Important Concept ⭐

Histogram.

---

## Kay karte?
Data distribution show karte.

---

## Histogram Meaning

Frequency graph.

---

## Ka use keli?
Values kiti vela yetat te baghayla.

---

## Output Interpretation

- tall bars → more frequency
- short bars → less frequency

---

## Syntax

```python
sns.histplot(column)
```

---

## Viva Question

### Q. Histogram ka use karto?
Frequency distribution baghayla.

---

# Code 9

```python
sns.boxplot(x='species', y='sepal_length', data=df)
```

---

# Very Important ⭐

⚠️ Boxplot viva madhe important aahe.

---

## Kay karte?
Box plot create karte.

---

## Box Plot Meaning

Data spread ani outliers show karto.

---

## Important Terms

| Term | Meaning |
|---|---|
| Median | Middle line |
| Outlier | Unusual value |
| Quartiles | Data divisions |

---

## Ka use keli?
Species comparison sathi.

---

## Output Interpretation

- box large → more spread
- dots outside → outliers

---

## Viva Question

### Q. Boxplot kay show karto?
Spread ani outliers.

---

# Code 10

```python
sns.pairplot(df, hue='species')
```

---

# Most Important Visualization ⭐

⚠️ Pairplot viva madhe favourite question aahe.

---

## Kay karte?
All columns cha relation graph ekatra dakhavte.

---

## Meaning of hue

Different categories la different colors.

---

## Ka use keli?
Complete dataset relationships baghayla.

---

## Output Interpretation

- Different colors = different species
- Diagonal graphs = distribution
- Other graphs = relationships

---

## Syntax

```python
sns.pairplot(data, hue='column')
```

---

## Viva Question

### Q. Pairplot advantage kay?
Multiple relationships ekach graph madhye.

---

# Code 11

```python
plt.title("Iris Dataset")
```

---

## Kay karte?
Graph la title dete.

---

## Ka use keli?
Graph understandable banvayla.

---

## Viva Question

### Q. title() ka use karto?
Graph heading denyasathi.

---

# Code 12

```python
plt.xlabel("Sepal Length")
plt.ylabel("Sepal Width")
```

---

## Kay karte?
Axis labels set karte.

---

## Meaning

| Label | Meaning |
|---|---|
| xlabel | X-axis name |
| ylabel | Y-axis name |

---

## Viva Question

### Q. xlabel() ani ylabel() use?
Axis naming sathi.

---

# 4. Visualization Types Summary

| Graph | Use |
|---|---|
| Scatter Plot | Relationship |
| Histogram | Distribution |
| Box Plot | Spread + outliers |
| Pairplot | Multiple relationships |
| Bar Graph | Comparison |
| Pie Chart | Percentage |

---

# 5. Theory + Practical Connection

| Theory | Practical madhe use |
|---|---|
| Visualization | Data graphs madhye convert kela |
| Correlation | Scatter plot madhye relation baghitla |
| Distribution | Histogram madhye baghitli |
| Outlier Detection | Boxplot madhye baghitla |
| Classification | Species comparison kela |

---

# 6. Common Errors And Solutions

## Error 1

```python
ModuleNotFoundError
```

## Ka yeto?
Library install nahi.

## Solution

```python
pip install matplotlib seaborn
```

---

## Error 2

```python
FileNotFoundError
```

## Ka yeto?
Wrong CSV path.

## Solution
Correct file path dya.

---

## Error 3

```python
KeyError
```

## Ka yeto?
Wrong column name.

---

# 7. Output Interpretation

| Graph | Meaning |
|---|---|
| Scatter | Relationship |
| Histogram | Frequency |
| Boxplot | Spread |
| Pairplot | Full comparison |

---

# 8. Important Viva Questions

### Q. Data visualization mhanje kay?
Data graphically represent karne.

---

### Q. Scatter plot ka use karto?
2 variables relationship sathi.

---

### Q. Histogram kay show karto?
Frequency distribution.

---

### Q. Boxplot kay show karto?
Spread ani outliers.

---

### Q. Pairplot advantage kay?
Multiple graphs ekatra.

---

### Q. Seaborn ka use karto?
Beautiful visualization sathi.

---

# 9. Teacher Impress Points ⭐

- “Visualization makes data easy to understand.”
- “Scatter plot helps in correlation analysis.”
- “Boxplot detects outliers.”
- “Histogram shows frequency distribution.”
- “Pairplot gives complete relationship analysis.”

---

# 10. Important Keywords

| Keyword | Meaning |
|---|---|
| Plot | Graph |
| Histogram | Frequency graph |
| Scatter | Relation graph |
| Outlier | Abnormal value |
| Distribution | Data spread |
| Visualization | Graphical data |

---

# 11. Shortcut Memory Tricks

| Topic | Trick |
|---|---|
| Scatter | Relation |
| Histogram | Frequency |
| Boxplot | Outliers |
| Pairplot | All relations |
| show() | Display graph |

---

# 12. 2 Minute Revision

## Fast Revision

- Pandas, matplotlib, seaborn import kele.
- Dataset load kela.
- Scatter plot ne relation baghitla.
- Histogram ne distribution baghitli.
- Boxplot ne outliers baghitले.
- Pairplot ne full comparison kela.
- Labels ani title add kele.

---

# Final One Line Summary

"Ya practical madhye Python visualization libraries वापरून dataset che graphs plot karun relationships, distribution ani outliers analyze kele."

