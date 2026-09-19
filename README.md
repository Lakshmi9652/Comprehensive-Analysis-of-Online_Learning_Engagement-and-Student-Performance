# 📊 Online Learning Engagement & Student Performance Analytics

> **Turning student activity data into meaningful educational insights using SQL and Power BI.**

##  About the Project

**Online Learning Engagement & Student Performance Analytics** is a data analytics project designed to understand how students interact with an online learning environment and how different engagement patterns are associated with academic performance.

The project combines **MySQL for data analysis** and **Power BI for interactive visualization** to explore student activity, performance, risk, and dropout patterns.

Instead of looking at student scores alone, this project looks at the bigger picture:

**Engagement → Activity → Performance → Risk → Student Outcome**

The analysis helps answer questions such as:

* How engaged are the students?
* Does higher online activity correspond with different performance levels?
* How are dropout patterns distributed across engagement groups?
* Which performance categories have higher dropout rates?
* How does student activity vary by region?
* How does educational background relate to performance and engagement?

---

##  Project Objectives

The major objectives of this project are:

* Analyze the overall level of student engagement.
* Measure student academic performance using average scores.
* Compare engagement levels with student performance.
* Analyze online activity using total clicks.
* Examine dropout patterns across engagement levels.
* Compare dropout rates across performance categories.
* Understand student risk-level distribution.
* Compare student performance and engagement across regions.
* Analyze performance and activity based on highest education level.
* Build a Power BI dashboard for interactive exploration.

---

##  Business Problem

Online education platforms generate large amounts of student activity data.

However, raw activity data alone does not provide meaningful answers.

Educational institutions need to understand:

> **Are students actively engaging with the platform, and how is that engagement associated with their academic outcomes?**

This project transforms student-level data into analytical information that can help identify **engagement patterns, performance differences, and potential dropout-risk patterns**.

The analysis is descriptive and exploratory; relationships found in the data should not automatically be interpreted as causal relationships.

---

#  Dataset & Key Fields

The analysis uses the `online_education_dataset` table from the `online_education_db` database.

Key fields used in the analysis include:

| Field               | Purpose                      |
| ------------------- | ---------------------------- |
| `id_student`        | Unique student identifier    |
| `avg_score`         | Student average score        |
| `total_clicks`      | Measure of online activity   |
| `engagement_level`  | Student engagement category  |
| `performance_level` | Student performance category |
| `risk_level`        | Student risk category        |
| `pass_flag`         | Indicates passing status     |
| `dropout_flag`      | Indicates dropout status     |
| `region`            | Student region               |
| `highest_education` | Highest education level      |

---

# 🛠️ Tools & Technologies

# Database & Analysis

* **MySQL**
* **SQL**
* Aggregate Functions
* `GROUP BY`
* `CASE WHEN`
* Conditional Aggregation
* Percentage & Rate Calculations

# Visualization

* **Microsoft Power BI**
* Interactive dashboards
* KPIs
* Charts and comparative analysis

---

# 🔄 Project Workflow

```text
                    ONLINE EDUCATION DATA
                             │
                             ▼
                    ┌─────────────────┐
                    │     MySQL       │
                    │ Data Exploration│
                    └────────┬────────┘
                             │
                             ▼
                    ┌─────────────────┐
                    │   SQL Analysis  │
                    │                 │
                    │ Engagement      │
                    │ Performance     │
                    │ Activity        │
                    │ Risk            │
                    │ Dropout         │
                    └────────┬────────┘
                             │
                             ▼
                    ┌─────────────────┐
                    │  Power BI       │
                    │ Visualization   │
                    └────────┬────────┘
                             │
                             ▼
                    ┌─────────────────┐
                    │    Insights     │
                    │ & Interpretation│
                    └─────────────────┘
```

---

🔍 Analysis Performed

 1. Student Overview

The project first establishes the overall size of the student population and calculates key averages such as:

* Total unique students
* Average student score
* Average total clicks

These provide a baseline for understanding the dataset.

---

 2. Pass & Dropout Analysis

Student outcomes are examined using pass and dropout indicators.

The analysis identifies:

* Number of students who passed
* Number of students who dropped out
* Dropout patterns across different student categories

This provides an overall view of student outcomes.

---

 3. Engagement Analysis

Students are grouped according to their engagement level.

This helps answer:

> How are students distributed across different engagement categories?**

The analysis counts unique students within each engagement category.

---

 4. Performance Analysis

Student performance levels are analyzed using:

* Number of students
* Average score
* Performance categories

This makes it possible to compare the size and average score of different performance groups.

---

5. Risk-Level Analysis

Students are grouped according to their risk level.

This analysis helps understand how the student population is distributed across different risk categories.

---

 🔗 Engagement vs Performance

One of the central analyses in this project is the relationship between **student engagement and academic performance**.

The analysis compares:

```text
Engagement Level
       │
       ▼
Number of Students
       │
       ▼
Average Score
```

This allows the different engagement categories to be compared based on their average student scores.

> **Important:** The analysis identifies associations in the dataset; it does not establish that engagement directly causes a change in performance.

---

# Online Activity Analysis

`total_clicks` is used as an indicator of online activity.

