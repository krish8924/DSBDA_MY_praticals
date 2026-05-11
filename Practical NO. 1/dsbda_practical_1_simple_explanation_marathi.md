# DSBDA Practical No. 1 — Simple Explanation

# Practical Topic
## Data Wrangling Using Python

---

# 1. Practical Cha Aim

Ya practical madhye:
- dataset load karaycha
- missing values check karaychya
- null values handle karaychya
- duplicate data remove karaycha
- data clean karaycha

Simple language madhe:
"Raw data clean ani usable banvne."

---

# 2. Main Concepts

| Term | Meaning | Simple Explanation |
|---|---|---|
| Data Wrangling | Data cleaning | Dirty data clean karne |
| Missing Values | Empty values | Blank data |
| Null | No value | Data nahi |
| Duplicate | Repeated data | Same row repeated |
| Data Cleaning | Error remove | Correct data banvne |
| DataFrame | Table format data | Excel sheet sarkha |

---

# 3. Code Line By Line Explanation

---

## Code 1

```python
import pandas as pd
```

## Kay karte?
Pandas library import karte.

## Ka use keli?
Data handle karayla.

## Important Point

⚠️ Viva madhe vicharu shaktat.

---

## Viva Question

### Q. Pandas kay aahe?
Python chi data analysis library.

---

# Code 2

```python
import numpy as np
```

---

## Kay karte?
NumPy library import karte.

## Ka use keli?
Numerical operations sathi.

---

## Important Term: NumPy

| Point | Explanation |
|---|---|
| Full Form | Numerical Python |
| Use | Math operations |
| Alias | np |

---

## Syntax

```python
import numpy as np
```

---

## Viva Question

### Q. NumPy ka use karto?
Fast numerical calculations sathi.

---

# Code 3

```python
df = pd.read_csv("data.csv")
```

---

## Kay karte?
CSV dataset load karte.

## Output var effect?
Data dataframe madhye store hoto.

---

## Important Function: read_csv()

| Use | CSV file read |
| Output | DataFrame |

---

## Syntax

```python
pd.read_csv("filename.csv")
```

---

## Viva Question

### Q. CSV full form?
Comma Separated Values.

---

# Code 4

```python
df.head()
```

---

## Kay karte?
First 5 rows display karte.

## Ka use keli?
Dataset preview baghayla.

---

## Syntax

```python
df.head()
```

---

## Alternative

```python
df.tail()
```

Last rows dakhavte.

---

## Viva Question

### Q. head() kay karte?
First rows display karte.

---

# Code 5

```python
df.info()
```

---

# Very Important Line ⭐

⚠️ Viva madhe frequently vichartat.

---

## Kay karte?
Dataset chi complete information dete.

---

## Output madhe kay diste?

- column names
- data types
- non-null values
- memory usage

---

## Important Term: Data Type

| Type | Meaning |
|---|---|
| int | Integer number |
| float | Decimal number |
| object | Text/string |

---

## Viva Question

### Q. info() kay karte?
Dataset information dete.

---

# Code 6

```python
df.isnull()
```

---

## Kay karte?
Null values check karte.

---

## Output

| Value | Meaning |
|---|---|
| True | Null value aahe |
| False | Value present aahe |

---

## Important Concept: Null Value

Missing data.

Example:
- empty cell
- blank value

---

## Viva Question

### Q. Null value mhanje kay?
Missing/empty data.

---

# Code 7

```python
df.isnull().sum()
```

---

# Most Important Line ⭐

⚠️ Hi line viva madhe nakkich vicharu shaktat.

---

## Kay karte?
Pratyek column madhye total null values count karte.

---

## Breakdown

| Part | Meaning |
|---|---|
| isnull() | Null check |
| sum() | Total count |

---

## Output Interpretation

```python
Age 5
```

Mhanje Age column madhye 5 missing values aahet.

---

## Viva Question

### Q. Missing values kasa count karto?

```python
df.isnull().sum()
```

---

# Code 8

```python
df.dropna()
```

---

## Kay karte?
Null values aslelya rows remove karte.

---

## Ka use keli?
Clean dataset banvayla.

---

## Important Function: dropna()

| Use | Null rows remove |
| Output | Clean data |

---

## Syntax

```python
df.dropna()
```

---

