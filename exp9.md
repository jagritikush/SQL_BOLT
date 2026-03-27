 List all movies and their combined sales in millions of dollars . 

  SELECT title,
  (domestic_sales + international_sales) / 1000000 AS combined_sales_millions
  FROM Movies
  JOIN Boxoffice
  ON Movies.id = boxoffice.movie_id

2. List all movies and their ratings in percent.

   SELECT title,
   Rating * 10 AS rating_percent
   FROM Movies
   JOIN Boxoffice
   ON Movies.id = boxoffice.movie_id

3. List all movies that were released on even number year.

   SELECT title
   FROM Movies
   WHERE year % 2 = 0;