Students are divided into activity bands:

```text
0 – 500
500 – 1,000
1,000 – 2,000
2,000 – 3,000
3,000+
```

The average score for each activity band is then compared.

This provides a more detailed view of how academic performance varies across different levels of platform activity.

---

#  Engagement vs Dropout

The project goes beyond simply counting dropouts.

It calculates dropout rates for each engagement category.

```text
Engagement Level
       │
       ├── Total Students
       │
       ├── Dropout Students
       │
       └── Dropout Rate (%)
```

This helps identify differences in dropout patterns between engagement groups.

---

# Performance vs Dropout

Dropout rates are also compared across performance levels.

This analysis examines:

* Total students in each performance group
* Number of dropout students
* Dropout rate

It provides another perspective on the relationship between academic performance categories and student outcomes.

---

#  Regional Analysis

Student data is also analyzed by region.

For every region, the project examines:

* Number of students
* Average score
* Average clicks

This enables regional comparisons of both **academic performance and online activity**.

---

# 🎓 Education-Level Analysis

The project also examines the relationship between **highest education level** and student outcomes.

The analysis compares:

* Number of students
* Average score
* Average clicks

across education categories.

---

# Power BI Dashboard

The SQL analysis is presented through an interactive **Power BI dashboard**.

### Dashboard focus areas

**Student Overview**

* Total Students
* Average Score
* Average Clicks

 **Engagement**

* Engagement distribution
* Engagement vs Average Score
* Activity/Click analysis

**Performance**

* Performance distribution
* Average score by performance level

 **Risk & Dropout**

* Risk-level distribution
* Dropout analysis
* Engagement vs dropout
* Performance vs dropout

 **Student Segmentation**

* Region
* Highest education level

---

#  Insights This Project Can Reveal

The analysis framework is designed to answer questions such as:

### Engagement

* Which engagement categories contain the most students?
* How does average performance vary between engagement groups?

### Activity

* How does average score vary across different click ranges?
* Do highly active and less active students show different performance patterns?

### Dropout

* How does dropout rate vary across engagement levels?
* How does dropout rate vary across performance levels?

### Risk

* Which risk categories contain the largest student populations?

### Demographics

* How do regions differ in average score and online activity?
* How does highest education level vary with student performance and activity?

---

#  SQL Concepts Demonstrated

This project demonstrates practical SQL skills including:

```text
SELECT
COUNT()
COUNT(DISTINCT)
SUM()
AVG()
ROUND()
CASE WHEN
GROUP BY
ORDER BY
Conditional Aggregation
Percentage Calculation
```

The queries use these concepts to turn raw student records into analytical summaries.

---

#  Repository Structure

```text
Online-Learning-Engagement-Analysis/
│
├── 📄 README.md
│
├── 📄 data.sql
│
├── 📄 query.sql
│
├── 📊 powerdidata.pbix
│
└── 📂 screenshots/
    └── dashboard.png
```

---

#  How to Run

## Step 1 — Create the Database

Open MySQL and create the database:

```sql
CREATE DATABASE online_education_db;

USE online_education_db;
```

## Step 2 — Load the Data

Import the SQL/data file into the database and make sure the table:

```text
online_education_dataset
```

is available.

## Step 3 — Run the Analysis

Open:

```text
query.sql
```

Execute the queries in MySQL Workbench or another MySQL client.

## Step 4 — Open Power BI

Open:

```text
powerdidata.pbix
```

using **Power BI Desktop**.

## Step 5 — Explore the Dashboard

Use the dashboard visuals and filters to investigate student engagement, performance, activity, risk, dropout, region, and education-level patterns.

---

# 📌 Project Highlights

 **SQL-driven analysis**
Uses MySQL to transform student-level records into meaningful analytical summaries.

📊 **Interactive visualization**
Power BI is used to present the analysis in an accessible dashboard format.

🎯 **Student-centric analysis**
The project connects engagement, activity, performance, risk, and dropout indicators.

🔍 **Multi-dimensional analysis**
Students are examined from multiple perspectives including engagement, performance, region, and education.

📈 **Decision-support approach**
The project demonstrates how educational data can be converted into information that supports further investigation and intervention planning.

---

#  Future Enhancements

The project can be extended with:

* Predictive student performance models
* Early dropout-risk prediction
* Student segmentation using clustering
* Time-based engagement analysis
* Automated Power BI refresh
* More detailed demographic analysis
* Machine-learning-based outcome prediction
* Personalized learning recommendations

---

#  Skills Demonstrated

**Data Analytics | SQL | MySQL | Power BI | Data Visualization | Exploratory Data Analysis | Business Intelligence | KPI Analysis | Data Interpretation | Dashboard Development**

---

# 👩‍💻 Author

**Lakshmi Tulasi**

**MCA Student | Aspiring Data Analyst**

### Areas of Interest

`SQL` · `Power BI` · `Data Analytics` · `Python` · `MySQL` · `Business Intelligence`

---

## ⭐ Project Summary

> **An end-to-end educational analytics project that uses SQL and Power BI to explore online learning engagement, student performance, activity, risk, and dropout patterns.**

If you found this project useful, feel free to ⭐ the repository.
