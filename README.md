# 🎬 IMDb India Movies — Data Cleaning & EDA

A data cleaning and exploratory analysis pipeline built on the **IMDb Movies India** dataset. The notebook prepares raw movie data for downstream analysis by handling missing values, standardising formats, and validating key fields.

---

## 📋 Dataset

| Field | Description |
|---|---|
| **Source** | `IMDb_Movies_India.csv` |
| **Columns** | Name, Year, Duration, Genre, Rating, Votes, Director, Actor 1, Actor 2, Actor 3 |

---

## 🔧 What the Notebook Does

1. **Raw Data Overview** — shape, dtypes, and a quick peek at the first few rows
2. **Missing Value Summary** — counts and percentages per column
3. **Remove Duplicates** — deduplicates on movie `Name`, keeping the last occurrence
4. **Clean `Name`** — strips whitespace and drops blank/unusable records
5. **Clean `Year`** — extracts 4-digit year from strings like `(2019)`, flags unrealistic values
6. **Clean `Duration`** — strips `" min"` suffix, casts to integer
7. **Clean `Votes`** — removes comma separators (e.g. `1,086` → `1086`)
8. **Validate `Rating`** — coerces to numeric and nullifies values outside the 1–10 IMDb range
9. **Strip Text Columns** — trims whitespace and normalises empty strings to `NaN` for Genre, Director, and Actor fields
10. **Missing Value Strategy** — preserves factual NaNs (Rating, Votes); fills Genre unknowns

---

## 🛠️ Tech Stack

- Python 3
- `pandas` · `numpy`
- `matplotlib` · `seaborn`

---

## 🚀 Getting Started

```bash
# Clone the repository
git clone https://github.com/soumimukherjee22/<repo-name>.git
cd <repo-name>

# Install dependencies
pip install pandas numpy matplotlib seaborn

# Launch the notebook
jupyter notebook Movie_Prediction.ipynb
```

> **Note:** Update the dataset path in the notebook to point to your local copy of `IMDb Movies India.csv`.

---

## 👩‍💻 Author

**Soumi Mukherjee** — Data Analyst

[![Email](https://img.shields.io/badge/Email-soumi.mukherjee2003%40gmail.com-red?style=flat&logo=gmail)](mailto:soumi.mukherjee2003@gmail.com)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-soumimukherjeeofficial-blue?style=flat&logo=linkedin)](https://www.linkedin.com/in/soumimukherjeeofficial/)
[![GitHub](https://img.shields.io/badge/GitHub-soumimukherjee22-black?style=flat&logo=github)](https://github.com/soumimukherjee22)
