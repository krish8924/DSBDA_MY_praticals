# DSBDA Practical No. 3 — Simple Explanation

## Practical Topic
### Descriptive Statistics — Measures of Central Tendency and Variability

---

# 1. Practical Cha Aim (Simple Madhe)

Ya practical madhye aplyala dataset madhil data samjun ghaycha aahe.

Aapan baghto:
- Average (Mean)
- Middle value (Median)
- Minimum value
- Maximum value
- Standard Deviation
- Group wise statistics

Simple language madhe:
Data cha summary kadhaycha aahe.

Example:
Student marks cha average, highest marks, lowest marks etc.

---

# 2. Main Concepts

| Term | Meaning | Simple Explanation |
|---|---|---|
| Dataset | Data collection | Full table of data |
| DataFrame | Table format data | Excel sheet sarkha data |
| Statistics | Data analysis | Data samjun ghene |
| Mean | Average | Total/Count |
| Median | Middle value | Center madhla number |
| Min | Smallest value | Lowest |
| Max | Largest value | Highest |
| Standard Deviation | Data spread | Data kiti phela aahe |
| GroupBy | Grouping data | Similar values ekatra |

---

# 3. Full Code With Line By Line Explanation

---

## Code 1

```python
import pandas as pd
```

## Explanation

### Kay karte?
Pandas library import karte.

### Ka use keli?
Data table handle karayla.

### Output var effect?
Direct output nahi.
Pan पुढचा sagla dataframe cha code run hoto.

---

## Important Term: Pandas

| Point | Explanation |
|---|---|
| Meaning | Python chi data handling library |
| Use | CSV file read karne, dataframe operations |
| Alias | pd |

## Syntax

```python
import pandas as pd
```

## Alternative

```python
import pandas
```

Pan mostly `pd` use kartat.

---

## Viva Question

### Q. Pandas kay aahe?
Python chi library aahe ji data analysis sathi use hote.

### Q. pd ka lihito?
Short form mhanun.

---

# Code 2

```python
df=pd.read_csv("Data files/IRIS.csv")
```

---

## Line Breakdown

| Part | Meaning |
|---|---|
| df | dataframe variable |
| pd | pandas |
| read_csv() | CSV file read function |
| IRIS.csv | dataset file |

---

## Kay karte?
CSV file madhla data load karte.

## Ka use keli?
Dataset memory madhye आणण्यासाठी.

## Output var effect?
Data dataframe madhye store hoto.

---

## Important Term: DataFrame

### Meaning
Rows ani columns madhla table.

### Excel sheet sarkha asto.

---

## Important Function: read_csv()

| Point | Explanation |
|---|---|
| Use | CSV file read karne |
| Input | File path |
| Output | DataFrame |

## Syntax

```python
pd.read_csv("filename.csv")
```

## Alternative Functions

| Function | Use |
|---|---|
| read_excel() | Excel file read |
| read_json() | JSON file read |

---

## Viva Important

⚠️ Hi line viva madhe vicharu shaktat.

### Q. CSV full form?
Comma Separated Values.

### Q. read_csv() kay return karte?
DataFrame return karte.

---

# Code 3

```python
df
```

---

## Kay karte?
Full dataframe display karte.

## Ka use keli?
Data properly load jhala ka check karayla.

## Output var effect?
Table display hoto.

---

## Output Interpretation

Tumhala rows ani columns disatil.

IRIS dataset madhye generally:
- sepal_length
- sepal_width
- petal_length
- petal_width
- species

हे columns astat.

---

## Viva Question

### Q. Dataframe display kasa karto?
Variable name lihun.

---

# Code 4

```python
df.describe()
```

---

# Most Important Line ⭐

⚠️ Hi line viva madhe nakkich vicharu shaktat.

---

## Kay karte?
Numeric columns chi statistical summary dete.

---

## Ka use keli?
Data quickly analyze karayla.

---

## Output madhe kay yet?

| Term | Meaning |
|---|---|
| count | total values |
| mean | average |
| std | standard deviation |
| min | minimum |
| 25% | first quartile |
| 50% | median |
| 75% | third quartile |
| max | maximum |

---

## Important Concept: Mean

Average value.

## Formula

genui{"math_block_widget_always_prefetch_v2":{"content":"Mean = \\frac{\\sum x}{n}"}}

---

## Important Concept: Standard Deviation

Data average pasun kiti dur aahe te sangte.

- Low std → data close aahe
- High std → data spread aahe

---

## Syntax

```python
df.describe()
```

---

## Alternative

```python
df.info()
```

Pan info() statistics det nahi.

---

## Output Interpretation

Example:

```python
mean = 5.8
```

Mhanje average value 5.8 aahe.

```python
max = 7.9
```

Mhanje highest value 7.9 aahe.

---

## Viva Questions

### Q. describe() function kay karte?
Statistical summary dete.

### Q. std meaning?
Standard deviation.

