# Student Performance Dataset Analysis

This project involves the analysis of the **Student Performance** dataset, including various statistical tests and visualizations. The dataset is sourced from two separate files, `student-mat.csv` (Mathematics) and `student-por.csv` (Portuguese), which were merged based on common columns.

## Dataset

The datasets are obtained from the [UCI Machine Learning Repository](https://archive.ics.uci.edu/dataset/320/student+performance). The key columns include:
- `school`: School
- `sex`: Gender
- `age`: Age
- `address`: Address
- `famsize`: Family Size
- `Pstatus`: Family Status
- `Medu`: Mother's Education
- `Fedu`: Father's Education
- `Mjob`: Mother's Job
- `Fjob`: Father's Job
- `reason`: Reason for School Choice
- `nursery`: Nursery
- `internet`: Internet Access

## Libraries Used
- `pandas`: For data manipulation and analysis.
- `scipy`: For statistical tests.
- `numpy`: For numerical computations.
- `matplotlib`: For creating visualizations.
- `seaborn`: For statistical data visualization.


## Data Processing

The two datasets were merged based on common columns (`school`, `sex`, `age`, `address`, `famsize`, `Pstatus`, `Medu`, `Fedu`, `Mjob`, `Fjob`, `reason`, `nursery`, `internet`), resulting in a dataset of 382 students.

## Visualizations

Several visualizations have been created to understand the distribution and relationships in the dataset:
- **Bar Plots**: To visualize the distribution of categorical variables.
- **Pair Plots**: To explore pairwise relationships between numerical variables.
- **Box Plots**: To compare the distributions of numerical variables across different groups.

Here are some examples of the visualizations:

![image](https://github.com/user-attachments/assets/889b5ec9-4527-458b-8488-a68257ce3372)
![image](https://github.com/user-attachments/assets/03fe1d00-bfeb-4344-aa95-6717717c0726)
![download](https://github.com/user-attachments/assets/6f11f9e5-5c86-4fab-b587-3c84ef9e4de0)
![download](https://github.com/user-attachments/assets/4e81ac42-7fa8-4928-99a4-02bf7336e792)

### Normality Tests

- **Studytime_x**
  - Shapiro-Wilk Test: `stat = 0.834`, `p-value = 6.548e-20` (Non-normal)
  - D'Agostino's K^2 Test: `stat = 23.12`, `p-value = 9.54e-06` (Non-normal)
  - Anderson-Darling Test: `stat = 27.58`, critical values: `15.0% = 0.57`, `10.0% = 0.65`, `5.0% = 0.779`, `2.5% = 0.909`, `1.0% = 1.081` (Non-normal)

- **Age**
  - Shapiro-Wilk Test: `stat = 0.910`, `p-value = 1.59e-14` (Non-normal)
  - D'Agostino's K^2 Test: `stat = 13.44`, `p-value = 0.00121` (Non-normal)
  - Anderson-Darling Test: `stat = 12.31`, critical values: `15.0% = 0.57`, `10.0% = 0.65`, `5.0% = 0.779`, `2.5% = 0.909`, `1.0% = 1.081` (Non-normal)

### Correlation Tests

- **Chi-Squared Test**
  - **Mathematics:**
    - G1 vs. G2: `Chi2 = 370.21`, `p-value = 7.57e-79`
    - G1 vs. G3: `Chi2 = 325.20`, `p-value = 3.95e-69`
    - G2 vs. G3: `Chi2 = 442.53`, `p-value = 1.79e-94`
  - **Portuguese:**
    - G1 vs. G2: `Chi2 = 404.32`, `p-value = 3.24e-86`
    - G1 vs. G3: `Chi2 = 325.74`, `p-value = 3.02e-69`
    - G2 vs. G3: `Chi2 = 450.24`, `p-value = 3.86e-96`

- **Spearman's Rank Correlation Test**
  - **Mathematics:**
    - G1 vs. G2: `rho = 0.90`, `p-value = 8.26e-139`
    - G1 vs. G3: `rho = 0.88`, `p-value = 6.48e-124`
    - G2 vs. G3: `rho = 0.96`, `p-value = 7.77e-204`
  - **Portuguese:**
    - G1 vs. G2: `rho = 0.90`, `p-value = 8.26e-139`
    - G1 vs. G3: `rho = 0.88`, `p-value = 6.48e-124`
    - G2 vs. G3: `rho = 0.96`, `p-value = 7.77e-204`

- **Kendall's Tau Correlation Test**
  - **Mathematics:**
    - G1 vs. G2: `Tau = 0.78`, `p-value = 1.99e-99`
    - G1 vs. G3: `Tau = 0.75`, `p-value = 4.89e-91`
    - G2 vs. G3: `Tau = 0.88`, `p-value = 7.36e-126`
  - **Portuguese:**
    - G1 vs. G2: `Tau = 0.78`, `p-value = 1.99e-99`
    - G1 vs. G3: `Tau = 0.75`, `p-value = 4.89e-91`
    - G2 vs. G3: `Tau = 0.88`, `p-value = 7.36e-126`

### Non-Parametric Tests

- **Mann-Whitney U Test**
  - **Mathematics:**
    - G1 vs. G2: `U = 71805.0`, `p-value = 0.702`
    - **Portuguese:**
    - G1 vs. G2: `U = 72526.0`, `p-value = 0.886`

- **Kruskal-Wallis H Test**
  - **Mathematics:**
    - G2 vs. G3: `stat = 0.007`, `p-value = 0.932`
  - **Portuguese:**
    - G2 vs. G3: `stat = 5.15`, `p-value = 0.023`

- **Friedman Test**
  - **Mathematics:**
    - `stat = 1.63`, `p-value = 0.443`
  - **Portuguese:**
    - `stat = 78.50`, `p-value = 8.99e-18`


## Conclusion

The statistical tests conducted reveal that none of the variables in the dataset follow a normal distribution. Consequently, non-parametric tests were employed to analyze the data:

- **Chi-Squared Tests** indicated significant associations between the different grading periods (G1, G2, and G3) for both Mathematics and Portuguese scores.
- **Spearman's Rank Correlation** and **Kendall's Tau Correlation** demonstrated strong correlations between the grading periods, suggesting consistent performance trends.
- **Non-Parametric Tests** such as the Mann-Whitney U Test, Kruskal-Wallis H Test, and Friedman Test further supported the observations, particularly showing significant differences in Portuguese data across grading periods.

The visualizations provided help in understanding the data distribution and relationships between different variables.







