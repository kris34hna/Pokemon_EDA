# Pokémon Exploratory Data Analysis

Exploring the stats, types, and generations of 800 Pokémon to uncover patterns in strength, distribution, and rarity.

---

### Brief Summary

An exploratory data analysis (EDA) on the classic Pokémon dataset (800 Pokémon, Gen 1–6), using Pandas, Matplotlib, Seaborn, and Plotly to analyze stat distributions, type combinations, legendary vs. regular Pokémon, and inter-stat correlations.

---

### Overview

This project performs a complete EDA workflow on the Pokémon dataset — from data cleaning and feature engineering to univariate, bivariate, and multivariate analysis. It explores how base stats (HP, Attack, Defense, Special Attack, Special Defense, Speed) vary across types, generations, and legendary status, and visualizes individual Pokémon stats using interactive radar charts.

---

### Dataset

|Detail |   Info|
|--------|---------|
|File |  pokemon.csv |
|Records  | 800 Pokémon |
|Features | 13 (ID, Name, Type 1, Type 2, Total, HP, Attack, Defense, Sp. Atk, Sp. Def, Speed, Generation, Legendary) |
|Missing Data | Type 2 (~half missing — single-type Pokémon) |
|Duplicates  |  None |

Column Highlights:

- Total — Sum of all 6 base stats (overall strength indicator)
- Type 1 / Type 2 — Determines weaknesses & resistances
- Legendary — Boolean flag for legendary status
- Generation — Which game generation the Pokémon belongs to

---

### Tools & Technologies

 |  Tool |  Purpose |
 |-------|----------|
 |Python |Core language|
 |Pandas / NumPy | Data manipulation & cleaning |
 |Matplotlib / Seaborn | Static visualizations |
 |Plotly | Interactive radar charts |
 |Jupyter Notebook | Development environment |

---

### Methods

1 Initial Inspection — Checked shape, data types, null values, duplicates, and descriptive statistics.  

2 Data Cleaning & Reduction

- Renamed columns (Sp. Atk → Special Attack, Sp. Def → Special Defense)
- Standardized column names to lowercase with underscores
- Filled missing Type 2 values with "No_2nd_Type"
- Dropped redundant ID column
  

3 Feature Extraction

- is_dual_type — flags whether a Pokémon has a second type
- average_total — Total stat divided by 6
- full_type — combined Type 1 + Type 2 string

4 Univariate & Multivariate Analysis

- Min/Max stat Pokémon identification
- Average stats per generation (bar charts)
- Stat distributions (histograms)
- Legendary & Generation distributions (pie charts)
- Type 1 × Type 2 combination heatmap
- Pairplot & correlation matrix across all stats

5 Interactive Visualizations — Built radar charts (Plotly) to visualize and compare individual Pokémon stats.

---

### Key Insights


-  The dataset contains 800 unique Pokémon with 13 features — 3 object, 1 boolean, 9 integer columns, and no duplicates.
-  Only Type 2 has missing values (~50%), since many Pokémon are single-typed (e.g., Charmander = Fire only, while Bulbasaur = Grass/Poison dual-type).
-  ega Mewtwo Y has the highest Special Attack (194) in the dataset.
-  "Total" stat is strongly positively correlated with almost all individual stats — logical, since Total is their sum.
-  Speed and Generation is the only stat pair with a negative correlation; all other relationships are positive.
-  The Legendary distribution is highly unbalanced — legendary Pokémon are a small minority.
-  The Generation distribution is also slightly unbalanced, though less so than Legendary status.
-  No outlier treatment was applied — extreme stat values represent real Pokémon abilities, not data errors.

---

### Dashboard / Output

This project's output is the Jupyter Notebook (POKEMON_EDA.ipynb) containing:

- Correlation heatmaps
- Bar charts of average stats per generation
- Histograms of stat distributions
- Pie charts (Legendary %, Generation %)
- Type 1 × Type 2 heatmap
- Pairplot of all 6 base stats
- Interactive Plotly radar charts for individual & comparative Pokémon stats

---

### Results & Conclusion

This EDA provided a comprehensive understanding of the Pokémon dataset's structure, relationships, and distributions. The "Total" stat serves as a strong overall strength proxy, type combinations reveal interesting design patterns across generations, and both Legendary status and Generation distributions show class imbalance — important considerations for any future predictive modeling on this dataset.

---

### Author & Contact

|Name    | KRISHNA |
|--------|---------|
|LinkedIn|https://www.linkedin.com/in/krishna-krishna-26a106231/ |
|GitHub   | https://github.com/kris34hna/Pokemon_EDA/edit/main/README.md | 


## ⭐ If you found this project helpful, consider giving it a star!
