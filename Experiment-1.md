#Experiment-1

## Aim

1. Create employee_master table with data using employee table.
2. Delete all rercord from Employee_master whose DEPTNO is 10
3. Update 10% in his salary of DEPTNO 20 into Employee_Master
4. Alter SAL with size 10,2 in employee_master
5. Drop employee-master table.

##Query

### Create employee_master table wiht data using employee table.

```sql
    CREATE TABLE Employee_Master AS SELECT * FROM Employee;
```

### Delete all record from Employee_Master whose DEPTNO is 10

```sql
    DELETE FROM Employee_Master WHERE DEPTNO = 10;
```

### Update 10% in his salary of DEPTNO 20 into Employee_Master

```sql
    UPDATE Employee_Master SET sal = sal * 1.10 WHERE DEPTNO = 20;
```

### Alter SAL with size 10,2 in employee_master

```sql
    ALTER TABLE Employee_Master MODIFY sal DECIMAL(10,2);
```

## Drop employee-master table.
