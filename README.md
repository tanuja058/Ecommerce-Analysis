# E-commerce Data Analysis using Python

## Project Overview

This project explores e-commerce customer, product, and sales data using
Python in Jupyter Notebook. The goal is to understand sales performance,
product demand, customer spending patterns, payment preferences, and
order fulfilment through exploratory data analysis (EDA) and
visualizations.

## Dataset

The notebook works with three CSV files:

  ---------------------------------------------------------------------------
  File                              Rows              Columns Description
  ----------------- -------------------- -------------------- ---------------
  `customers.csv`                 40,000                   15 Customer
                                                              details, age
                                                              groups,
                                                              customer tiers,
                                                              order counts,
                                                              and spending

  `products.csv`                   2,000                   12 Product
                                                              details,
                                                              categories,
                                                              brands, prices,
                                                              discounts,
                                                              stock, and
                                                              ratings

  `sales.csv`                    250,000                   21 Order dates,
                                                              products,
                                                              quantities,
                                                              amounts,
                                                              payment modes,
                                                              order statuses,
                                                              and ratings
  ---------------------------------------------------------------------------

> The CSV files are expected separately from the notebook. Update the
> `DATA_PATH` variable in the notebook to match the folder where you
> store the files.

## Tools and Libraries

-   Python
-   Jupyter Notebook
-   Pandas --- data loading, cleaning, merging, and analysis
-   NumPy --- numerical operations
-   Matplotlib --- charts and plots
-   Seaborn --- statistical visualizations
-   Plotly, SciPy, and scikit-learn are imported in the notebook,
    although the main analysis documented here focuses on exploratory
    data analysis.

## Project Workflow

1.  Load the customer, product, and sales datasets.
2.  Inspect dataset dimensions, column data types, and descriptive
    statistics.
3.  Check missing values and duplicate rows.
4.  Standardize text fields by trimming leading and trailing whitespace.
5.  Explore order statuses and payment methods.
6.  Combine sales with product and customer data for additional
    analysis.
7.  Analyze top-selling products, category sales, top customers, and
    monthly sales.
8.  Visualize the results and summarize business insights with
    recommendations.

## Analysis and Visualizations

The notebook includes: - Order status distribution, including a pie
chart - Top 10 products by quantity sold - Monthly sales trend -
Correlation heatmap for numeric sales fields - Total amount by customer
tier - Order value by payment method - Distribution of order amounts -
Average recorded rating by product category

## Key Findings

The following findings are based on the outputs recorded in the
notebook:

-   **Most frequently sold product:** `boAt Headphones V6`, with **3,473
    units** sold.
-   **Highest recorded sales category:** **Electronics**, with a total
    `Total_Amount` of approximately **4.31 billion** in the dataset's
    recorded currency units.
-   **Most common payment method:** **UPI**, appearing in **128,474**
    sales records.
-   **Highest-sales month:** **March 2026**, with a recorded total
    amount of approximately **248.03 million**.
-   **Order status distribution:**
    -   Delivered: **80.06%**
    -   Cancelled: **5.00%**
    -   Returned: **5.00%**
    -   Shipped: **4.98%**
    -   Processing: **4.96%**

These results are descriptive findings from the current notebook output
and should be rechecked if the data changes.

## Business Recommendations

-   Monitor stock levels for products with high sales volume.
-   Review the Electronics category to understand which products and
    brands contribute most to sales.
-   Keep UPI payments convenient because UPI is the most frequently
    recorded payment method.
-   Use monthly sales patterns to support inventory and promotional
    planning.
-   Investigate cancelled, returned, shipped, and processing orders to
    identify possible fulfilment improvements.
-   Review customer-tier spending and product-category ratings to
    identify opportunities for better customer experience.

## How to Run the Project

1.  Download or clone this repository.

2.  Install the required libraries:

    ``` bash
    pip install pandas numpy matplotlib seaborn plotly scipy scikit-learn jupyter
    ```

3.  Keep `customers.csv`, `products.csv`, and `sales.csv` in one folder.

4.  Open `Ecommerce Analysis.ipynb` in Jupyter Notebook.

5.  Update `DATA_PATH` to the folder containing the CSV files. For
    example:

    ``` python
    from pathlib import Path

    DATA_PATH = Path("path/to/ecommerce_data")

    customers = pd.read_csv(DATA_PATH / "customers.csv")
    products = pd.read_csv(DATA_PATH / "products.csv")
    sales = pd.read_csv(DATA_PATH / "sales.csv")
    ```

6.  Run the notebook cells from top to bottom.

## Project Structure

``` text
Ecommerce-Data-Analysis/
├── Ecommerce Analysis.ipynb
├── README.md
└── ecommerce_data/
    ├── customers.csv
    ├── products.csv
    └── sales.csv
```

The `ecommerce_data/` folder is an example structure; the CSV files may
be stored elsewhere as long as `DATA_PATH` is updated.

## Skills Demonstrated

-   Data loading and inspection
-   Data quality checks
-   Basic data cleaning
-   DataFrame merging and grouping
-   Descriptive statistics
-   Exploratory data analysis (EDA)
-   Data visualization
-   Communicating findings and business recommendations

## Conclusion

This project demonstrates an intermediate, beginner-friendly Python EDA
workflow using customer, product, and sales datasets. It turns raw
records into understandable summaries and visualizations that can
support basic e-commerce business decisions.
