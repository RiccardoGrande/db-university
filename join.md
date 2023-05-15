1. Selezionare tutti gli studenti iscritti al Corso di Laurea in Economia

SELECT `students`.`name`, `students`.`surname`, `students`.`degree_id`, `degrees`.`name`
FROM `students` 
JOIN `degrees` ON `students`.`degree_id` = `degrees`.`id` 
WHERE `degrees`.`name` = 'Corso di Laurea in Economia';




2. Selezionare tutti i Corsi di Laurea Magistrale del Dipartimento di Neuroscienze

SELECT `degrees`.`department_id`,`degrees`.`level`,`degrees`.`name`, `departments`.`name`
FROM `degrees`
JOIN `departments` ON `departments`.`id`
AND `departments`.`name` = 'Dipartimento di Neuroscienze'
WHERE LEVEL = 'magistrale';


3. Selezionare tutti i corsi in cui insegna Fulvio Amato (id=44)

SELECT *
FROM `course_teacher` 
JOIN `teachers` ON `id` = `course_teacher`.`teacher_id` 
WHERE `course_teacher`.`teacher_id` = '44';


4. Selezionare tutti gli studenti con i dati relativi al corso di laurea a cui sono iscritti e il
relativo dipartimento, in ordine alfabetico per cognome e nome


5. Selezionare tutti i corsi di laurea con i relativi corsi e insegnanti


6. Selezionare tutti i docenti che insegnano nel Dipartimento di Matematica (54)


7. BONUS: Selezionare per ogni studente quanti tentativi d’esame ha sostenuto per superare ciascuno dei suoi esami