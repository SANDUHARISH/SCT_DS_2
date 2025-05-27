# 🚢 Titanic Dataset - Data Cleaning & Exploratory Data Analysis (EDA) 🧹📊

## 📋 Project Overview
This project performs **data cleaning** and **exploratory data analysis (EDA)** on the Titanic dataset from Kaggle.  
The main goal is to explore relationships between variables, identify patterns and trends, and understand factors influencing survival on the Titanic.

---

## 🗂 Dataset Description
The Titanic dataset contains passenger information, including survival status, socio-economic class, demographics, and travel details.

| Column       | Description                                          |
|--------------|------------------------------------------------------|
| PassengerId  | Unique ID for each passenger                         |
| Survived     | Survival status (0 = No, 1 = Yes)                   |
| Pclass       | Passenger class (1 = Upper, 2 = Middle, 3 = Lower)  |
| Name         | Passenger name                                       |
| Sex          | Gender of the passenger                              |
| Age          | Age in years (fractional for infants)               |
| SibSp        | Number of siblings/spouses aboard                    |
| Parch        | Number of parents/children aboard                    |
| Ticket       | Ticket number                                       |
| Fare         | Ticket fare paid                                    |
| Cabin        | Cabin number (many missing values)                  |
| Embarked     | Port of embarkation (C = Cherbourg, Q = Queenstown, S = Southampton) |

---

## 🛠 Libraries Used
- `numpy`  
- `pandas`  
- `matplotlib`  
- `seaborn`

---

## 🧹 Data Cleaning Steps
- Loaded dataset using `pd.read_csv()`.
- Checked dataset shape, info, and summary statistics.
- Handled missing values:
  - Filled **Age** missing values with mean age. 🧓
  - Dropped **Cabin** column due to too many missing entries. 🚫
  - Filled missing **Embarked** values with mode (most common port). ⚓
- Verified no duplicate entries found.

---

## 🔍 Exploratory Data Analysis (EDA)

### Survival Distribution
- About **61.6% did NOT survive**. 💔
- Visualized survival counts using countplots and pie charts.

### Gender and Survival
- Females had a much higher survival rate than males. 👩‍🦰 > 👨
- Visualized survival by gender using countplots and pie charts.

### Passenger Class and Survival
- Most passengers were in 3rd class, which had the lowest survival rate. 🥉
- Males in 3rd class were the most vulnerable group.
- Visualized survival by class and gender.

### Embarkation Point
- Analyzed survival rates and distribution by embarkation port.

### Family Relationships
- Explored the impact of siblings/spouses (`SibSp`) and parents/children (`Parch`) aboard on survival.

### Age and Fare Distributions
- Plotted histograms and KDE plots for Age and Fare.
- Created age groups (Infant, Child, Teenager, Young Adult, Adult, Senior) to study survival rates.
- Notably, **young adults had the lowest survival rate**.

### Correlation Analysis
- Converted categorical features (`Sex`, `Embarked`) to numerical codes.
- Correlation heatmap revealed meaningful correlations with survival:
  - Fare, Sex, Pclass, Embarked.

---

## 📝 Observations & Conclusions
- **Gender Disparity:** Females had significantly higher survival, aligned with "women and children first" protocol. 👩‍👧‍👦
- **Passenger Class:** 3rd class passengers had lower survival, reflecting socio-economic disparities. 🥉
- **Age Effect:** Young adults had the lowest survival rates. Age mattered. 🎂
- **Important Factors:** Fare, sex, passenger class, and embarkation point correlate with survival outcomes.

---

## 🚀 How to Run
1. Clone the repository.  
2. Ensure Python environment with required libraries (`numpy`, `pandas`, `matplotlib`, `seaborn`) is installed.  
3. Load the dataset (`Titanic-Dataset.csv`).  
4. Run the Jupyter Notebook or Python script to view the cleaning process, EDA visuals, and insights.

---

## 📚 References
- Titanic Dataset: [Kaggle Titanic Competition](https://www.kaggle.com/c/titanic)  
- Python Libraries: NumPy, Pandas, Matplotlib, Seaborn documentation  

---

Feel free to ⭐ this repo if you find it useful!  
Questions? Reach out! 😊
