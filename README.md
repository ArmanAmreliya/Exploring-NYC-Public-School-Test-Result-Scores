# Exploring-NYC-Public-School-Test-Result-Scores
# 🏫 NYC Schools SAT Analysis

<div align="center">
  <img src="schoolbus.jpg" alt="NYC Schools" width="200"/>

[![Python](https://img.shields.io/badge/Python-3.10+-blue.svg)](https://python.org)
[![Pandas](https://img.shields.io/badge/Pandas-Latest-green.svg)](https://pandas.pydata.org/)
[![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-orange.svg)](https://jupyter.org/)

</div>

## 📖 About The Project

Welcome to the **NYC Schools SAT Analysis** project! 📊

This project analyzes New York City public school SAT results to understand performance across schools and boroughs. By working with a dataset of SAT scores (math, reading, writing), we uncover insights about top schools and borough-level variations.

### 🎯 What We Explore

* 🧮 **Best Math Schools** - Schools with math scores above 80% of the maximum (≥ 640/800)
* 🏆 **Top 10 Overall Schools** - Based on combined SAT scores (math + reading + writing)
* 🌆 **Borough Analysis** - Find which borough has the largest variation (standard deviation) in SAT performance

## 🚀 Getting Started

### Prerequisites

* Python 3.10+
* Jupyter Notebook
* Basic knowledge of Pandas

### 📦 Required Libraries

```python
import pandas as pd
```

### 🛠️ Installation

1. **Clone the repository**

   ```bash
   git clone <your-repo-url>
   cd nyc-schools-sat-analysis
   ```

2. **Install required packages**

   ```bash
   pip install pandas jupyter
   ```

3. **Launch Jupyter Notebook**

   ```bash
   jupyter notebook
   ```

4. **Open `schools_analysis.ipynb`** and start exploring!

## 📁 Project Structure

```
📦 NYC-Schools-SAT-Analysis
 ┣ 📜 schools_analysis.ipynb   # Main analysis notebook
 ┣ 📊 schools.csv              # NYC schools dataset
 ┣ 🖼️ schoolbus.jpg            # Project banner image
 ┗ 📜 README.md                # You are here!!
```

## 📊 Dataset Information

### 📝 NYC Schools Data Schema

| Column            | Description                                                       |
| ----------------- | ----------------------------------------------------------------- |
| `school_name`     | Name of the school                                                |
| `borough`         | Borough (e.g., Manhattan, Bronx, Brooklyn, Queens, Staten Island) |
| `average_math`    | Average SAT math score                                            |
| `average_reading` | Average SAT reading score                                         |
| `average_writing` | Average SAT writing score                                         |
| `building_code`   | School building code                                              |
| `percent_tested`  | % of students who took the SAT                                    |

## 🔍 Key Analysis Features

### 🎯 Best Math Schools

* Schools with **average math ≥ 640**
* Sorted by math performance (descending)

### 🏆 Top 10 Schools

* Ranked by combined SAT scores (math + reading + writing)
* Results include school name and total SAT

### 🌆 Borough Standard Deviation

* Calculate **number of schools, mean SAT, and standard deviation** per borough
* Identify the borough with the highest variability

## 📝 Usage Examples

```python
import pandas as pd

# Load data
schools = pd.read_csv("schools.csv")

# Create total SAT score
schools["total_SAT"] = schools["average_math"] + schools["average_reading"] + schools["average_writing"]

# Top 10 schools
top_10 = schools[["school_name", "total_SAT"]].sort_values("total_SAT", ascending=False).head(10)
print(top_10)
```

## 🏆 Key Findings

* Schools with average math ≥ 640 show standout performance across NYC
* Top 10 schools are mainly concentrated in certain boroughs
* One borough shows the **highest variation** in SAT performance — meaning schools in that area have the widest score gap

## 🤝 Contributing

Contributions are always welcome! 🎉

1. Fork the Project
2. Create a Feature Branch (`git checkout -b feature/NewFeature`)
3. Commit Changes (`git commit -m 'Add some feature'`)
4. Push to Branch (`git push origin feature/NewFeature`)
5. Open a Pull Request

---

<div align="center">
  <p><strong>⭐ Star this repository if you found it helpful! ⭐</strong></p>
  <p>Made with ❤️ by Arman Amreliya</p>
</div>

---

**Happy Analyzing! 🏫📊**
