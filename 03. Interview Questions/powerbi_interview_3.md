
# 🔁 LOOKUPVALUE DAX Function in Power BI – Complete Guide with Example

This guide explains how to use the `LOOKUPVALUE` DAX function in Power BI to fetch related values from another table — similar to a SQL JOIN or Excel VLOOKUP — using a practical example with EMP and DEPT tables.

---

## 📌 Objective

Use the `LOOKUPVALUE` function to retrieve the **Department Name (DNAME)** from the `DEPT` table and show it in the `EMP` table using the common key column: `DEPTNO`.

---

## 🪜 Step-by-Step Guide

### ✅ Step 1: Import Tables into Power BI

Import the following two tables into Power BI Desktop:

1. **EMP Table**
   - Columns: `EMPNO`, `ENAME`, `JOB`, `MGR`, `SAL`, `COMM`, `DEPTNO`, etc.

2. **DEPT Table**
   - Columns: `DEPTNO`, `DNAME`

You can import these from Excel, SQL, or enter manually using "Enter Data" option in Power BI.

---

### ✅ Step 2: Understand the Tables and Goal

The `EMP` table contains employee records including the `DEPTNO` (Department Number).  
The `DEPT` table contains department names (`DNAME`) mapped to each `DEPTNO`.

**Goal**: Add a new column in `EMP` that shows the `DNAME` from the `DEPT` table based on matching `DEPTNO`.

---

### ✅ Step 3: Use the LOOKUPVALUE DAX Function

Create a **new column** in the `EMP` table with the following DAX formula:

```DAX
lookupvalue_dname = 
LOOKUPVALUE (
    DEPT[DNAME],        // Column to return (result column)
    DEPT[DEPTNO],       // Column to search in (search column)
    EMP[DEPTNO]         // Value to match (search value)
)
```

This function will return the corresponding department name from the DEPT table into the EMP table.

---

### 🔍 Explanation of Parameters

| Parameter        | Description                                           |
|------------------|-------------------------------------------------------|
| `DEPT[DNAME]`    | Column to return (Department Name)                   |
| `DEPT[DEPTNO]`   | Column in DEPT table to match                        |
| `EMP[DEPTNO]`    | Value in EMP table used for matching                 |

This is equivalent to:  
**"Get the DNAME from DEPT where DEPTNO in DEPT = DEPTNO in EMP."**

---

### ✅ Step 4: Result Example

| EMPNO | ENAME  | JOB       | DEPTNO | lookupvalue_dname |
|-------|--------|-----------|--------|--------------------|
| 7499  | ALLEN  | SALESMAN  | 30     | SALES              |
| 7934  | MILLER | CLERK     | 10     | ACCOUNTING         |
| 7788  | SCOTT  | ANALYST   | 20     | RESEARCH           |

Each employee now has their respective department name next to them.

---

## 🎯 Why Use `LOOKUPVALUE`?

| Feature           | Description                                                    |
|-------------------|----------------------------------------------------------------|
| 🔗 Join-like logic | Retrieves a value from another table based on match condition |
| 🚫 No relation     | Works without model relationships                             |
| 🔄 Dynamic         | Reacts to filters and slicers                                 |
| 🔐 Flexible        | Can be used with composite keys (multiple search conditions)  |

---

## 📝 When to Use `LOOKUPVALUE`

- You want to bring values from another table without creating relationships.
- Creating calculated columns where matching is required.
- Need a custom mapping or lookup logic inside your DAX formula.
- `RELATED()` is not applicable due to missing relationship.

---

## 🚨 Notes and Caveats

- If **multiple rows match**, it returns an error.
- If **no row matches**, it returns blank.
- Use `RELATED()` instead of `LOOKUPVALUE` if a relationship already exists for better performance.

---

## ✅ Summary

| Topic              | Description                                         |
|--------------------|-----------------------------------------------------|
| Function           | `LOOKUPVALUE`                                       |
| Use Case           | Fetch column value from another table using a match |
| Syntax             | `LOOKUPVALUE(Result_Column, Search_Column, Search_Value)` |
| Example Result     | Department Name displayed in EMP table              |
| Works Without Join | ✅                                                  |

---

## 📚 Bonus Tip

If you want to lookup based on **two columns** (composite key), you can do:

```DAX
LOOKUPVALUE (
    Table1[Return_Column],
    Table1[Key1], Table2[Key1],
    Table1[Key2], Table2[Key2]
)
```

This is useful when no single column uniquely identifies rows in the lookup table.

---

> ℹ️ This guide is great for beginners learning how to use `LOOKUPVALUE` in real-world scenarios without needing relationships in Power BI's data model.
