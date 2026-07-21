# Statistics-Mathematics-in-DS
A comprehensive reference guide and code repository covering fundamental Mathematics and Statistics for Data Science—including Linear Algebra, Calculus, Probability, and Inferential Statistics.


# Mathematics & Statistics for Data Science 📐📊

Welcome to the **Mathematics & Statistics for Data Science** repository! Mathematics and Statistics form the backbone of Data Science, Machine Learning, and Artificial Intelligence algorithms. 

This repository serves as a hands-on guide translating core mathematical formulas and statistical principles into practical Python code using libraries like `NumPy`, `SciPy`, `Pandas`, and `Matplotlib`.

---

## 🚀 Key Modules Covered

### 1. Linear Algebra 🔢
The foundation for handling multi-dimensional data, matrices, and vector spaces:
* **Vectors & Matrices:** Dot products, matrix multiplication, rank, and transpose.
* **Matrix Decompositions:** Eigenvalues, Eigenvectors, and Principal Component Analysis (PCA) intuition.
* **Systems of Linear Equations:** Solving linear equations using matrix inversion (`np.linalg.solve`).

### 2. Calculus 📉
Understanding how Machine Learning algorithms learn and optimize:
* **Derivatives & Partial Derivatives:** Rates of change and slopes.
* **Gradient Descent:** Understanding how loss functions are minimized in ML models.
* **Integral Calculus:** Area under the curve (AUC) and Probability Density Functions (PDF).

### 3. Descriptive Statistics 📊
Summarizing and understanding raw data distributions:
* **Measures of Central Tendency:** Mean, Median, and Mode.
* **Measures of Dispersion:** Range, Variance, Standard Deviation, and Interquartile Range (IQR).
* **Shape of Data:** Skewness (left/right bias) and Kurtosis (tail heaviness).

### 4. Probability & Probability Distributions 🎲
Modeling uncertainty and likelihoods:
* **Basic Probability:** Conditional Probability, Independent events, and Bayes' Theorem.
* **Discrete Distributions:** Binomial and Poisson distributions.
* **Continuous Distributions:** Normal (Gaussian) Distribution, Standard Normal Distribution ($Z$-score), and Uniform distribution.

### 5. Inferential Statistics & Hypothesis Testing 🧪
Drawing insights and conclusions about population parameters from sample data:
* **Central Limit Theorem (CLT):** The foundation of sampling distribution.
* **Confidence Intervals:** Estimating population parameters with a margin of error.
* **Hypothesis Testing:**
  * Null Hypothesis ($H_0$) vs. Alternative Hypothesis ($H_1$).
  * $p$-values, Significance level ($\alpha$), and Type I/Type II errors.
  * $Z$-test, $t$-test (One-sample, Two-sample, Paired), Chi-Square test ($\chi^2$), and ANOVA.

---

## 🛠️ Python Libraries Used

* **Mathematics & Linear Algebra:** `NumPy`, `SciPy`
* **Data Handling:** `Pandas`
* **Visualization & Plotting:** `Matplotlib`, `Seaborn`

---

## 💻 Sample Code Snippet (Hypothesis Testing in Python)

Here is a quick example of running a 2-sample $t$-test using Python's `scipy.stats`:

```python
import numpy as np
from scipy import stats

# Generating two independent sample groups
group_a = np.random.normal(loc=70, scale=10, size=50) # Mean = 70
group_b = np.random.normal(loc=75, scale=10, size=50) # Mean = 75

# Performing a Two-Sample Independent T-Test
t_stat, p_value = stats.ttest_ind(group_a, group_b)

print(f"T-statistic: {t_stat:.4f}")
print(f"P-value: {p_value:.4f}")

# Decision making at 5% Significance Level (alpha = 0.05)
if p_value < 0.05:
    print("Reject Null Hypothesis: Significant difference found between groups.")
else:
    print("Fail to Reject Null Hypothesis: No significant difference found.")
