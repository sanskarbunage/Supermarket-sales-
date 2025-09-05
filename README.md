1. Data Understanding
Loaded dataset into Python (Pandas).
Checked shape, column names, and datatypes.
Reviewed first few rows to understand structure (customers, sales, payments, products, etc.).

2. Data Cleaning
Column Formatting:
Converted all column headers to lowercase for consistency.
Renamed columns with spaces → snake_case (e.g., Unit price → unit_price).
Missing Values:
Checked for NaN values across dataset.
Filled missing numeric values with median (robust against outliers).
Filled categorical missing values with mode (most frequent category).
Data Types:
Converted date column to proper datetime format.
Extracted day, month, year from date for analysis.
Separated date and time into two columns (if combined).
Duplicates:Checked and dropped duplicate rows.
Categorical Formatting:Converted gender, city, customer_type, product_line, payment into categorical type.
Standardized values (e.g., lowercase male/female).
Numerical Fixes:
Converted object-type numeric columns into float (if any currency symbol was present).
Checked for negative or unrealistic values (cleaned if found).

3. Feature Engineering
Created total_price = unit_price × quantity (if not already provided).
Extracted day_name (Mon–Sun) from date.
Created time_of_day column (Morning, Afternoon, Evening) from transaction time.
Derived profit margin = gross_income / total.

4. Exploratory Data Analysis (EDA)
Descriptive Stats: Mean, median, mode for numeric columns.
Univariate Analysis:
Distribution of unit_price, quantity, rating.
Countplots of categorical columns (city, gender, payment, product_line).
Bivariate Analysis:
Average sales by city, gender, customer type.
Relationship between total and payment method.

5. Insights Derived
Which product line generated most revenue.
Which city contributed highest sales.
Which payment method was most used.
Who spent more on average: members vs normal customers, male vs female.
Rating distribution across different product lines.
