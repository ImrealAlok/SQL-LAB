# Experiment-3

## Aim

1.List all employers and jobs in department 30 in descending order by salary.
2.List job and department No. of employes whose name are five letters long begin with "A" and end with "N"
3.Display name of employes whose name ends with alphabet S.
4.Display the names of employes working in department no. 10 or 20 or 40 or employers working as clerks, salesman or analyst.
5.Display employee member names for employes who earn commission
6.Display employee no. and total salary for each employee.
7.Display employee no and annual salary for each employee.
8.Display the names of all employes working as clerks and drawing a salary more than 3000.
9.Display the names of employees who are working and drawing a salary more than 3000.

## Queries

### List all employers and jobs in department 30 in descending order by salary.

```sql
    SELECT ENAME, JOB
    FROM Employee
    WHERE DEPTNO = 30
    ORDER BY SAL DESC;
```

### List job and department No. of employes whose name are five letters long begin with "A" and end with "N"

```sql
    SELECT JOB, DEPTNO
    FROM Employee
    WHERE ENAME LIKE 'A___N';
```

### Display name of employes whose name ends with alphabet S.

```sql
    SELECT ENAME
    FROM Employee
    WHERE ENAME LIKE '%S';
```

### Display the names of employes working in department no. 10 or 20 or 40 or employers working as clerks, salesman or analyst.

```sql
    SELECT ENAME
    FROM Employee
    WHERE DEPTNO IN (10, 20, 40)
    OR JOB IN ('CLERK', 'SALESMAN', 'ANALYST');
```

### Display employee member names for employes who earn commission

```sql
    SELECT ENAME
    FROM Employee
    WHERE COMM IS NOT NULL
    AND COMM > 0;
```

### Display employee no. and total salary for each employee.

```sql
    SELECT EMPNO, (SAL + NVL(COMM, 0)) AS TOTAL_SALARY
    FROM Employee;
```

### Display employee no and annual salary for each employee.

```sql
    SELECT EMPNO, (SAL * 12) AS ANNUAL_SALARY
    FROM Employee;

```

### Display the names of all employes working as clerks and drawing a salary more than 3000.

```sql
    SELECT ENAME
    FROM Employee
    WHERE JOB = 'CLERK'
    AND SAL > 3000;
```

### Display the names of employees who are working and drawing a salary more than 3000.

```sql
    SELECT ENAME
    FROM Employee
    WHERE SAL > 3000;
```
