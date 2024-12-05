1. **what is data manipulation techniques**
- Data Manipulation Techniques
- Data manipulation is the process of transforming, cleaning, reorganizing, and restructuring raw data into a more usable and meaningful format. It's a crucial step in data analysis, as it prepares the data for further analysis, reporting, or visualization.
- Key Data Manipulation Techniques
- Data Cleaning:
    - Handling Missing Values:
    - Deletion: Removing rows or columns with missing values.
    - Imputation: Filling missing values with estimated values (mean, median, mode, or predictive models).
    - Outlier Detection and Treatment:
    - Identifying anomalies using statistical methods (e.g., Z-score, IQR).
    - Handling outliers: Removing, capping, or winsorizing.
    - Data Formatting and Standardization:
    - Ensuring consistency in data formats (e.g., date, currency).
    - Standardizing units of measurement.
- Data Transformation:
    - Aggregation: Combining multiple data points into a single summary value (e.g., sum, average, count).
    - Normalization: Scaling numerical values to a common range (e.g., min-max scaling, Z-score normalization).
    - Discretization: Converting continuous numerical data into discrete categories (e.g., binning).
    - Feature Engineering: Creating new features from existing ones (e.g., combining variables, calculating ratios).
- Data Integration:
    - Joining Data Sources: Combining data from multiple sources based on common keys (e.g., inner join, outer join).
    - Merging Data: Appending data from different sources into a single dataset.
- Data Reshaping:
    - Pivoting: Restructuring data by converting rows into columns or vice versa.
    - Melting: Unpivoting data by converting columns into rows.
- Tools for Data Manipulation
    - Programming Languages: Python (Pandas, NumPy), R
    - SQL: For database operations and data extraction.
    - Spreadsheets: Excel, Google Sheets
    - Data Analysis Tools: Tableau, Power BI, SPSS

- Example Use Cases
    - E-commerce: Analyzing customer purchase history to identify trends and make personalized recommendations.
    - Healthcare: Identifying disease patterns and optimizing treatment plans.
    - Finance: Predicting stock market trends and managing risk.
    - Marketing: Analyzing customer behavior to target specific segments.
    - By mastering these techniques, data analysts and scientists can unlock valuable insights from complex datasets, enabling data-driven decision-making.

2. Aggregated Functions with examples?
    - https://learn.microsoft.com/en-us/dax/aggregation-functions-dax
3. what is **RANK**,**DENSERANK**,**ROWNUMBER** and their difference?
    - **RANK**, **DENSE_RANK**, and **ROW_NUMBER** are functions commonly used in analytical queries for ranking or assigning a unique order to rows. They are most widely recognized in SQL but are also implemented conceptually in other tools like DAX. Here's an explanation of each and their key differences:

    - **1. RANK**
    - **RANK** assigns a rank to each row in a result set based on the order of a specified column or expression. It accounts for ties by assigning the same rank to equal values but skips ranks after ties.

      #### Example
      | Row | Value | RANK (Descending) |
      |-----|-------|-------------------|
      | 1   | 100   | 1                 |
      | 2   | 90    | 2                 |
      | 3   | 90    | 2                 |
      | 4   | 80    | 4                 |

    - **Ties**: Rows with the same value get the same rank.
    - **Skipping**: The next rank skips numbers equal to the number of ties.

      **2. DENSE_RANK**
    - **DENSE_RANK** is similar to **RANK**, but it does not skip ranks after ties. It assigns consecutive ranks even when there are ties.
      #### Example
      | Row | Value | DENSE_RANK (Descending) |
      |-----|-------|-------------------------|
      | 1   | 100   | 1                       |
      | 2   | 90    | 2                       |
      | 3   | 90    | 2                       |
      | 4   | 80    | 3                       |

    - **Ties**: Rows with the same value get the same rank.
    - **No Skipping**: The next rank is consecutive, regardless of the number of ties.
     ### **3. ROW_NUMBER**
     **ROW_NUMBER** assigns a unique number to each row based on the specified order. It does not consider ties, meaning no two rows can have the same number.
     #### Example
     | Row | Value | ROW_NUMBER (Descending) |
     |-----|-------|--------------------------|
     | 1   | 100   | 1                        |
     | 2   | 90    | 2                        |
     | 3   | 90    | 3                        |
     | 4   | 80    | 4                        |

    - **No Ties**: Each row has a unique number, even if the values are the same.
    - **Sequential**: The numbers are always sequential.
    ### **Key Differences**
     | **Aspect**       | **RANK**                   | **DENSE_RANK**             | **ROW_NUMBER**             |
     |-------------------|----------------------------|----------------------------|----------------------------|
     | **Ties Handling** | Same rank for ties         | Same rank for ties         | No ties; unique number per row |
     | **Skipping**      | Skips ranks after ties     | No skipping                | No skipping                |
     | **Uniqueness**    | Not unique if ties exist   | Not unique if ties exist   | Always unique             |
     | **Use Case**      | When relative positioning matters, and gaps are acceptable | When relative positioning matters, and no gaps are allowed | When each row needs a 
       unique position |
    ### **Real-World Use Cases**
     1. **RANK**
      - Used when you need to rank items (e.g., sales by salesperson) but don't need consecutive numbering.
      - Example: Assigning ranks in a competition where the same score gets the same rank.

    2. **DENSE_RANK**
     - Used when consecutive ranking is important, even with ties.
     - Example: Ranking categories by revenue without skipping numbers.

    3. **ROW_NUMBER**
     - Used when you need a unique identifier for each row, irrespective of value.
     - Example: Paginating results in a query or assigning a unique sequence to records.
    ### **In SQL**
    #### Syntax for RANK, DENSE_RANK, and ROW_NUMBER:
    ```sql
    SELECT 
        Value, 
        RANK() OVER (ORDER BY Value DESC) AS Rank,
        DENSE_RANK() OVER (ORDER BY Value DESC) AS DenseRank,
        ROW_NUMBER() OVER (ORDER BY Value DESC) AS RowNumber
     FROM TableName;
  ### **In DAX**
   - **RANK** and **DENSE_RANK** can be implemented using the `RANKX` function.
   - **ROW_NUMBER** requires a combination of `RANKX` or advanced measures.
     Example in DAX for Ranking:
  ```dax
     Rank = RANKX(ALL('Table'), 'Table'[Value], , DESC)
     Dense Rank = RANKX(SUMMARIZE('Table', 'Table'[Value]), 'Table'[Value], , DESC)
     Row Number = RANKX(ALL('Table'), 'Table'[ID], , ASC)
By understanding these concepts, you can select the most appropriate ranking method based on your analytical or reporting requirements.
4. f
5. f
6. f
7. f
8. f
9. f
10. f
11. f
   

   

   

