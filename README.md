UPDATE employees
SET salary = salary * 1.1
WHERE department = 'HR';

DELETE FROM salary
WHERE salary < (SELECT AVG(salary) FROM salary);

INSERT INTO new_departments (name, location)
SELECT DISTINCT department, 'New York'
FROM employees
WHERE department = 'Finance';
