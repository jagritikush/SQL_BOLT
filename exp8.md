1. Find the name and role of all employees who have not been assigned to a building .

   SELECT Name, Role 
   FROM Employees
   WHERE Building IS NULL;

2. Find the names of the buildings that hold no employees.

   SELECT b.building_name
   FROM Buildings b
   LEFT JOIN Employees e
   ON b.building_name = e.building
   WHERE e.name IS NULL;