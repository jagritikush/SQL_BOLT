1. Find the domestic and international sales for each movie.

   SELECT * Domestic_sales, International_sales
   FROM Boxoffice
   INNER JOIN Movies
   ON Movies.id = Boxoffice.Movie_id;

2. Show the sales numbers for each movie that did better internationally rather than domestically.

   SELECT * 
   FROM Boxoffice
   INNER JOIN Movies
   ON Movies.id = Boxoffice.Movie_id
   WHERE International_sales > Domestic_sales;

3. List all the movies by their ratings in descending order

   SELECT * 
   FROM Boxoffice
   INNER JOIN Movies
   ON Movies.id = Boxoffice.Movie_id
   ORDER BY Rating DESC 