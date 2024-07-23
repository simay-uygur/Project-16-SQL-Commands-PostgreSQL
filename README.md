# Project-16-SQL-Commands-PostgreSQL
These are assignments given in Patika Java Intermediate course.

The taks are:

- Group the films in the film table by their rating values.
- When grouping the films in the film table by the replacement_cost column, list the replacement_cost values and the corresponding number of films where the number of films is more than 50.
- What are the numbers of customers corresponding to the store_id values in the customer table?
- After grouping the city data in the city table by the country_id column, share the country_id information and the number of cities for the country_id that contains the most cities.


## Answers:
Rating groups:
1. 
```
PG
R
NC-17
PG-13
G
```
2. 
```
12.99 55
13.99 55
14.99 51
20.99 57
21.99 55
22.99 55
27.99 53
29.99 53

```

3. 
```
1 326
2 273

```

4. 
````
44 60
```


The Queries are

````
-- Task1
SELECT rating FROM film
GROUP BY rating;


-- Task 2
SELECT replacement_cost , COUNT(*) FROM film
GROUP BY replacement_cost
HAVING COUNT(*) > 50
ORDER BY replacement_cost , COUNT(*);


-- Task 3
SELECT store_id, COUNT(*) FROM customer
GROUP BY store_id;

-- Task 4
SELECT country_id, COUNT(*) FROM city
GROUP BY country_id
ORDER BY COUNT(*) DESC
LIMIT 1;

```