# Trading Data Assessment Report
This report analyzes a trading dataset focusing on data quality, profitability patterns, and key factors contributing to trading success.

# 1. Dataset Overview
# 1.1 Basic Information
**OUTPUT**
| Metric | Value |
|Total Records | 59,317 entries | 
| Total Columns | 14 |
| Data Completeness | 100% (No NULL or Missing Values) |
| Data Quality | No Duplicate records found

**OUTPUT**
| Metric | Value | PRICEEACH | ORDERLINENUMBER | SALES   | ORDERDATE | STATUS  | QTR_ID | MONTH_ID | YEAR_ID | PRODUCTLINE | MSRP | PRODUCTCODE | CUSTOMERNAME          | PHONE       | ADDRESSLINE1            | ADDRESSLINE2 | CITY          | STATE | POSTALCODE | COUNTRY | TERRITORY | CONTACTLASTNAME | CONTACTFIRSTNAME | DEALSIZE |
|-------------|------------------|
| 10107       | 30.00            | 95.70     | 2                | 2871.00 | 24/2/03   | Shipped | 1      | 2        | 2003    | Motorcycles | 95   | S10_1678    | Land of Toys Inc.     | 2125557818  | 897 Long Airport Avenue |              | NYC           | NY    | 10022      | USA     | NA        | Yu              | Kwai             | Small    |
| 10121       | 34.00            | 81.35     | 5                | 2765.90 | 7/5/03    | Shipped | 2      | 5        | 2003    | Motorcycles | 95   | S10_1678    | Reims Collectables    | 26.47.1555  | 59 rue de l'Abbaye     |              | Reims         |       | 51100      | France  | EMEA       | Henriot         | Paul             | Small    |
| 10134       | 41.00            | 94.74     | 2                | 3884.34 | 1/7/03    | Shipped | 3      | 7        | 2003    | Motorcycles | 95   | S10_1678    | Lyon Souveniers       | +33 1 46 62 7555 | 27 rue du Colonel Pierre Avia |              | Paris         |       | 75508      | France  | EMEA       | Da Cunha        | Daniel           | Medium   |
| 10145       | 45.00            | 83.26     | 6                | 3746.70 | 25/8/03   | Shipped | 3      | 8        | 2003    | Motorcycles | 95   | S10_1678    | Toys4GrownUps.com     | 6265557265  | 78934 Hillside Dr.     |              | Pasadena      | CA    | 90003      | USA     | NA        | Young           | Julie            | Medium   |
| 10159       | 49.00            | 100.00    | 14               | 5205.27 | 10/10/03  | Shipped | 4      | 10       | 2003    | Motorcycles | 95   | S10_1678    | Corporate Gift Ideas Co. | 6505551386  | 7734 Strong St.        |              | San Francisco | CA    |            | USA     | NA        | Brown           | Julie            | Medium   |


2. Data Handling & Exploration
2.1 Data Cleaning Steps

Handling Missing & Duplicate Values: Checked for missing and duplicate values. None found.
Column Standardization: Renamed columns with spaces to underscore format

Example: take profit → take_profit


Whitespaces: Removed leading and trailing whitespaces from string values.
DateTime Conversion: Converted time columns (e.g., open_time, close_time) to proper datetime format.
Numeric Validation: Created a list of columns that contains crucial financial data and converted them into numeric floating point numbers to handle NaN, inconsistent, and non-numeric values.

2.2 Data Wrangling Steps

Profitable Flag: Binary indicator (1 for profit, 0 otherwise)
Price Change: Absolute difference between close_price and open_price
Pips per Volume: Efficiency metric with 1e-6 added to prevent division by zero
Trade Duration: Calculated in both seconds and hours


3. Profitability Analysis
3.1 Top 5 Most Profitable Logins
RankLogin IDTotal Profit113378390$53,891.98255009560$28,475.44313088202$27,848.61413205503$27,049.34513070589$27,023.68
3.2 Top 5 Least Profitable Logins
RankLogin IDTotal Profit113103928-$14,778.82213333728-$13,868.00355011482-$12,215.00413018096-$12,194.31513251499-$11,405.24
3.3 Distribution of Profit across Different Logins
Based on the histogram analysis, the profit distribution appears right-skewed with a long tail toward positive profits. Most logins cluster around breakeven or modest profits, indicating high variability in trading outcomes.

4. Key Insights & Interpretations
4.1 Profitability Factors

Trade Efficiency Metrics

Better entry and exit timing
Capital allocation
Risk-reward ratios


Trade Duration Strategy

Time-based performance correlations
Holding period optimization


Risk Management Excellence

Smart use of stop-loss orders
Position sizing
Better risk-reward ratios



4.2 Performance Disparity
Insights: The top performer achieved almost $54,000 in profit, while the least profitable trader lost approximately $15,000.
Interpretation: This significant difference indicates variations in:

Trader skill levels
Trading strategies
Understanding of market conditions
Risk management approaches
