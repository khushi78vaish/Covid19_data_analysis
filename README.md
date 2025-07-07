# 🦠 Covid-19 Data Analysis using Python

This project performs exploratory data analysis (EDA) on global Covid-19 data using Python. It covers data cleaning, feature engineering, aggregation, and visualization to understand the spread and impact of the pandemic based on factors like GDP per capita and human development index.

---

## 📌 Dataset

The dataset is sourced from [this public URL](https://raw.githubusercontent.com/SR1608/Datasets/main/covid-data.csv). It contains worldwide Covid-19 data including:

- Location and continent
- Date-wise total cases and deaths
- Socio-economic indicators like GDP per capita and Human Development Index

---

## 🛠 Technologies Used

- **Python** (Pandas, NumPy)
- **Seaborn & Matplotlib** (for data visualization)
- **Google Colab** (development environment)

---

## 📊 Project Workflow

### 1. 📥 Data Loading
- Imported dataset using `pandas.read_csv()` from a raw GitHub URL.

### 2. 🧠 High-Level Data Understanding
- Checked rows, columns, datatypes, and basic statistics using `.shape`, `.dtypes`, `.info()` and `.describe()`.

### 3. 🔎 Low-Level Data Understanding
- Counted unique values in `location`.
- Identified continent with the highest data frequency.
- Calculated max/mean of `total_cases`, and quartiles of `total_deaths`.
- Found continents with highest `human_development_index` and lowest `gdp_per_capita`.

### 4. 🧹 Data Cleaning
- Removed duplicate entries.
- Dropped rows with missing `continent` values.
- Replaced remaining null values with 0 using `fillna(0)`.

### 5. 🗓 Date Formatting
- Converted `date` column to datetime format.
- Extracted the month into a new column `month`.

### 6. 📈 Data Aggregation
- Grouped data by `continent` and calculated the maximum values for all columns.
- Stored the result in a new DataFrame called `df_groupby`.

### 7. 🧮 Feature Engineering
- Created a new column:  
  `total_deaths_to_total_cases = total_deaths / total_cases`

### 8. 📊 Data Visualization
- Histogram of `gdp_per_capita`
- Scatter plot of `total_cases` vs `gdp_per_capita`
- Pairplot of `df_groupby` DataFrame
- Bar plot showing `total_cases` per continent

### 9. 💾 Output
- Saved the final `df_groupby` DataFrame as a CSV file: `df_groupby.csv`

---

## 📎 How to Run

1. Open [Google Colab](https://colab.research.google.com/)
2. Copy and paste the Python code from this repository
3. Run each cell in sequence
4. Download the CSV output using `files.download()`

---

## 📌 Key Learnings

- Cleaned real-world Covid-19 data
- Used aggregation and grouping to summarize global health metrics
- Created custom features for deeper insight
- Visualized data with informative plots

---

## 📁 Output File

- `df_groupby.csv` — Final cleaned and aggregated dataset.

---

## 🙋‍♀️ Author

**Khushi Vaish**  
B.Tech | Data Science Enthusiast

---

## 📜 License

This project is open source and free to use for educational purposes.
