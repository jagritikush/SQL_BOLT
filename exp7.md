1.Find the list of all buildings that have employees .

  SELECT DISTINCT b.building_name
  FROM Buildings b
  INNER JOIN Employees e
  ON b.building_name = e.building;

2.Find the list of all buildings and their capacity.

  SELECT Building_name, capacity
  FROM Buildings;

3. List all buildings and the distinct employee roles in each building (including empty buildings).

   SELECT DISTINCT b.building_name, e.role
   FROM Buildings b
   LEFT JOIN Employees e
   ON b.building_name = e.building;