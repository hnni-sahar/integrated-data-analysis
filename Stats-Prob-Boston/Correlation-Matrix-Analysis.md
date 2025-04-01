## Correlation Analysis of the Boston Housing Dataset

*The analysis is based on the Boston Housing dataset, which includes information on housing values, tax rates, and other features. This analysis was part of the **DetailedBoston** question in the **Statistics and Probability** section of my Quera Data Analysis Bootcamp.*

### Feature Descriptions
- **crim**: Crime rate in the area.
- **zn**: Percentage of big residential areas (lots bigger than 25,000 sq. ft.).
- **indus**: Percentage of land used for industries, not shops.
- **chas**: Is the property near the Charles River? (1 = Yes, 0 = No).
- **nox**: Air pollution level (nitric oxide concentration).
- **rm**: Average number of rooms in a house.
- **age**: Percentage of houses built before 1940.
- **dis**: Distance to nearby job centers.
- **rad**: How easy it is to get to highways.
- **tax**: Property tax rate.
- **ptratio**: Number of students per teacher in schools.
- **b**: A special calculation related to the Black population in the area.
- **lstat**: Percentage of low-income population.
- **medv**: Median house value in thousands of dollars.

### 1. Factors Affecting House Prices (MEDV)

#### **Positively Correlated Features:**
- **RM (Number of rooms) (~0.7):** More rooms in a house generally lead to higher prices.
- **DIS (Distance to job centers):** Houses farther from job centers tend to be more expensive, possibly indicating suburban or luxury residential areas.

#### **Negatively Correlated Features:**
- **LSTAT (Percentage of low-income population) (~-0.74):** A higher percentage of low-income residents is associated with lower house prices.
- **PTRATIO (Student-to-teacher ratio) (~-0.51):** Higher student-to-teacher ratios suggest lower education quality, reducing property values.
- **CRIM (Crime rate) (~-0.39):** Higher crime rates generally lead to lower house prices.
- **NOX (Air pollution level) (~-0.42):** More polluted areas tend to have lower property values.
- **INDUS (Percentage of industrial land) (~-0.48):** Industrialized regions often have lower housing prices due to pollution and noise.

---

### 2. Key Correlations Between Independent Variables
- **TAX and RAD (~0.91):** Higher property tax rates are strongly associated with better access to highways.
- **INDUS and NOX (~0.77):** Industrial areas tend to have higher pollution levels.
- **AGE and NOX (~0.73):** Older houses are often located in more polluted areas, possibly due to outdated heating systems or nearby factories.

---

### 3. Key Takeaways for Modeling & Feature Selection
- The most influential features for predicting house prices are:  
  **RM, LSTAT, PTRATIO, CRIM, TAX, NOX, INDUS**
- Features with high correlation (**TAX and RAD**) may cause multicollinearity issues, so one of them might need to be removed in predictive models.
- Some features, such as **CHAS (proximity to the Charles River),** have minimal impact on house prices and might not be significant for modeling.

### Conclusion
This correlation analysis helps identify the most relevant features affecting house prices in Boston. Further analysis, such as regression modeling and feature engineering, can enhance predictions and improve model accuracy.


