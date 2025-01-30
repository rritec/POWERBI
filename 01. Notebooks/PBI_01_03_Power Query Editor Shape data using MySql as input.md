
# Working with MySql

![image](https://user-images.githubusercontent.com/20516321/196849404-a9371f5d-6a66-4d5c-9285-75e3131c8332.png)


1. MySql is a oracle product
1. Install **MySql** software by following [this link](https://github.com/rritec/POWERBI/blob/master/01.%20Notebooks/PBI_01_01_Introduction_Installation.md#mysql-installationoptional)
1. Open **MySql Workbench** > if required create **new connection** or use **existing connection** > Click on **New SQL Tab for execution of queries**
1. In **Navigator** Window in empty space > Right Click > click on **Create Schema** > Provide schema name as **rritecdb** > click on **apply** > click on **apply** > Click on **Finish**

**or**

run below script 

``` sql
CREATE SCHEMA rritecDB;
```
``` sql
USE rritecdb;
```

## Load Data
``` sql
drop table if exists emp;

drop table if exists dept;

drop table if exists salgrade;

drop table if exists emp10;

drop table if exists emp20;

drop table if exists emp30;
```

``` sql
CREATE TABLE `emp` (
  `empno` decimal(4,0) NOT NULL,
  `ename` varchar(10) DEFAULT NULL,
  `job` varchar(9) DEFAULT NULL,
  `mgr` decimal(4,0) DEFAULT NULL,
  `hiredate` date DEFAULT NULL,
  `sal` decimal(7,2) DEFAULT NULL,
  `comm` decimal(7,2) DEFAULT NULL,
  `deptno` decimal(2,0) DEFAULT NULL,
  `test` varchar(100) DEFAULT NULL
) ;


INSERT INTO emp (empno,ename,job,mgr,hiredate,sal,comm,deptno,test) VALUES 
(7369,'SMITH','CLERK',7902,'1980-12-17',800.00,NULL,20,'1')
,(7499,'ALLEN','SALESMAN',7698,'1981-02-20',1600.00,300.00,30,'1')
,(7521,'WARD','SALESMAN',7698,'1981-02-22',1250.00,500.00,30,'1')
,(7566,'JONES','MANAGER',7839,'1981-04-02',2975.00,NULL,20,'1')
,(7654,'MARTIN','SALESMAN',7698,'1981-09-28',1250.00,1400.00,30,'1')
,(7698,'BLAKE','MANAGER',7839,'1981-05-01',2850.00,NULL,30,'1')
,(7782,'CLARK','MANAGER',7839,'1981-06-09',2450.00,NULL,10,'1')
,(7788,'SCOTT','ANALYST',7566,'1982-12-09',3000.00,NULL,20,'1')
,(7839,'KING','PRESIDENT',NULL,'1981-11-17',5000.00,NULL,10,'1')
,(7844,'TURNER','SALESMAN',7698,'1981-09-08',1500.00,0.00,30,'1')
,(7876,'ADAMS','CLERK',7788,'1983-01-12',1100.00,NULL,20,'1')
,(7900,'JAMES','CLERK',7698,'1981-12-03',950.00,NULL,30,'1')
,(7902,'FORD','ANALYST',7566,'1981-12-03',3000.00,NULL,20,'1')
,(7934,'MILLER','CLERK',7782,'1982-01-23',1300.00,NULL,10,'1')
,(1234,'RamReddy','DS',7839,'1981-12-03',2400.00,100.00,50,'1')
;

CREATE TABLE `dept` (
  `deptno` decimal(2,0) DEFAULT NULL,
  `dname` varchar(14) DEFAULT NULL,
  `loc` varchar(13) DEFAULT NULL,
  `test` varchar(100) DEFAULT NULL
) ;

INSERT INTO dept (deptno,dname,loc,test) VALUES 
(10,'ACCOUNTING','NEW YORK','1')
,(20,'RESEARCH','DALLAS','1')
,(30,'SALES','CHICAGO','1')
,(40,'OPERATIONS','BOSTON','1')
;

CREATE TABLE salgrade(
  grade decimal(1),
  losal decimal(4),
  hisal decimal(4)
);

INSERT INTO salgrade VALUES 
(1, 700, 1200)
,(2, 1201, 1400)
,(3, 1401, 2000)
,(4, 2001, 3000)
,(5, 3001, 9999);

CREATE TABLE `emp10` (
  `empno` decimal(4,0) NOT NULL,
  `ename` varchar(10) DEFAULT NULL,
  `job` varchar(9) DEFAULT NULL,
  `mgr` decimal(4,0) DEFAULT NULL,
  `hiredate` date DEFAULT NULL,
  `sal` decimal(7,2) DEFAULT NULL,
  `comm` decimal(7,2) DEFAULT NULL,
  `deptno` decimal(2,0) DEFAULT NULL,
  `test` varchar(100) DEFAULT NULL
) ;


INSERT INTO emp10 (empno,ename,job,mgr,hiredate,sal,comm,deptno,test) VALUES 
(7782,'CLARK','MANAGER',7839,'1981-06-09',2450.00,NULL,10,'1')
,(7839,'KING','PRESIDENT',NULL,'1981-11-17',5000.00,NULL,10,'1')
,(7934,'MILLER','CLERK',7782,'1982-01-23',1300.00,NULL,10,'1')
;

CREATE TABLE `emp20` (
  `empno` decimal(4,0) NOT NULL,
  `ename` varchar(10) DEFAULT NULL,
  `job` varchar(9) DEFAULT NULL,
  `mgr` decimal(4,0) DEFAULT NULL,
  `hiredate` date DEFAULT NULL,
  `sal` decimal(7,2) DEFAULT NULL,
  `comm` decimal(7,2) DEFAULT NULL,
  `deptno` decimal(2,0) DEFAULT NULL,
  `test` varchar(100) DEFAULT NULL
) ;


INSERT INTO emp20 (empno,ename,job,mgr,hiredate,sal,comm,deptno,test) VALUES 
(7369,'SMITH','CLERK',7902,'1980-12-17',800.00,NULL,20,'1')
,(7566,'JONES','MANAGER',7839,'1981-04-02',2975.00,NULL,20,'1')
,(7788,'SCOTT','ANALYST',7566,'1982-12-09',3000.00,NULL,20,'1')
,(7876,'ADAMS','CLERK',7788,'1983-01-12',1100.00,NULL,20,'1')
,(7902,'FORD','ANALYST',7566,'1981-12-03',3000.00,NULL,20,'1')
;

CREATE TABLE `emp30` (
  `empno` decimal(4,0) NOT NULL,
  `ename` varchar(10) DEFAULT NULL,
  `job` varchar(9) DEFAULT NULL,
  `mgr` decimal(4,0) DEFAULT NULL,
  `hiredate` date DEFAULT NULL,
  `sal` decimal(7,2) DEFAULT NULL,
  `comm` decimal(7,2) DEFAULT NULL,
  `deptno` decimal(2,0) DEFAULT NULL,
  `test` varchar(100) DEFAULT NULL
) ;


INSERT INTO emp30 (empno,ename,job,mgr,hiredate,sal,comm,deptno,test) VALUES 
(7499,'ALLEN','SALESMAN',7698,'1981-02-20',1600.00,300.00,30,'1')
,(7521,'WARD','SALESMAN',7698,'1981-02-22',1250.00,500.00,30,'1')
,(7654,'MARTIN','SALESMAN',7698,'1981-09-28',1250.00,1400.00,30,'1')
,(7698,'BLAKE','MANAGER',7839,'1981-05-01',2850.00,NULL,30,'1')
,(7844,'TURNER','SALESMAN',7698,'1981-09-08',1500.00,0.00,30,'1')
,(7900,'JAMES','CLERK',7698,'1981-12-03',950.00,NULL,30,'1')
;
```
## Import below tables into Power BI

1. emp
1. dept
1. salgrade
1. emp10
1. emp20
1. emp30


1. Open **Power BI Desktop** > Click on **Get Data** > Click on **Databases** > select **MySql Database** > click on **connect**

![](https://github.com/rritec/powerbi/blob/master/images/PBI_0089.png?raw=true)
 
1. provider server as **localhost** > Database as **rritec** > Click on **ok**

    ![](https://github.com/rritec/powerbi/blob/master/images/PBI_0090.png?raw=true)
    
1. Select all the tables as shown below > clcik on **LoadData** 

    ![](https://github.com/rritec/powerbi/blob/master/images/PBI_0091.png?raw=true)


## Do all exercise of Previous chapter [PBI_01_02_Power Query Editor Shape data using Excel as source](https://github.com/rritec/powerbi/blob/master/Notebooks/PBI_01_02_Power%20Query%20Editor%20Shape%20data%20using%20Excel%20as%20source.md)

## Questions
1. What is the official tool, to query MySql database?
    - MySQL Workbench
2. 
```python

```