### Q. Median kuthe asto?
50% row madhye.

---

# Code 5

```python
df["sepal_length"].describe()
```

---

## Kay karte?
Fakta `sepal_length` column chi statistics dete.

---

## Ka use keli?
Single column analyze karayla.

---

## Output var effect?
Specific column chi summary diste.

---

## Important Concept: Column Selection

```python
df["column_name"]
```

### Meaning
Specific column select karne.

---

## Viva Questions

### Q. Single column kasa select karto?

```python
df["column"]
```

---

# Code 6

```python
df.groupby("species").describe()
```

---

# Very Important Line ⭐

⚠️ GroupBy viva madhe khup vichartat.

---

## Kay karte?
Species nusar data groups madhye divide karte.

Nantar प्रत्येक group chi statistics dete.

---

## Example

IRIS madhye:
- Setosa
- Versicolor
- Virginica

हे species groups astat.

---

## Ka use keli?
Group wise comparison karayla.

---

## Output Interpretation

Pratyek species sathi:
- mean
- min
- max
- std

disnar.

---

## Important Function: groupby()

| Point | Explanation |
|---|---|
| Use | Similar data grouping |
| Input | Column name |
| Output | Groups |

---

## Syntax

```python
df.groupby("column")
```

---

## Alternative

```python
df.groupby("species").mean()
```

Fakta mean dete.

---

## Viva Questions

### Q. groupby() ka use karto?
Similar values group karayla.

### Q. Categorical variable mhanje?
Text/category type data.

Example:
species

---

# Code 7

```python
df.groupby("species").describe().sum()
```

---

## Kay karte?
Group statistics kadhte ani total sum dete.

---

## Ka use keli?
Combined statistical values baghayla.

---

## Important Point

He practical madhye compulsory nahi pan extra analysis sathi use hote.

---

## Viva Question

### Q. sum() kay karte?
Values add karte.

---

# 4. Theory + Practical Connection

| Theory | Practical madhe kasa use jhala |
|---|---|
| Mean | Average kadhla |
| Median | Middle value baghitli |
| Standard Deviation | Data spread analyze kela |
| Data Analysis | Dataset summarize kela |
| Grouping | Species wise comparison |

---

# 5. Variables Explanation

| Variable | Meaning |
|---|---|
| df | Full dataframe |
| species | Flower category |
| sepal_length | Flower measurement |

---

# 6. ML/Data Analysis Flow

## Full Process

1. Library import
2. Dataset load
3. Data display
4. Statistical analysis
5. Group analysis
6. Interpretation

---

# 7. Common Errors And Solutions

## Error 1

```python
FileNotFoundError
```

## Ka yeto?
CSV file path wrong aahe.

## Solution
Correct path dya.

---

## Error 2

```python
KeyError
```

## Ka yeto?
Wrong column name.

Example:

```python
df["sepal"]
```

Pan actual column:

```python
sepal_length
```

---

## Error 3

```python
ModuleNotFoundError
```

## Ka yeto?
Pandas install nahi.

## Solution

```python
pip install pandas
```

---

# 8. Important Viva Questions With Answers

## Basic Viva

### Q. Descriptive statistics mhanje kay?
Data summarize karne.

---

### Q. Mean formula?

genui{"math_block_widget_always_prefetch_v2":{"content":"Mean = \\frac{\\sum x}{n}"}}

---

### Q. Median kay aahe?
Middle value.

---

### Q. Standard deviation kay sangte?
Data spread.

---

### Q. DataFrame mhanje kay?
Rows-column madhla table.

---

### Q. groupby() ka use karto?
Grouping sathi.

---

### Q. describe() kay dete?
Statistical summary.

---

# 9. Teacher Impress Points ⭐

He points बोलले तर impression changla padto:

- “describe() statistical summary dete.”
- “groupby() categorical analysis sathi useful aahe.”
- “Standard deviation data variability show karte.”
- “DataFrame is tabular data structure.”
- “IRIS dataset machine learning madhye famous aahe.”

---

# 10. Important Keywords

| Keyword | Meaning |
|---|---|
| DataFrame | Table data |
| CSV | Comma separated file |
| Mean | Average |
| Median | Middle value |
| Std | Spread |
| GroupBy | Grouping |
| Statistics | Data analysis |

---

# 11. Shortcut Memory Tricks

| Topic | Trick |
|---|---|
| Mean | Average |
| Median | Middle |
| Min | Small |
| Max | Large |
| Std | Spread |
| GroupBy | Grouping |

---

# 12. 2 Minute Revision

## Fast Revision

- Pandas import kela.
- CSV dataset load kela.
- Dataframe display kela.
- describe() ne statistics baghitli.
- Single column analysis kela.
- groupby() ne species wise analysis kela.
- Mean, median, min, max, std samjhla.

---

# Final One Line Summary

"Ya practical madhye dataset chi statistical summary ani group wise analysis kela using pandas functions like describe() and groupby()."

