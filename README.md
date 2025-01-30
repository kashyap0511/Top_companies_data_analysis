# Top 10,000 Companies Data Analysis

## Introduction
This project analyzes data from the top 10,000 companies across various sectors to extract insights about ratings, salaries, job availability, and benefits. The goal is to provide actionable information for prospective employees and stakeholders.

## Objectives
- Evaluate company ratings and their relationship with salary structures.
- Compare interviews taken and job availability.
- Identify industries with the highest market share.
- Analyze benefits and critical factors influencing employee satisfaction.

## Data Source
- Dataset: `companies.csv` (kaggle).

## Technical Requirements
- **Python Libraries**:
  - `pandas`, `numpy`: Data manipulation.
  - `matplotlib`, `seaborn`: Visualization.
  - `warnings`: Handle warnings.
- **Tools**: Jupyter Notebook.

## Project Structure
### 1. **Data Collection**
   - Load the dataset using `pd.read_csv`.
   - Initial exploration with `head()`, `shape`, and `info()`.

### 2. **Data Cleaning**
   - Handle missing values in `Highly_rated_for` and `Critically_rated_for` by filling "Not Rated".
   - Remove duplicate rows, reducing the dataset from 10,000 to 9,359 entries.

### 3. **Data Transformation**
   - Convert columns like `Total_reviews`, `Avg_salary`, and `Interviews_taken` from strings (e.g., "73.1k") to numeric values.
   - Split the `Description` column into `Industry`, `Employees`, `Company_type`, and `Company's_years`.

### 4. **Analysis & Visualization**
   - **Descriptive Statistics**: Summary of ratings, salaries, and jobs.
   - **Distributions**:
     - Ratings: Most companies cluster between 3.7 and 4.1.
     - Average Salary: Skewed toward lower ranges (25th percentile: ₹2.5L, median: ₹3.26L).
   - **Top Companies**:
     - *Most Benefits*: Whitehat Jr, Sutherland Global Services, Asian Paints.
     - *Highest-Rated*: Matrimonialsindia, Stirring Winds (5.0 ratings).
   - **Market Share by Industry**:
     - IT Services & Consulting (13.07%), Engineering & Construction (4.98%), Auto Components (4.56%).
   - **Highest Jobs vs. Interviews**:
     - Indianart Intermesh (374k interview taken where number of jobs is 981k)
   - **Highest Interviews vs. Jobs**:
     - Flipkart (972k interviews taken where number of job is 364k).
   - **Correlation Analysis**:
     - Strong positive correlation between `Interviews_taken` and `Total_benefits` (0.71).

## Key Findings
- **IT Dominance**: IT Services & Consulting leads in market share.
- **Benefits Drive Engagement**: Companies offering high benefits attract more interviews.
- **Salary-Rating Mismatch**: Higher ratings don’t always correlate with higher salaries (e.g., top-rated companies have modest salaries).
