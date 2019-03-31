# DB09-RelationalAlgebra
Database Assignment 09 - Relational Algebra

Assignment:

https://github.com/datsoftlyngby/soft2019spring-databases/blob/master/assignments/assignment9.md

-----

## Assignment Desciroption

Consider this query from the classic models:

```sql
select customers.customerName, offices.city as office_city
from customers, employees, offices
where 
	customers.salesRepEmployeeNumber = employees.employeeNumber and 
	employees.officeCode = offices.officeCode and
    customers.city = offices.city;
```

1. Rewrite it as an expression in relational algebra
2. Add row counts to the subexpressions
3. Rewrite to a better expression

---

### Assignment 1 And 2

![latex](https://latex.codecogs.com/svg.latex?\Pi_{customerName,office\\_city}(\rho_{office\\_city/office.city}(\sigma_{salesRepEmployeeNumber=employeeNumber}(customers^{119}\times%20(employees^{21}\bowtie%20offices^{6})^{22})^{2806})^{13}))

-----

### Assignment 3

![latex](https://latex.codecogs.com/svg.latex?\Pi_{customerName,office\\_city}(\rho_{office\\_city/office.city}((\sigma_{salesRepEmployeeNumber=employeeNumber}(customers^{119}\times%20employees^{21}))^{14}\bowtie%20offices^{6})^{22}))
