
# Power Pivot

## Data Analysis eXpressions (DAX):
1. Data Analysis eXpressions (DAX) is a library of functions and operators that can be combined to build formulas and expressions in 
    - Power BI Desktop
    - Azure Analysis Services
    - SQL Server Analysis Services
    - Power Pivot in Excel data models.
1. Refer below MSFT Materials
    - [Help Document](https://docs.microsoft.com/en-us/dax/)
    - [Guided Learning Path](https://docs.microsoft.com/en-us/learn/paths/dax-power-bi/)

## DAX Functions mainily catagorized as below

    - Aggregation functions
    - Date and time functions
    - Filter functions
    - Financial functions 
    - Information functions
    - Logical functions
    - Math and Trig functions
    - Other functions
    - Parent and Child functions
    - Relationship functions
    - Statistical functions
    - Table manipulation functions
    - Text functions
    - Time intelligence functions

## Exercise 1: Learn Calendar function

1. Open PBI Desktop
1. In left side Navigation bar > Click on **Data**
1. Click on New Table
1. Provide DAX formula as **dt_table = CALENDAR (DATE (2019, 1, 1), DATE (2020, 12, 31))**
1. Create **new column** to extract **year**
2. Create **new column** to extract **month**
3. Create **new column** to extract **weeknumber**
4. Create **new column** to extract **day**
5. Create **new column** to extract **dayname**
    - **Hint:** Use Format Dax function [Refer help document](https://docs.microsoft.com/en-us/dax/format-function-dax#custom-datetime-formats)
7. Create **new column** to extract **end_of_the_month**
8. Create **new column** to extract **hour**
9. Create **new column** to extract **minute**
10. Create **new column** to extract **Second**

## Exercise 2: How many years survived by Mahatma Gandhi?

- We know Gandhi Born on October 2, 1869, and Died on January 30, 1948
- Read help document and find out no of years survived by Gandhi

    https://docs.microsoft.com/en-us/dax/datediff-function-dax
 - Process:
    - In Fields pane > Click on dt_table ... > click on new mesure > type the formula **Number of years survived = datediff(date(1869,10,02),date(1948,01,30))** > click on validate > drag this column into table and observe the output.

## Exercise 3: Using Variables to improve performance
- Any calculation, we are using twice or more better to store the calculation result in variable and use the variable where ever needed.
- Open [Adventure Works DW 2020 M02](https://github.com/rritec/POWERBI/blob/master/02.%20Labdata/Adventure%20Works%20DW%202020%20M02.pbix) file
- Observe Calculation inside **Sales** table **Revenue YoY %**
- The last year sales, calculating two times right .
- Develop one mesure with the name of **Revenue YOY % using Var** with below formula

    ```
    Revenue YoY %_var =     
    VAR LySales = CALCULATE([Revenue],SAMEPERIODLASTYEAR('Date'[Date]))
    RETURN
    if(HASONEVALUE('Date'[Fiscal Year]),DIVIDE([Revenue]-LySales,LySales))
    ```
- Develop report as shown below
    - ![image](https://user-images.githubusercontent.com/20516321/147716190-3778224e-e457-4198-ae42-7a6d1fd08f7c.png)


## Exercise 4: Duplicate Table
- In Which scenario duplication of table is needed?
    - Role Playing Dimension
- Open [Adventure Works DW 2020 M03](https://github.com/rritec/powerbi/raw/master/Labdata/Adventure%20Works%20DW%202020%20M03.pbix)
- In the Data view > Click on New Table > type below formula 

    ```
    Ship Date = 'Date'
    ```
- To complete the design of the Ship Date table, you can:
    - Rename the following columns:
        - **Date** as **Ship Date**
        - **Fiscal Year** as **Ship Fiscal Year**
        - **Fiscal Quarter** as **Ship Fiscal Quarter**
        - **Month** as **Ship Month**
        - **Full Date** as **Ship Full Date**
    - Sort the **Ship Full Date** column by the **Ship Date** column.
    - Sort the **Ship Month** column by the **MonthKey** column.
    - Hide the **MonthKey** column.
    - Create a hierarchy named Fiscal with the following levels:
        - Ship Fiscal Year
        - Ship Fiscal Quarter
        - Ship Month
        - Ship Full Date
    - Mark the **Ship Date** table as a date table by using the Ship Date column.

## Exercise 5: Can you populate dates of india financial year
- The financial year of India begins from April 1 of a calendar year and ends on March 31 of the next calendar year
- https://en.wikipedia.org/wiki/Fiscal_year
- In above PBIX file, develop a table report to understand range of dates

  ![image](https://user-images.githubusercontent.com/20516321/111573915-72de0680-87d1-11eb-8895-158a5d895da2.png)

- In the Data view > Click on New Table > type below formula 

    ```
    India Fin Dates =  CALENDARAUTO(3)
    ```
 - Using **India Fin Dates** Table **Date** Column  develop below report and understand how the Calendar Auto working.

   ![image](https://user-images.githubusercontent.com/20516321/111574107-d831f780-87d1-11eb-83ca-9b1254d9e1ff.png)

 - Read the [doc](https://docs.microsoft.com/en-us/dax/calendarauto-function-dax)



## Questions
1. About USERNAME() and USERPRINCIPALNAME()?
    - https://docs.microsoft.com/en-us/dax/username-function-dax
    - https://docs.microsoft.com/en-us/dax/userprincipalname-function-dax
    - In PowerBI Desktop
        - ![image](https://user-images.githubusercontent.com/20516321/109728973-34dfc080-7bdd-11eb-8dbb-ad4fd8316da4.png)
    - In Power BI Service
        - ![image](https://user-images.githubusercontent.com/20516321/109729142-740e1180-7bdd-11eb-9ec5-25db46bfd2cf.png)
        
 1. What is User Principal Name?
    - User Principal Name (UPN) is the name of a system user in an email address format.
    - A UPN (for example: john.doe@domain.com) consists of the user name (login name), separator (the @ symbol), and domain name (UPN suffix)
  
1. What is Implicity Measure.
    - Implicit measures are automatic behaviours that allow visuals to summarize model column data. 
1. What is Explicity Measure.
    - Explicit measures, also known simply as measures, are calculations that you can add to your model.
1. What is compound Measure.
    - When a measure references one or more measures, it's known as a compound measure.
    - Example ``` Profit = [Revenue] - [Cost] ```

1. Calculated columns Vs measures

    - DAX beginners often experience a degree of confusion about calculated columns and measures. The following section reviews the similarities and differences between both.
        - Regarding similarities between calculated columns and measures, both are:
            - Calculations that you can add to your data model.
            - Defined by using a DAX formula.
            - Referenced in DAX formulas by enclosing their names within square brackets.
        - The areas where calculated columns and measures differ include:
            - **Purpose** - Calculated columns extend a table with a new column, while measures define how to summarize model data.
            - **Evaluation** - Calculated columns are evaluated by using row context at data refresh time, while measures are evaluated by using filter context at query time. Filter context is introduced in a later module; it's an important topic to understand and master so that you can achieve sophisticated summarizations.
            - **Storage** - Calculated columns (in Import storage mode tables) store a value for each row in the table, but a measure never stores values in the model.
            - **Visual use** - Calculated columns (like any column) can be used to filter, group, or summarize (as an implicit measure), whereas measures are designed to summarize.
# Interview Questions 
1. Based on return type, DAX functions are divided into how many types ?
    - Two Types
          - Table Return(Calender,all,filter..etc)
          - Scalar Return(Date,year,month,hour...etc)    - 
2. Any calculated column first priority goes to M-language ?
    - True
3. 


 



