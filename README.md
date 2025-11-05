# 🏏 IPL Data Analysis Project

**Author:** Prashant Trivedi  
**Role:** Data Engineer  
**Technologies:** Apache Spark, Python, Amazon S3, Data Visualization  

---

## 🚀 Project Overview

This project focuses on **analyzing IPL (Indian Premier League) data** to gain insights about teams, players, and match outcomes. The goal is to **extract meaningful patterns from raw match data** using **Big Data tools** and **Python visualizations**.  

---

## 🛠️ Tools & Technologies Used

- **Apache Spark** ⚡ – For **big data processing and transformation**  
- **Amazon S3** ☁️ – For **storing and retrieving IPL datasets**  
- **Python** 🐍 – For **data analysis, scripting, and automation**  
- **Matplotlib / Seaborn** 📊 – For **charts and visualizations**  
- **Git & GitHub** 🐙 – Version control and project repository  

---

## 🔹 Key Features / Tasks

1. **Data Collection & Storage**  
   - IPL datasets stored in **Amazon S3 buckets** for scalable and secure storage.  
   - CSV/JSON files organized for efficient access and processing.

2. **Data Processing**  
   - Used **Apache Spark** for **cleaning, transforming, and aggregating** large datasets.  
   - Handled **player statistics, team performance metrics, and match details**.  

3. **Data Analysis**  
   - Calculated **top scorers, strike rates, and wicket takers**.  
   - Analyzed **team performance trends over seasons**.  

4. **Data Visualization**  
   - Created **interactive charts and graphs** using Python libraries.  
   - Examples:  
     - 🥇 Top 5 run scorers per season  
     - 🎯 Wicket distribution among bowlers  
     - 📈 Team win/loss trends over seasons  

---

## 💻 Sample Python Code (Data Visualization)

```python
import pandas as pd
import matplotlib.pyplot as plt
import seaborn as sns

# Load data from S3
df = pd.read_csv("s3://ipl-data-bucket/matches.csv")

# Example: Top 5 scorers
top_scorers = df.groupby('batsman')['runs'].sum().sort_values(ascending=False).head(5)

# Plotting
plt.figure(figsize=(10,6))
sns.barplot(x=top_scorers.index, y=top_scorers.values, palette='viridis')
plt.title("🏏 Top 5 Run Scorers in IPL", fontsize=16)
plt.ylabel("Total Runs")
plt.xlabel("Batsman")
plt.show()


IPL Data Engineering & Analytics using Apache Spark
Project Overview

This project demonstrates an end-to-end Big Data Engineering pipeline for analyzing Indian Premier League (IPL) cricket datasets. Using Apache Spark, Python, and SQL, the project processes raw match, player, and team data to provide actionable insights about IPL performance trends, top players, and team statistics.

The main objective of this project is to showcase data engineering skills, including data ingestion, cleaning, transformation, aggregation, and visualization of large-scale datasets in a scalable and efficient manner.

Key Features

Data Ingestion & Cleaning: Efficiently read large IPL datasets (matches, players, scores) and handle missing or inconsistent data using PySpark.

Data Transformation: Aggregate and transform raw data into structured formats suitable for analysis using Spark SQL and PySpark DataFrames.

Analytical Queries: Perform complex queries to identify top run-scorers, highest wicket-takers, team win ratios, and player performance trends.

Data Visualization: Generate meaningful visualizations using Matplotlib and Seaborn to represent insights such as runs per season, match outcomes, and team comparisons.

Scalable & Efficient: Designed to handle large datasets, ensuring performance optimization and efficient memory usage using Spark transformations and caching techniques.

Technologies & Tools Used

Big Data Tools: Apache Spark, PySpark

Databases / Querying: Spark SQL, Hive (optional)

Programming Languages: Python

Visualization: Matplotlib, Seaborn

Environment / Platforms: Databricks, Jupyter Notebook, Google Colab

Version Control: Git & GitHub

Project Workflow

Data Collection: Download IPL datasets (matches, teams, players, and statistics) from open sources or official APIs.

Data Cleaning & Preprocessing: Handle missing values, normalize formats, and convert data into structured formats for Spark processing.

Data Transformation & Aggregation: Use Spark SQL and PySpark DataFrames to calculate player stats, team performance, and match summaries.

Visualization & Analysis: Create visual insights such as top players per season, team win-loss trends, and performance comparisons.

Insights & Reporting: Summarize findings in dashboards, plots, and tables for quick decision-making or reporting.

Sample Insights

Top run-scorers in each IPL season

Highest wicket-takers and bowling economy analysis

Team win-loss ratios over seasons

Player performance trends across matches and seasons

Visualization of runs scored per match, season, and player

Learning Outcomes

Hands-on experience in Big Data processing using Apache Spark

Writing efficient Spark SQL queries and DataFrame transformations

Building scalable data pipelines for real-world sports datasets

Presenting analytical insights via Python visualizations

Understanding the end-to-end workflow of a data engineering project

Conclusion

This project serves as a comprehensive showcase of data engineering and analytics skills applied to sports data. By leveraging Apache Spark, Python, and SQL, it demonstrates how large-scale datasets can be processed, analyzed, and visualized to generate meaningful insights — making it an ideal portfolio project for aspiring Data Engineers or Data Analysts.
