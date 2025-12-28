## Instacart - Grocery Delivery Platform Analysis
Analyzed Instacart's grocery delivery platform data to understand customer purchasing patterns, identify peak ordering times, and optimize inventory and delivery operations. Processed multiple datasets to uncover insights about order frequency, product popularity, and user behavior to support business decisions.

## 1. Objectives 🎯
- Load and preprocess multiple Instacart datasets containing order, product, and user information
- Identify and handle missing values and duplicate entries across all datasets
- Verify data integrity and ensure appropriate data types for analysis
- Analyze customer ordering patterns by day of week and hour of day
- Examine time intervals between customer orders to understand purchasing frequency
- Investigate product department and aisle distributions to optimize inventory management
- Prepare clean, reliable datasets for further business intelligence applications

## 2. Key Findings 🏆
- Identified and removed 15 duplicate orders that occurred specifically on Wednesdays at 2:00 AM
- Found 1,258 missing product names, all associated with aisle_id 100 and department_id 21
- Discovered 28,817 missing values in days_since_prior_order, all corresponding to customers' first orders
- Located 836 missing values in add_to_cart_order, with affected orders containing 65+ products
- Confirmed order_hour_of_day ranges from 0-23 and order_dow ranges from 0-6, validating data quality
- Observed peak ordering hours between 10 AM and 8 PM, with the highest activity around 3 PM
- Determined Wednesday and Thursday are the most popular shopping days
- Established that missing add_to_cart_order values represent orders exceeding 64 products

## 3. Visualizations Included 🎨
- Hourly order distribution histogram showing customer ordering patterns throughout the day
- Daily order frequency analysis by day of week
- Data type verification visualizations for key columns
- Missing value heatmaps across all datasets
- Duplicate record identification displays

## 4. Skills Demonstrated 🛠️
- Data Integration: Merging and relating multiple datasets (orders, products, aisles, departments)
- Data Cleaning: Handling missing values, removing duplicates, correcting data types
- Data Validation: Verifying value ranges and business logic constraints
- Exploratory Analysis: Identifying patterns in customer behavior and product data
- Data Quality Assessment: Detecting anomalies and inconsistencies in raw data
- Problem Solving: Developing strategies to handle various data quality issues
- Documentation: Creating clear explanations of data preprocessing decisions and findings

## 5. Technical Details 💻
- Programming Language: Python
- Main Libraries: pandas, matplotlib
- Datasets: instacart_orders.csv, products.csv, order_products.csv, aisles.csv, departments.csv
- Data Volume: 478,967 initial orders, 49,694 products, 4,545,007 order items
- Preprocessing Tasks: Missing value imputation, duplicate removal, data type conversion
- Key Columns Processed: product_name, days_since_prior_order, add_to_cart_order
- Special Handling: Used 999 as placeholder for missing add_to_cart_order values

## 6. Installation and Usage
```bash
# Clone the repository
git clone https://github.com/yourusername/instacart-analysis.git

# Navigate to project directory
cd instacart-analysis

# Install required dependencies
pip install pandas matplotlib

# Run the analysis notebook
jupyter notebook Instacart-Grocery_Delivery_Platform.ipynb



