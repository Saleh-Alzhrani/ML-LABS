In this lab, we perform Exploratory Data Analysis (EDA).
 
The goal is to clean the data, visualize key patterns, and prepare the dataset for machine learning models (Regression) to predict the Sales Amount.

**Dataset Description**:

The dataset contains transaction records for coffee sales across different countries.

**Target Variable**: `Amount` (Total sales value in USD).
    Features:
    `Boxes Shipped`: Quantity of coffee boxes sold.
    `Product`: Type of coffee (Arabica, Robusta, etc...).
    `Country`: Destination country of the shipment.
    `Date`: Date of the transaction.

**Steps Performed**:

A. Data Cleaning
The raw data contained symbols that prevented numerical analysis. We performed the following  cleaning steps:

**Currency Conversion**: Removed the `$` symbol and comma `,` from the `Amount` column and converted it to a numerical float format.
**Date Parsing**: Converted the `Date` column to a proper DateTime object to allow time-based analysis.

B. Exploratory Data Analysis (EDA)
We used **Matplotlib** and **Seaborn** to visualize relationships:
1.  **Sales by Country:** A bar chart showing which countries have the highest sales volume.
2.  **Sales by Product:** Identifying the most popular coffee types.
3.  **Correlation Analysis:** A heatmap to check the relationship between `Boxes Shipped` and `Amount`.

C. Data Preprocessing (Encoding)
Machine learning models cannot understand text. We applied **Label Encoding / One-Hot Encoding** to convert categorical columns:
`Country` → Converted to numerical values.
`Product` → Converted to numerical values.

**Key Findings**
There is a strong positive correlation between `Boxes Shipped` and `Amount` (as expected).
The dataset is now clean, numerical, and ready for training a Linear Regression model.

**Libraries Used**

**Pandas:** For data manipulation.
**Matplotlib & Seaborn:** For data visualization.

