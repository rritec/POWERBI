1. Tell me about your self
1. I completed [Btech] in [cse] specilaization and got opprtunity to work as fresher in [abc] company. I got onboard/Induction training on skills SQL and               PowerBI.
2. From last 3 years iam working as a power Bi developer.
3. In current Project iam working in IC role. As part of this role i will be speaking directly with Product Owner and getting user stories in jira board. We are         following 4 standard user stories 1) Requirment Gathering 2) Development 3) Testing 4) Deployment
4. In current Project Iam working with Pobwer BI and SQl are main skills.
5. In Power BI the building blocks which iam working are power Query, Power Pivot, Power View, and Power BI Pro and Premium license

2. **What are the important components of Power BI?**

Important components of Power BI are: 
1. Power BI Desktop
1. Power Query Editor
2. Power Pivot
3. Power View
2. Power BI Service
3. Power BI Mobile
3. **What you know about Data Analysis Expressions (DAX)**

Data Analysis Expressions (DAX) is a library of functions and operators that can be combined to build formulas and expressions in

1. Power BI Desktop
2. Azure Analysis Services
3. SQL Server Analysis Services
4. Power Pivot in Excel data models.

DAX formulas include functions, operators, and values to perform advanced calculations and queries on data in related tables and columns in tabular data models    
4. **Data types of DAX?**
1. Whole Number
2. Decimal Number
3. Boolean
4. Text
5. Date
6. Currency
refer more details [here](https://docs.microsoft.com/en-us/dax/dax-overview#data-types)
5. **Name two types of connectivity modes in Power BI?**
1. Import
2. Direct Query
6. Explain DAX Function Crossfilter
1. [Read it](https://docs.microsoft.com/en-us/dax/crossfilter-function#:~:text=There%20are%20two%20ways%20to,work%20for%20just%20this%20measure.)
7. How to keep images in Slicer? and filter visulizations based on image selection?
8. How to show negative Values in pie chart?
9. What is HASONEVALUE DAX formula ? Develop Some report?
1. https://docs.microsoft.com/en-us/dax/hasonevalue-function-dax
10. How to use **selectedvalue**
1. https://docs.microsoft.com/en-us/dax/selectedvalue-function
11. what is ALL dax formula?
12. How to use particulat direction in one mesure calculation?
13. How to implement RLS?
14. How to use Mesure in slicer?

15. How to pass multiple values of disconnected table to visulization?

16. Difference between sum vs sumx in dax.

1. https://radacad.com/sum-vs-sumx-what-is-the-difference-of-the-two-dax-functions-in-power-bi

17. common table expression in sql server example
18. Create table from view in sql server?

19. What is query folding in power bi
1. https://docs.microsoft.com/en-us/power-query/power-query-folding
20. How to add images ?
1. https://www.blue-granite.com/blog/simple-steps-to-embed-images-in-power-bi
21. Count Vs CountA 
22. Rolling Months
1. https://stackoverflow.com/questions/49146565/show-last-3-months-from-selected-month-in-power-bi
2. https://www.youtube.com/watch?v=duMSovyosXE

23. Number of unique rows – by multiple columns
1. https://exceltown.com/en/tutorials/power-bi/powerbi-com-and-power-bi-desktop/dax-query-language-for-power-bi-and-power-pivot/number-of-unique-rows-by-multiple-columns/

24. Can you  do sub totals in table visulization?
1. https://docs.microsoft.com/en-us/power-bi/visuals/desktop-matrix-visual#subtotals-and-grand-totals-with-matrix-visuals

25. What is stepped-layout-with-matrix-visuals
1. https://docs.microsoft.com/en-us/power-bi/visuals/desktop-matrix-visual#stepped-layout-with-matrix-visuals

26. How Many Built-in Joins available in Power BI?


1. Inner Join 
2. Left Outer Join
3. Right Outer Join
4. Full Outer Join
5. Left Anti Join
6. Right Anti Join


27. See all these 

1. https://data-flair.training/blogs/power-bi-interview-questions/
2. https://data-flair.training/blogs/power-bi-interview-questions-and-answers/

28. Think and develop below reports.
![image](https://user-images.githubusercontent.com/20516321/115226802-44837c00-a12d-11eb-94d3-b1ced898ddf1.png)
![image](https://user-images.githubusercontent.com/20516321/115226863-57964c00-a12d-11eb-8d66-f248102aa75a.png)



29. Think and develop below reports.
![image](https://user-images.githubusercontent.com/20516321/115226962-785ea180-a12d-11eb-991c-623b1c43dccd.png)
![image](https://user-images.githubusercontent.com/20516321/115227020-8ca29e80-a12d-11eb-83e2-ca85877e5bca.png)


30. Do you know Power BI Rest API?
31. Do you know power Shell commands of Power BI?
- https://docs.microsoft.com/en-us/powershell/power-bi/overview?view=powerbi-ps
- Right click on  Windows power shell ISE > Run as Administartor 
- Install all below moduls
```
Install-Module -Name MicrosoftPowerBIMgmt
Install-Module -Name MicrosoftPowerBIMgmt.Admin
Install-Module -Name MicrosoftPowerBIMgmt.Capacities
Install-Module -Name MicrosoftPowerBIMgmt.Data
Install-Module -Name MicrosoftPowerBIMgmt.Profile
Install-Module -Name MicrosoftPowerBIMgmt.Reports
Install-Module -Name MicrosoftPowerBIMgmt.Workspaces
```
- In Power Shell > Click on **New Script** > copy paste below code and change path accordingly.
```
Connect-PowerBIServiceAccount
Get-PowerBIWorkspace | Export-Csv -Path C:\work\powerbi-powershell\ws.csv
Disconnect-PowerBIServiceAccount
```
Click on Run > observe Csv file output
32. Project Methodology (Agil)
33. Errors rectifing (debugging)
34. What is the definition of L1, L2, L3, L4 support levels in IT Operations Management?
- https://myfirstsite99.wordpress.com/what-is-the-definition-of-l1-l2-l3-l4-support-levels-in-it-operations-management/

35. Write Sql Query to get running totals.
```sql
select empno,sal,
sum(sal)over (order by empno) 
from emp
order by empno
```
36. Difference between summarize and summarizecolumns
* https://www.sqlbi.com/articles/introducing-summarizecolumns/#:~:text=Another%20difference%20between%20SUMMARIZE%20and,only%20and%20no%20row%20context.

37. Explain about data alerts ?
https://docs.microsoft.com/en-us/power-bi/create-reports/service-set-data-alerts

38. How many types of gateways are available in power BI?

1. Personal Gateway
2. Enterprise gateway

39. When we need to gateway?

1. For on permise data sources(for example Oracle,Sql Server ,MySql,Excel, Notepad ...etc)

40. What are the ticketing tools available ?

1. Ivanti
2. Zendesk
3. Freshservice ....etc

41. What is GetData in PowerBI ?
1. GetData is a simple icon on PowerBI used to import data from the source.

42. List out some drawbacks/limitations of using PowerBI ?

1. PowerBi Doesn't accepts file sizes larger than 1GB and doesn't mix imported data accessed from real-time connections.
2. There are very few data soures that allow real-time connections to PowerBi reports and dashboards.
3. it only shares dashboards and reports with users logged in with the same email address.
4. Dashboard doesn't accept or pass user,account,or other entity parameters.

43. Name some commonly used tasks in the query editor ?

1. Connect to data
2. Shape and Combine data
3. Group rows
4. Pivot columns 
5. Create custom columns 
6. Query formulas

44. How many types of buildings blocks in power BI ?

There are Five Types of Building Blocks
1. Visualizations
2. Datasets
3. Reports
4. Dashboards
5. Tiles

45. What is Visualizations ?

* Visualization is the visual representation of data in the form of maps, charts, or tables.

46. What is Datasets ?

* Dataset is a collection of data gathered from various sources like SQL Server, Azure, Text, Oracle, XML, JSON, and many more. With the GetData feature in         Power BI, we can easily fetch data from any data source.

47. What is Report ?

* Reports are a structured representation of datasets that consists of multiple pages. Reports help to extract important information and insights from               datasets to take major business decisions.

48. What is Dashboard ?

* A dashboard is a single-page representation of reports made of various datasets. Each element is termed a tile. 

49. What is Tile ?

* Tiles are single-block containing visualizations of a report. Tiles help to differentiate each report 

50. Name any 3 most useful aggregation functions DAX?

DAX has a number of aggregation functions, including the following commonly used functions:
* SUM
* AVERAGE
* MIN
* MAX
* SUMX (and other X functions)

51. Name any 3 most useful text functions in DAX?

The text functions in DAX include the following:
* CONCATENTATE
* REPLACE
* SEARCH
* UPPER
* FIXED

52. What are formats in Power BI ?

1. Power BI Desktop – Power BI Desktop can be downloaded and installed on your PC. You can connect it to the data source, transform the data, and analyze and             visualize it with the help of templates.
2. Power BI Services – Power BI Services is a Service-as-a-platform or a cloud based service.
3. Power BI Mobile App – The Power BI App is available for iOs, Android, and Windows.

53. What is row-level security?

Row-level security limits the data a user can view and has access to, and it relies on filters. 
Users can define the rules and roles in Power BI Desktop and also publish them to Power BI Service to configure row-level security.

54. Define bi-directional cross filtering?

Bidirectional cross-filtering enables them to apply filters on both sides of a table relationship. 
You can apply the filters by propagating the filter context to a second related table on the other side of a table relationship.

55. What is "M language"?

M is a programming language used in Power Query as a functional, case-sensitive language similar to other programming languages and easy to use.

56. What are the major differences between visual-level, page-level, and report-level filters in Power BI?

Visual-level filters are used to filter data within a single visualization. Page-level filters are used to work on an entire page in a report, and 
different pages can have various filters. 
Report-level filters are used to filter all the visualizations and pages in the report.

57. What are KPIs in Power BI?

KPI is abbreviated as Key Performance Indicator. Any professional organization has teams and employees follow the KPI protocols. The organizations set 
up KPIs for all the employees. These KPIs act as their targets. These KPIs are compared to previous performance and analyze the progress.

58. What is the incremental refresh in the context of Power BI?

Incremental refresh is used to refresh the newly added data to avoid truncating and loading data.

59. What are the different joins in Power BI?

1.Horizontal Joins to append data from multiple tables
2.Vertical Joins to merge the data from multiple tables

60. Divide Function Vs Divide Operator
- It's recommended that you use the **DIVIDE function** whenever the denominator is an expression that could return zero or BLANK.
- In the case that the denominator is a **constant value**, we recommend that you use the **divide operator**. In this case, the division is guaranteed to succeed, and your expression will perform better because it will avoid unnecessary testing.
- [Refer document](https://learn.microsoft.com/en-us/dax/best-practices/dax-divide-function-operator)
61. Table 1 has one column and 4 rows with values 1,1,0,null and Table2 has one column with values 1,1,null,null then let me know how many rows we will get in full outer join? left outer join? reight outerjoin?inner join? ca you get full outer join results without using full outer join ?
``` sql


Create Table DATATableA
(
ColumA Varchar(20),
integrationid int,
)


Insert into DATATableA(ColumA,integrationid) Values ('1',1)
Insert into DATATableA(ColumA,integrationid) Values ('1',2)
Insert into DATATableA(ColumA,integrationid) Values ('0',3)
Insert into DATATableA(integrationid) Values (4)


Select * From DATATableA;



Create Table DATATableB
(
ColumB Varchar(20),
integrationid int,
)
Insert into DATATableB(ColumB,integrationid) Values ('1',1)
Insert into DATATableB(ColumB,integrationid) Values ('0',2)
Insert into DATATableB(integrationid) Values (3)
Insert into DATATableB(integrationid) Values (4)


Select * From DATATableB;



Select DATATableA.ColumA,DATATableB.ColumB  from DATATableA
Full OUTER JOIN DATATableB ON DATATableA.ColumA = DATATableB.ColumB;


```

![image](https://github.com/rritec/powerbi/assets/20516321/1bb17dbe-1a73-42f2-ac7f-ebcbf733d9bc)
![image](https://github.com/rritec/powerbi/assets/20516321/8ecc76e6-f14b-457a-b1d9-926696255e26)
![image](https://github.com/rritec/powerbi/assets/20516321/2ba3a4ed-22e0-4bb5-82e2-67ecb316c558)
![image](https://github.com/rritec/powerbi/assets/20516321/5053f064-a965-47b5-ae78-8122e10dcecc)


62. split below data in power query to get two columns
- SAR:98
- IND-560
- RAND_:9854
- AED=78
63. Get domain name from mail ids using SQL and PowerBI
``` Sql
Create Table Domine
(
EmailID Varchar(30)
)

Insert Into Domine(EmailID) Values ('abcgd@Microsoft.com'),
('Tarun@Rightsoftware.com'),
('Ravi Teja @ LtiMindtree.com'),
('Chetan@google.com')

Select * from Domine;

Select EmailID,SUBSTRING(EmailID,CHARINDEX('@',EmailID)+1,LEN(EmailID)-CHARINDEX('@',EmailID)) AS Domine_Name
from Domine;

```

![image](https://github.com/rritec/powerbi/assets/20516321/aaa372a7-4b51-4fbd-8e9e-ff2fb901cc30)


64. write query to get duplicate rows 
``` Sql
Create Table Duplicate
(
Name_Col Varchar(30)
)

Insert Into Duplicate(Name_Col) Values ('Ravi Teja'),
('Ravi Teja'),('Tarun'),('Tarun'),('Chetan'),('SAI'),('Rinku'),('Geetham'),('Rinku'),('SAI'),('Geetham');

Select * from Duplicate;

Select Name_Col,COUNT(*) As count
From Duplicate
Group BY Name_Col
Having Count(*)>1

```
![image](https://github.com/rritec/powerbi/assets/20516321/cf65e319-bef4-4733-afa1-af9892ade202)




65. reverse the ddmmyyyy into yyyymmdd in sql and powerbi.
66. Difference between treat as and filter dax functions ?

- TREATAS and FILTER are both DAX functions used for filtering data, but they serve different purposes and have distinct use cases:
- TREATAS Function:
- Purpose: TREATAS is used to establish a virtual relationship between tables by applying a filter context from one table to another, even when no physical relationship exists between them in the data model.
- Syntax: TREATAS(<table_or_expression_to_use_as_filter_context>, <table_to_filter>)
- Use Case: You would use TREATAS when you want to create a temporary relationship between tables for a specific calculation or analysis. For instance, when you want to filter one table based on values in another table without creating a physical relationship in the data model.
- Example: If you have two tables, Sales and Product, without a direct relationship, you can use TREATAS to filter the Product table based on values from the Sales table.
- FILTER Function:
- Purpose: FILTER is used to create a new table by filtering an existing table based on a specified condition or expression.
- Syntax: FILTER(<table>, <filter_expression>)
- Use Case: You would use FILTER when you want to filter rows within a single table based on specific criteria. This is often used for creating subsets of data within a single table.
- Example: If you have a Sales table and you want to filter it to include only rows where the sales amount is greater than 1000, you would use the FILTER function.
- In summary, the key difference between the two functions is that TREATAS is primarily used to establish temporary relationships between tables, whereas FILTER is used to filter rows within a single table. Your choice between them depends on the specific data modeling or analysis scenario you are working on.

67. Performance tunning in powerbi?

- Performance tuning in Power BI is crucial to ensure that your reports and dashboards load and respond quickly, providing a smooth user experience. Here are some tips for optimizing the performance of your Power BI reports:

68. **Data Model Optimization**:

- **Data Loading**: Limit the data loaded into your Power BI model. Only load the data that is necessary for your analysis.
- **Data Transformation**: Optimize data transformation steps in Power Query to reduce data size.
- **Data Type Selection**: Choose appropriate data types for your columns to reduce memory usage.
- **Remove Unnecessary Columns**: Remove columns you don't need for analysis to reduce data size.
- **Data Compression**: Enable data compression when possible to reduce memory footprint.

2. **Data Modeling**:

- **Star Schema**: Use a star schema for your data model, with a central fact table and dimension tables. This can improve query performance.
- **Relationships**: Define relationships between tables efficiently. Use one-to-many relationships when appropriate.
- **Bi-Directional Filtering**: Use bi-directional filtering with caution, as it can affect performance.

3. **DAX Optimization**:

- **Measure Optimization**: Write efficient DAX measures. Avoid using complex DAX functions that slow down performance.
- **Row-Level Security**: If you use Row-Level Security, make sure it's optimized to avoid excessive data filtering.

4. **Aggregations**:

- Use aggregations to pre-calculate and store summary data for large datasets. This can significantly improve query performance.

5. **Filter Optimization**:

- Minimize the number of visual-level filters. Excessive filters can slow down report performance.
- Use slicers and filters strategically to limit the data loaded.

6. **Visual Design**:

- Use summarization and drill-through features to provide a balance between detail and performance.
- Limit the number of visuals on a single report page.
- Use visuals with caution, especially if they have a large number of data points.

7. **Performance Analyzer**:

- Use Power BI's built-in Performance Analyzer to identify bottlenecks in your report. It helps pinpoint slow-performing visuals or DAX measures.

8. **Data Refresh Schedule**:

- Schedule data refresh during off-peak times to minimize the impact on the Power BI Service's performance.

9. **Power BI Service Considerations**:

- Be mindful of dataset size limitations in the Power BI Service.
- Utilize the Power BI Premium or Premium Per User (PPU) capacities for better performance.

10. **Monitor Usage**:

- Use the Power BI Service's usage metrics and monitoring tools to identify reports that need optimization.

11. **Regular Testing**:

- Continuously test your reports and measures for performance as your data and report complexity grow.

Remember that performance optimization is an ongoing process. Regularly review and optimize your Power BI reports as data and business requirements evolve to ensure that your reports remain responsive and provide a good user experience.

69. What is formula engine and storage engine in DAX?

- https://www.sqlbi.com/articles/formula-engine-and-storage-engine-in-dax/#:~:text=Differences%20between%20the%20formula%20engine,made%20by%20the%20formula%20engine.

70. What is tabular Editor external tool  in context of powerbi
- https://docs.tabulareditor.com/?tabs=TE3
71. What is data lineage in DAX ?
- https://www.sqlbi.com/articles/understanding-data-lineage-in-dax/    
73. What is XMLA endpoint?
- https://learn.microsoft.com/en-us/power-bi/enterprise/service-premium-connect-tools
74. context transition in DAX?
- https://www.sqlbi.com/articles/understanding-context-transition-in-dax/
75. What is SQL Server Profiler?
- https://learn.microsoft.com/en-us/sql/tools/sql-server-profiler/sql-server-profiler?view=sql-server-ver16
76. What is CTE and WITH?
- https://www.metabase.com/learn/sql-questions/sql-cte#cte-example
77. What are the windows functions in SQL?
- https://mode.com/sql-tutorial/sql-window-functions

# Part 2

1. Explain about field parameters and calculation groups
    - https://www.sqlbi.com/articles/using-field-parameters-and-calculation-groups-for-conditional-formatting/
2. What is data manipulation techniques ?
Data Manipulation Techniques

Data manipulation is the process of transforming, cleaning, reorganizing, and restructuring raw data into a more usable and meaningful format. It's a crucial step in 
data analysis, as it prepares the data for further analysis, reporting, or visualization.
Key Data Manipulation Techniques
Data Cleaning:
Handling Missing Values:
Deletion: Removing rows or columns with missing values.
Imputation: Filling missing values with estimated values (mean, median, mode, or predictive models).
Outlier Detection and Treatment:
Identifying anomalies using statistical methods (e.g., Z-score, IQR).
Handling outliers: Removing, capping, or winsorizing.
Data Formatting and Standardization:
Ensuring consistency in data formats (e.g., date, currency).
Standardizing units of measurement.
Data Transformation:

Aggregation: Combining multiple data points into a single summary value (e.g., sum, average, count).
Normalization: Scaling numerical values to a common range (e.g., min-max scaling, Z-score normalization).
Discretization: Converting continuous numerical data into discrete categories (e.g., binning).
Feature Engineering: Creating new features from existing ones (e.g., combining variables, calculating ratios).
Data Integration:

Joining Data Sources: Combining data from multiple sources based on common keys (e.g., inner join, outer join).
Merging Data: Appending data from different sources into a single dataset.
Data Reshaping:
Pivoting: Restructuring data by converting rows into columns or vice versa.
Melting: Unpivoting data by converting columns into rows.
Tools for Data Manipulation

Programming Languages: Python (Pandas, NumPy), R
SQL: For database operations and data extraction.
Spreadsheets: Excel, Google Sheets
Data Analysis Tools: Tableau, Power BI, SPSS
Example Use Cases

E-commerce: Analyzing customer purchase history to identify trends and make personalized recommendations.
Healthcare: Identifying disease patterns and optimizing treatment plans.
Finance: Predicting stock market trends and managing risk.
Marketing: Analyzing customer behavior to target specific segments.
By mastering these techniques, data analysts and scientists can unlock valuable insights from complex datasets, enabling data-driven decision-making.
3. Aggregated functions
-https://learn.microsoft.com/en-us/dax/aggregation-functions-dax
4. Rank and Dense Rank in DAX
-https://learn.microsoft.com/en-us/dax/rank-function-dax
























