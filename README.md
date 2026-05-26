# Amazon Prime Movies & Shows EDA 📊

[![Python](https://img.shields.io/badge/Python-3.x-blue?logo=python)](https://www.python.org/)
[![Pandas](https://img.shields.io/badge/Library-Pandas-yellow)](https://pandas.pydata.org/)
[![EDA](https://img.shields.io/badge/Project-EDA-green)](https://en.wikipedia.org/wiki/Exploratory_data_analysis)

A beginner-friendly Exploratory Data Analysis (EDA) project on the Amazon Prime Movies and Shows dataset using Python.

---

# 📌 Project Overview

This project analyzes Amazon Prime Movies and Shows data using Python libraries like Pandas, NumPy, Matplotlib, and Seaborn. The project focuses on:

- Data cleaning
- Handling missing values
- Duplicate detection
- Dataset exploration
- Statistical analysis
- Data visualization

The analysis helps understand:
- Movies and TV Shows distribution
- Release year trends
- Missing data patterns
- Content-related insights

---

# ✨ Features

- ✔ Data loading and preprocessing
- ✔ Missing value handling
- ✔ Duplicate checking
- ✔ Statistical analysis
- ✔ Dataset exploration
- ✔ Basic data visualization
- ✔ Beginner-friendly EDA workflow

---

# 🛠️ Tech Stack

| Technology | Description |
|------------|-------------|
| Python 🐍 | Programming Language |
| Pandas 📊 | Data Analysis |
| NumPy 🔢 | Numerical Operations |
| Matplotlib 📈 | Data Visualization |
| Seaborn 🎨 | Statistical Visualization |

---

# 📂 Dataset Files

The project uses the following dataset files:

- `titles.csv`
- `credits.csv`

---

# 📚 Libraries Used

```python
import pandas as pd
import matplotlib.pyplot as plt
import seaborn as sns
import numpy as np
```

---

# 🚀 Complete Project Code

## ✅ Import Required Libraries

```python
import pandas as pd
import matplotlib.pyplot as plt
import seaborn as sns
import numpy as np
```

---

## ✅ Load Dataset

```python
titles = pd.read_csv("titles.csv")
credits = pd.read_csv("credits.csv")
```

---

## ✅ Display First 5 Rows

```python
titles.head()
```

```python
credits.head()
```

---

## ✅ Dataset Shape

```python
print("Titles Dataset Shape:", titles.shape)
print("Credits Dataset Shape:", credits.shape)
```

---

## ✅ Dataset Information

```python
titles.info()
```

```python
credits.info()
```

---

## ✅ Check Missing Values

```python
titles.isnull().sum()
```

```python
credits.isnull().sum()
```

---

## ✅ Handle Missing Values

```python
titles['age_certification'] = titles['age_certification'].fillna('Not Rated')
```

---

## ✅ Check Duplicate Values

```python
print("Duplicate Rows in Titles:", titles.duplicated().sum())
print("Duplicate Rows in Credits:", credits.duplicated().sum())
```

---

## ✅ Remove Duplicate Values

```python
titles.drop_duplicates(inplace=True)
credits.drop_duplicates(inplace=True)
```

---

## ✅ Statistical Summary

```python
titles.describe()
```

---

## ✅ Check Unique Values

```python
titles.nunique()
```

---

# 📊 Data Visualization

## ✅ Movies vs TV Shows Count

```python
plt.figure(figsize=(6,4))
sns.countplot(x='type', data=titles)
plt.title("Movies vs TV Shows")
plt.show()
```

---

## ✅ Release Year Distribution

```python
plt.figure(figsize=(10,5))
sns.histplot(titles['release_year'], bins=20)
plt.title("Release Year Distribution")
plt.xlabel("Release Year")
plt.ylabel("Count")
plt.show()
```

---

## ✅ Age Certification Distribution

```python
plt.figure(figsize=(10,5))
titles['age_certification'].value_counts().plot(kind='bar')
plt.title("Age Certification Distribution")
plt.xlabel("Certification")
plt.ylabel("Count")
plt.show()
```

---

## ✅ Missing Values Heatmap

```python
plt.figure(figsize=(10,5))
sns.heatmap(titles.isnull(), cbar=False)
plt.title("Missing Values Heatmap")
plt.show()
```

---

## ✅ Top 10 Genres

```python
top_genres = titles['genres'].value_counts().head(10)

plt.figure(figsize=(10,5))
top_genres.plot(kind='bar')
plt.title("Top 10 Genres")
plt.xlabel("Genres")
plt.ylabel("Count")
plt.show()
```

---

# 🚀 How to Run the Project

## ✅ Step 1: Install Required Libraries

Open terminal or command prompt and run:

```bash
pip install pandas numpy matplotlib seaborn
```

---

## ✅ Step 2: Open the Project

You can run the project using:

- Jupyter Notebook
- VS Code
- Google Colab

---

## ✅ Step 3: Run the Notebook

Open the notebook file:

```bash
Amazon_Prime_Movies_and_Shows.ipynb
```

Run all cells step by step.

---

# 📈 Analysis Performed

- Dataset structure analysis
- Missing value detection
- Duplicate value checking
- Statistical summary generation
- Unique value analysis
- Data visualization

---

# 🌟 Future Improvements

- Interactive dashboards
- Genre-wise analysis
- Recommendation system
- Machine learning integration
- Advanced visualizations

---

# 🙋‍♂️ Author

**Sahil Singh**  
🎓 B.Tech CSE (AI & ML), GHRCEM Pune  

🔗 GitHub: https://github.com/sahilsingh30

---

# 📜 License

This project is created for educational and learning purposes.
