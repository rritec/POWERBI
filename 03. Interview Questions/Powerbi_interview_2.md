1. What is the difference between SUMMARIZE
- SUMMARIZE:
    - Creates a summary of the input table grouped by the specified columns.
    - Syntax: ```SUMMARIZE ( <Table> [, <GroupBy_ColumnName> [, [<Name>] [, [<Expression>] [, <GroupBy_ColumnName> [, [<Name>] [, [<Expression>] [, … ] ] ] ] ] ] ] )```
    - Example:
      ``` dax
      SUMMARIZE(
      'Sales',
      'Product'[Category],
      "Total Amount",sum(Sales[Sales Amount])
      )
      ```
- SUMMARIZECOLUMNS:
    - Create a summary table for the requested totals over set of groups
    - Syntax: ```SUMMARIZECOLUMNS ( [<GroupBy_ColumnName> [, [<FilterTable>] [, [<Name>] [, [<Expression>] [, <GroupBy_ColumnName> [, [<FilterTable>] [, [<Name>] [, [<Expression>] [, … ] ] ] ] ] ] ] ] ] )```
    - Example:
    ``` dax
--  SUMMARIZECOLUMNS is the primary querying function in DAX
--  It provides most querying features in a single function:
--      First set of arguments are the groupby columns
--      Second set are the filters
--      Third set are additional columns added to the resultset
EVALUATE
SUMMARIZECOLUMNS (
    'Product'[Brand],
    'Date'[Calendar Year],
    TREATAS ( { "CY 2008", "CY 2009" }, 'Date'[Calendar Year] ),
    TREATAS ( { "Red", "Blue" }, 'Product'[Color] ),
    "Amount", [Sales Amount],
    "Qty", SUM ( Sales[Quantity] )
)
    ```


2. 
