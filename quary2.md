Risposte :

Secondo Esercizio sulle quary 15/12/2021:

- Esercizi GROUP BY

- 1) SELECT COUNT(id) AS 'number-of-student', YEAR(enrolment_date) AS 'enrolment-year'
FROM `students`
GROUP BY YEAR(enrolment_date);

- 2) SELECT COUNT(id) AS `number-of-person`,  `office_address` AS `location`
FROM `teachers` 
GROUP BY `office_address`

- 3) SELECT `exam_id` AS 'appello', AVG(`vote`) AS 'average'
FROM `exam_student`
GROUP BY `exam_id`

- 4) SELECT `department_id`,COUNT(department_id)
FROM `degrees`
GROUP BY `department_id`

__________________________________________________________________

- Esercizi JOIN

- 5) SELECT * FROM `degrees`
JOIN `students` ON students.degree_id = degrees.id 
WHERE degrees.name LIKE '%Economia';

- 6) SELECT degrees.name 
FROM departments
JOIN degrees ON degrees.department_id = departments.id
WHERE departments.name LIKE '%Neuroscienze'

- 7) 