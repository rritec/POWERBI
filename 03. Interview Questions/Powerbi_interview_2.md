1. What is the difference between SUMMARIZE
- SUMMARIZE:
    - Creates a summary of the input table grouped by the specified columns.
    - Syntax: SUMMARIZE ( <Table> [, <GroupBy_ColumnName> [, [<Name>] [, [<Expression>] [, <GroupBy_ColumnName> [, [<Name>] [, [<Expression>] [, … ] ] ] ] ] ] ] )
    - Example:
      ``` dax
      SUMMARIZE(
	'Sales',
	'Product'[Category],	
	"Total Amount",sum(Sales[Sales Amount]))
```


2. 
