Risposte :

Secondo Esercizio sulle quary 15/12/2021:
- 1) SELECT COUNT(id) AS 'number-of-student', YEAR(enrolment_date) AS 'enrolment-year'
FROM `students`
GROUP BY YEAR(enrolment_date);

- 2) SELECT COUNT(id) AS `number-of-person`,  `office_address` AS `location`
FROM `teachers` 
GROUP BY `office_address`

- 3) 