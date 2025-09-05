# Exploratory Data Analysis of Paris Housing Dataset

This project performs a comprehensive exploratory data analysis (EDA) on the `ParisHousingClass.csv` dataset. The goal is to uncover key insights, distributions, and relationships between various housing features in Paris using a variety of data visualization techniques.

The analysis is conducted using Python with the following libraries:
- **Pandas**  
  For data loading, manipulation, and aggregation.
- **Matplotlib** and **Seaborn**  
  For creating a wide range of static visualizations.

---

## Visualizations

The analysis is broken down into several categories, each using a different type of chart to highlight specific aspects of the data.

### Univariate Analysis

These charts examine the distribution of a single variable.

- **Histograms**  
  Used to visualize the distribution of continuous variables like `price` and `squareMeters`. A histogram of `price` also uses a hue to show the distribution by `category` (Basic vs. Luxury).
- **Count Plots**  
  Used to show the frequency of categorical variables like `cityPartRange` and `hasPool`.

### Bivariate Analysis

These charts explore the relationship between two variables.

- **Scatter Plots**  
  Used to show the relationship between `squareMeters` and `price`. This helps in understanding the correlation between a house's size and its cost.
- **Box Plots**  
  Used to compare the distribution of a continuous variable (`price`) across a categorical one (`category` or `hasStormProtector`). This provides a clear visual of median values, quartiles, and outliers.

### Correlation Analysis

These charts provide a high-level overview of relationships across multiple features.

- **Correlation Heatmap**  
  A visual matrix showing the correlation coefficients between all numerical features in the dataset. This helps to quickly identify which variables are most strongly related.
- **Pair Plot**  
  A powerful grid of plots that shows the relationship between every pair of variables in a selected list. The diagonal plots show the distribution of each variable, while the off-diagonal plots show scatter plots between the pairs.

### Proportional Breakdown

These charts are ideal for showing the percentage breakdown of a single categorical variable.

- **Pie Charts**  
  Used to visualize the proportion of houses with a pool versus those without (`hasPool`). This is also used to show the percentage breakdown of houses by their `category` (Basic vs. Luxury).
