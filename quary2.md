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

- 7) SELECT *
FROM `teachers`
JOIN course_teacher ON course_teacher.teacher_id = teachers.id
WHERE course_teacher.teacher_id = 44;

- 8) SELECT degrees.name, degrees.level, degrees.address, degrees.email, degrees.website
FROM `degrees`
JOIN `students` ON students.degree_id = degrees.id
JOIN `departments` ON departments.id = degrees.department_id
ORDER BY `students`.`surname` ASC, `students`.`name` ASC;

- 9) SELECT courses.name AS 'courses', degrees.name AS 'degrees', teachers.name AS 'with'
FROM `courses`
JOIN `course_teacher` ON course_teacher.course_id = courses.id
JOIN `teachers` ON teachers.id = course_teacher.teacher_id
JOIN `degrees` ON degrees.id = courses.degree_id

- 10) SELECT DISTINCT teachers.name AS 'Teacher Name', teachers.surname AS 'Teacher Lastname', departments.name AS 'Department'
FROM `course_teacher`
JOIN `courses` ON courses.id = course_teacher.course_id
JOIN `degrees` ON degrees.id = courses.degree_id
JOIN `departments` ON departments.id = degrees.department_id
JOIN `teachers` ON teachers.id = course_teacher.teacher_id
WHERE `departments`.id = 5

