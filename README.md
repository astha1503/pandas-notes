# 🐼 Pandas Basics with Pokémon Dataset

This repo contains my personal notes and beginner-level practice using **Pandas**, with the help of a fun Pokémon dataset!

---

## 🧠 Quick Revision Notes

### 🔹 1. Importing Pandas
```python
import pandas as pd
```

### 🔹 2. Reading a CSV File
```python
df = pd.read_csv("pokemon.csv")
```

### 🔹 3. Exploring the Data
```python
df.head()          # First 5 rows  
df.tail()          # Last 5 rows  
df.shape           # (rows, columns)  
df.columns         # Column names  
df.info()          # Data types & null count  
df.describe()      # Summary statistics  
```

### 🔹 4. Selecting Data
```python
df["Name"]  
df[["Name", "Type 1"]]  
df.iloc[0]  
df.iloc[0:5]  
df.loc[0, "Name"]  
```

### 🔹 5. Filtering Data
```python
df[df["Type 1"] == "Fire"]  
df[(df["Type 1"] == "Fire") & (df["HP"] > 70)]  
```

### 🔹 6. Sorting Data
```python
df.sort_values("HP", ascending=False)
```

### 🔹 7. Adding New Column
```python
df["Total"] = df["HP"] + df["Attack"] + df["Defense"]
```

### 🔹 8. Dropping Columns
```python
df.drop(columns=["Total"], inplace=True)
```

### 🔹 9. Grouping Data
```python
df.groupby("Type 1").mean()  
df["Type 1"].value_counts()  
```

### 🔹 10. Exporting to CSV
```python
df.to_csv("modified_pokemon.csv", index=False)
```

---

## 💬 Why Pokémon?

Because learning Pandas is way more fun with Pikachu in the dataset ⚡

---

## ✅ What's Included?
- `pokemon.csv` — Sample dataset
- `pandas_pokemon.ipynb` — Practice notebook
- `README.md` — These quick notes!

---

Made with 💖 while learning data science!
