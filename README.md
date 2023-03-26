# SQL-Querying-Assignment
sql commands


Questions


1. SELECT first_name, last_name FROM student;



2. SELECT instructor_id FROM instructor WHERE tenured = 1;




3. SELECT s.first_name AS student_first, s.last_name AS student_last, 
    	 a.first_name AS advisor_first, a.last_name AS advisor_last
FROM student s
JOIN instructor a ON s.advisor_id = a.instructor_id;



4. SELECT instructor_id, first_name, last_name
FROM instructor
WHERE instructor_id NOT IN (SELECT advisor_id FROM student WHERE advisor_id IS NOT NULL);



5. SELECT i.first_name, i.last_name, SUM(c.num_credits) AS total_credits
 	FROM instructor i
            JOIN course c ON i.instructor_id = c.instructor_id
            GROUP BY i.instructor_id;



6. SELECT course_code, course_name
    	FROM course
WHERE course_code LIKE '3%';



7. SELECT c.course_code, i.first_name, i.last_name, c.num_credits
FROM student_schedule ss
JOIN student s ON ss.student_id = s.student_id
JOIN course c ON ss.course_id = c.course_id
JOIN instructor i ON c.instructor_id = i.instructor_id
WHERE s.student_id = 1;