## Alternative

```python
df.fillna(0)
```

Null replace karte.

---

## Viva Question

### Q. dropna() kay karte?
Missing values remove karte.

---

# Code 9

```python
df.fillna(df.mean())
```

---

# Important Concept ⭐

Null values replace karne.

---

## Kay karte?
Missing values average value ne fill karte.

---

## Mean Formula

genui{"math_block_widget_always_prefetch_v2":{"content":"Mean = \\frac{\\sum x}{n}"}}

---

## Ka use keli?
Data loss avoid karayla.

---

## Output Interpretation

Null value replace hote.

---

## Viva Question

### Q. fillna() ka use karto?
Missing values fill karayla.

---

# Code 10

```python
df.duplicated()
```

---

## Kay karte?
Duplicate rows check karte.

---

## Output

| True | Duplicate row |
| False | Unique row |

---

## Important Concept: Duplicate Data

Same row repeated asel tar.

---

## Viva Question

### Q. Duplicate data problem ka aahe?
Analysis wrong hou shakto.

---

# Code 11

```python
df.drop_duplicates()
```

---

## Kay karte?
Duplicate rows remove karte.

---

## Ka use keli?
Accurate analysis sathi.

---

## Viva Question

### Q. drop_duplicates() kay karte?
Repeated rows remove karte.

---

# 4. Data Cleaning Process

## Full Flow

1. Dataset load
2. Dataset preview
3. Information check
4. Missing values detect
5. Missing values handle
6. Duplicate rows remove
7. Clean dataset prepare

---

# 5. Theory + Practical Connection

| Theory | Practical madhe use |
|---|---|
| Data Cleaning | Dirty data clean kela |
| Missing Values | Null values handle kelya |
| Duplicate Removal | Repeated rows remove kelya |
| Mean | Average value fill keli |
| Data Analysis | Clean data prepare kela |

---

# 6. Common Errors And Solutions

## Error 1

```python
FileNotFoundError
```

## Ka yeto?
Wrong file path.

## Solution
Correct CSV path dya.

---

## Error 2

```python
ModuleNotFoundError
```

## Ka yeto?
Library install nahi.

## Solution

```python
pip install pandas
```

---

## Error 3

```python
KeyError
```

## Ka yeto?
Wrong column name.

---

# 7. Output Interpretation

| Output | Meaning |
|---|---|
| True | Null/duplicate exists |
| False | No issue |
| count | Total rows |
| object | Text data |
| float | Decimal number |

---

# 8. Important Viva Questions

### Q. Data wrangling mhanje kay?
Data clean ani prepare karne.

---

### Q. Missing values ka problem aahet?
Wrong analysis hou shakto.

---

### Q. dropna() ani fillna() madhla difference?
- dropna() rows remove karte
- fillna() values replace karte

---

### Q. Duplicate rows ka remove karto?
Correct analysis sathi.

---

### Q. DataFrame mhanje kay?
Table format data structure.

---

# 9. Teacher Impress Points ⭐

- “Data cleaning improves data quality.”
- “Missing values affect analysis accuracy.”
- “fillna() prevents data loss.”
- “Duplicate rows create redundancy.”
- “Data wrangling is important before machine learning.”

---

# 10. Important Keywords

| Keyword | Meaning |
|---|---|
| Null | Missing value |
| Duplicate | Repeated row |
| Cleaning | Error removal |
| Mean | Average |
| DataFrame | Table |
| CSV | File format |

---

# 11. Shortcut Memory Tricks

| Topic | Trick |
|---|---|
| isnull() | Check null |
| dropna() | Drop null |
| fillna() | Fill null |
| duplicated() | Check duplicate |
| drop_duplicates() | Remove duplicate |

---

# 12. 2 Minute Revision

## Fast Revision

- Pandas ani NumPy import kele.
- CSV dataset load kela.
- head() ne preview baghitla.
- info() ne dataset details baghitlya.
- isnull() ne missing values check kelya.
- dropna() ne null rows remove kelya.
- fillna() ne null values fill kelya.
- duplicated() ne repeated rows check kelya.
- drop_duplicates() ne duplicate rows remove kelya.

---

# Final One Line Summary

"Ya practical madhye dataset clean karun missing values ani duplicate data handle kela using pandas functions."

