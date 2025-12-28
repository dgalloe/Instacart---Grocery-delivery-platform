# Instacart - Grocery-delivery-platform
Cleaned and analyzed Instacart's 2017 Kaggle dataset to uncover customer purchasing patterns and provide actionable insights into shopping habits.

# Instacart Data Analysis Project

## 📊 Description
Complete analysis of purchasing patterns on Instacart, including data cleaning, preprocessing, and trend visualization. This project was developed as part of the Tripleten Data Science program.

## 🎯 Objectives
1. Load and explore Instacart datasets
2. Perform data cleaning and preprocessing
3. Analyze purchasing patterns (timing, days, frequency)
4. Visualize findings through informative charts
5. Draw business-relevant conclusions from the data

## 📁 Project Structure

instacart-analysis/
├── instacart_analysis.ipynb # Main analysis notebook
├── requirements.txt # Project dependencies
├── README.md # This file
└── datasets/ # Data folder (not included in repo)
├── instacart_orders.csv
├── products.csv
├── order_products.csv
├── aisles.csv
└── departments.csv


## 🔧 Installation and Usage

### Prerequisites
- Python 3.8+
- Jupyter Notebook or JupyterLab

### Installation
```bash
# Clone the repository
git clone https://github.com/your-username/instacart-analysis.git

# Navigate to directory
cd instacart-analysis

# Install dependencies
pip install -r requirements.txt

# Run Jupyter Notebook
jupyter notebook instacart_analysis.ipynb

## 📈 Key Findings

### 1. Temporal Patterns
- **Peak hour**: 3:00 PM (approximately 120,000 orders)
- **Busiest day**: Saturday
- **Least active period**: Early morning (2:00-6:00 AM)
- Most orders occur between 10:00 AM and 4:00 PM

### 2. User Behavior
- 6% of orders are first-time purchases
- Average time between orders is 7-30 days
- Some users place orders with more than 64 products
- Wednesday at 2:00 AM showed data quality issues (duplicate entries)

### 3. Data Quality Issues Identified and Resolved
- **15 duplicate orders**: All occurring on Wednesday at 2:00 AM (removed)
- **1,258 missing product names**: All in aisle 100, department 21 (filled with "unknown")
- **28,817 missing values** in `days_since_prior_order`: First orders (kept as NaN, valid business case)
- **836 missing values** in `add_to_cart_order`: Orders with >64 products (filled with 999)

## 📊 Visualizations Included
1. **Order distribution by hour of day** (Bar chart)
2. **Order distribution by day of week** (Bar chart)
3. **Distribution of time between orders** (Histogram)

## 🛠️ Data Processing Workflow

### Preprocessing Steps
1. **Data Loading**: All CSV files loaded with correct semicolon separator
2. **Duplicate Detection & Removal**: Identified and removed 15 duplicate orders
3. **Missing Value Treatment**:
   - Product names: Imputed with "unknown"
   - `add_to_cart_order`: Set to 999 for orders with >64 items
   - `days_since_prior_order`: Kept as NaN for first orders (valid business logic)
4. **Data Type Correction**: Ensured all ID columns are integers

### Exploratory Analysis
- Validated data ranges (hours: 0-23, days: 0-6)
- Analyzed purchase frequency patterns
- Investigated reordering behavior
- Examined product and department distributions

## 🎓 Skills Demonstrated
- **Data Manipulation**: Advanced Pandas operations
- **Data Cleaning**: Handling duplicates, missing values, and data type issues
- **Exploratory Data Analysis (EDA)**: Pattern identification and hypothesis testing
- **Data Visualization**: Creating informative charts with Matplotlib
- **Business Insight Extraction**: Translating data findings into actionable insights
- **Project Documentation**: Clear commenting and documentation of analysis process

## 📝 Technical Details

### Libraries Used
- **Pandas**: Data manipulation and analysis
- **Matplotlib**: Data visualization
- **NumPy**: Numerical operations

### Data Challenges Overcome
- Non-standard CSV separators (semicolon instead of comma)
- Mixed data quality across multiple related tables
- Business-specific missing value patterns
- Large dataset optimization (4.5+ million rows in order_products)

### Performance Optimizations
- Efficient use of Pandas vectorized operations
- Appropriate data type selection for memory efficiency
- Batch processing techniques for large datasets

## 👥 Credits
- **Author**: Daniel
- **Reviewer**: Ezequiel Ferrario (Tripleten)
- **Dataset Source**: Instacart (modified for educational purposes by Tripleten)
- **Educational Program**: Tripleten Data Science Bootcamp

## 📄 License
This project is for educational purposes as part of the Tripleten Data Science program.

## 🔗 Related Links
- [Tripleten](https://tripleten.com/)
- [Original Instacart Dataset](https://www.instacart.com/datasets/grocery-shopping-2017)
- [My GitHub Profile](https://github.com/your-username)

---

## Business Recommendations
Based on the analysis, here are potential business improvements for Instacart:

### 1. **Staffing Optimization**
- Schedule more delivery personnel during peak hours (10 AM - 4 PM)
- Prepare for higher weekend demand, especially Saturdays

### 2. **Marketing Opportunities**
- Target first-time customers with special promotions to encourage repeat purchases
- Create time-sensitive offers for low-activity periods (early morning)

### 3. **System Improvements**
- Investigate and fix the Wednesday 2:00 AM data duplication issue
- Implement better validation for large orders (>64 items)

### 4. **Customer Retention**
- Develop loyalty programs for users who reorder within 7-30 days
- Send reminder notifications based on individual purchase frequency patterns

pandas==1.5.3
matplotlib==3.7.0
jupyter==1.0.0
numpy==1.24.0

# Datasets (not included in repository)
/datasets/
data/

# Virtual environments
venv/
env/
ENV/
.venv/

# Jupyter files
.ipynb_checkpoints/
*.ipynb_checkpoints

# System files
.DS_Store
Thumbs.db

# Python files
__pycache__/
*.py[cod]
*$py.class
*.so
.Python

# Logs
*.log

# Analysis outputs
output/
results/

# IDE files
.vscode/
.idea/

# OS generated files
ehthumbs.db
Desktop.ini


