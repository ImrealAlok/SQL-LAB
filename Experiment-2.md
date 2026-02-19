# Experiment-2

## Aim

1.List all distinct job in employee.
2.List all information about employee in department no 30.
3.Find all department member with department names greater than 20.
4.Find all information about all the managers as well as the clerks in department 30.
5.List the employee name, employee members and department of all clerks
6.Find all managers in department 30
7.List info about all employees in department 10 who are not managers or clerks.
8.Find employees and jobs earning between 1200 to 1400.
9.List Name and department no of employee who are clerks analyst or salesman.
10.List name and department no of employee whose names began with M.

## Queries

### List all distinct job in employee.

```sql
    SELECT DISTINCT JOB FROM Employee
```

### List all information about employee in department no 30.

```sql
    SELECT *
    FROM Employee
    WHERE DEPTNO = 30;
```

### Find all department member with department names greater than 20.

```sql
    SELECT *
    FROM Employee
    WHERE DEPTNO > 20;
```

### Find all information about all the managers as well as the clerks in department 30.

```sql
    SELECT *
    FROM Employee
    WHERE DEPTNO = 30
    AND JOB IN ('MANAGER', 'CLERK');

```

### List the employee name, employee members and department of all clerks

```sql
    SELECT ENAME, EMPNO, DEPTNO
    FROM Employee
    WHERE JOB = 'CLERK';
```

### Find all managers in department 30.

```sql
    SELECT *
    FROM Employee
    WHERE JOB = 'MANAGER'
    AND DEPTNO = 30;
```

### List info about all employees in department 10 who are not managers or clerks.

```sql
    SELECT *
    FROM Employee
    WHERE DEPTNO = 10
    AND JOB NOT IN ('MANAGER', 'CLERK');
```

### Find employees and jobs earning between 1200 to 1400.

```sql
    SELECT ENAME, JOB
    FROM Employee
    WHERE SAL BETWEEN 1200 AND 1400;
```

### List Name and department no of employee who are clerks analyst or salesman.

```sql
    SELECT ENAME, DEPTNO
    FROM Employee
    WHERE JOB IN ('CLERK', 'ANALYST', 'SALESMAN');
```

### List name and department no of employee whose names began with M.

```sql
    SELECT ENAME, DEPTNO
    FROM Employee
    WHERE ENAME LIKE 'M%';
```
