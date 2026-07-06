# Student Exam Performance Analysis

Exploratory data analysis of student exam scores, examining how factors like test preparation, parental education, lunch type, and race/ethnicity relate to academic performance.

## Objective

To understand which factors are most strongly associated with student exam performance, and to identify actionable patterns (e.g. does test preparation help, and does it help all student groups equally?).

## Dataset

- **Source:** [Students Performance in Exams](https://www.kaggle.com/datasets/spscientist/students-performance-in-exams) (Kaggle)
- **Size:** 1000 rows, 8 columns
- **Columns:** gender, race/ethnicity, parental level of education, lunch type, test preparation course, math score, reading score, writing score

## Tech Stack

- Python
- Pandas (data loading, cleaning, feature engineering)
- Matplotlib & Seaborn (visualization)
- Jupyter Notebook

## Workflow

1. Load and inspect the dataset (shape, columns, nulls, duplicates)
2. Clean column names (lowercase, underscores)
3. Feature engineering — created an `average_score` column (mean of math, reading, and writing scores)
4. Exploratory analysis across gender, lunch type, parental education, race/ethnicity, and test preparation
5. Two-factor analysis — combined lunch type with test preparation to uncover a deeper pattern
6. Correlation analysis between the three subject scores

## Key Insights

- **Test preparation matters:** students who completed a test prep course averaged 72.67, versus 65.04 for those who didn't — a gap of about 7.6 points.
- **Lunch type shows the largest single-factor gap:** students with standard lunch averaged 70.84, versus 62.20 for free/reduced lunch — a gap of about 8.6 points, likely reflecting broader socioeconomic factors.
- **Test prep helps more for lower-income students:** among students with free/reduced lunch, test prep raised scores by about 8.8 points, slightly more than the 7.2 point boost seen among standard-lunch students — suggesting test prep may help narrow, not widen, the economic performance gap.
- **Race/ethnicity shows a steady, gradual trend:** average scores rise consistently from group A (62.99) to group E (72.75), a spread of about 9.8 points across groups.
- **Parental education level shows a clear step-up pattern:** average scores rise from 65.11 (some high school) up to 73.60 (master's degree), though high school (63.10) is slightly lower than "some high school" — worth noting as a small irregularity in an otherwise increasing trend.
- **Reading and writing are nearly interchangeable:** the two scores are highly correlated (0.95), while math shows a comparatively weaker relationship with both (0.80–0.82), suggesting math ability is somewhat more independent of general language performance.
- **Overall score distribution is left-skewed:** most students scored above the average, with a smaller group of lower scorers pulling the tail leftward.

## Future Improvements

- Explore whether gender interacts with subject-specific performance (e.g. does the gender gap differ between math and writing?)
- Add a simple regression model to quantify which factor is the strongest predictor of average score
- Expand the dataset with more features (e.g. study hours, attendance) if a larger version becomes available

## Project Structure

```
Student-Exam-Performance-Analysis/
├── Data/
│   └── StudentsPerformance.csv
├── Notebook/
│   └── exam_analysis.ipynb
└── README.md
```
