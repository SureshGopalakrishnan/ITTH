# Hotel Booking Exploratory Data Analysis (EDA)

This project conducts a detailed exploratory data analysis on a hotel booking dataset to uncover patterns and trends. The primary objective is to understand the factors influencing booking cancellations, which is crucial for revenue management and business strategy.

---

## **1. Data Overview and Preparation**

The analysis begins with data inspection, including checking for missing values, data types, and a statistical summary. Key steps include:

* **Data Cleaning:** We handle missing values and remove entries with logical inconsistencies, such as those with an `adr` (Average Daily Rate) of zero.
* **Feature Engineering:** New, informative variables are created from existing data to enhance the analysis. These include `total_guests`, `total_nights`, and a combined `arrival_date`.
* **Data Transformation:** Categorical variables like `hotel` and `is_canceled` are converted to numerical representations for plotting and correlation analysis.

---

## **2. Key Visualizations and Insights**

The core of this EDA is a series of visualizations that reveal significant insights into booking behavior.

### **Cancellation Rate by Hotel Type**

A bar chart shows the cancellation rate for both "City Hotel" and "Resort Hotel."

> **Insight:** Resort hotels have a higher cancellation rate than city hotels, suggesting a potential difference in customer booking behavior or cancellation policies between the two.

### **Monthly Cancellation Rate by Hotel Type**

A line plot tracks the percentage of cancellations over each month of the year for both hotel types.

> **Insight:** Cancellations follow a clear seasonal pattern. City hotels have a consistently higher cancellation rate, with peaks in April and August. Resort hotels show a dramatic spike in cancellations during the peak summer months of June, July, and August.

### **Cancellation Rate by Market Segment**

A bar chart compares cancellation rates across different market segments, such as `Online TA` (Online Travel Agents), `Corporate`, and `Direct`.

> **Insight:** The `Online TA` and `Groups` segments have the highest cancellation rates, while `Corporate` and `Direct` bookings are much more reliable, showing a much lower rate of cancellation. This is a critical finding for marketing and sales strategies.

### **Lead Time Distribution for Canceled Bookings**

A Kernel Density Estimate (KDE) plot visualizes the distribution of `lead_time` for canceled bookings, split by hotel type.

> **Insight:** This plot reveals a crucial difference in customer behavior. City hotel cancellations often occur with a short lead time (0-25 days), suggesting last-minute changes. Resort hotel cancellations, on the other hand, are often made much further in advance (100-200 days), possibly due to long-term vacation planning.

---

## **3. Project Structure and How to Run**

The analysis is performed using a Python script designed for a Jupyter Notebook or Google Colab environment

**Libraries Used:**

-   `pandas` for data manipulation
-   `numpy` for numerical operations
-   `seaborn` and `matplotlib` for data visualization
-   `calendar` for date-related conversions

## 4. Next Steps
The insights from this EDA provide a strong foundation for future work. Next steps could include

* Further Visualizations: Creating additional plots to explore the impact of other variables, such as deposit_type, customer_type, or country
* Feature Engineering: Building more complex features, such as family_booking or season, to improve a future predictive model
* Predictive Modeling: Using the cleaned and prepared data to build a machine learning model that can predict which bookings are most likely to be cancelled
