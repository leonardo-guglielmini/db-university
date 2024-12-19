### Selezionare tutti gli studenti iscritti al Corso di Laurea in Economia

```SQL
SELECT `students`.name, `students`.surname AS surname, `degrees`.name as degree_name
FROM `students`
JOIN `degrees`
ON `students`.degree_id = `degrees`.id
WHERE `degrees`.name = 'Corso di laurea in economia'
ORDER BY surname ASC;
```

### Selezionare tutti i Corsi di Laurea Magistrale del Dipartimento di Neuroscienze

```SQL
SELECT `degrees`.name as degree_name, `degrees`.level, `departments`.name as department_name
FROM `degrees`
JOIN `departments`
ON `degrees`.department_id = `departments`.id
WHERE `departments`.name = 'dipartimento di neuroscienze' AND `degrees`.level LIKE 'magistrale';
```

### Selezionare tutti i corsi in cui insegna Fulvio Amato (id=44)

```SQL
SELECT `courses`.name as course_name, `courses`.period, `courses`.year, `teachers`.name as teacher_name, `teachers`.surname as teacher_surname
FROM `courses`
JOIN `course_teacher`
ON `courses`.id = `course_teacher`.course_id
JOIN `teachers`
ON `course_teacher`.teacher_id = `teachers`.id
WHERE `teachers`.id = 44
ORDER BY course_name ASC;
```

### Selezionare tutti gli studenti con i dati relativi al corso di laurea a cui sono iscritti e il relativo dipartimento, in ordine alfabetico per cognome e nome

```SQL
SELECT `s`.name AS student_name, `s`.surname AS student_surname, `deg`.name AS degree_name, `dep`.name AS department_name
FROM `students` AS `s`
JOIN `degrees` AS `deg`
ON `s`.degree_id = `deg`.id
JOIN `departments` AS `dep`
ON `deg`.department_id = `dep`.id
ORDER BY student_surname ASC, student_name ASC;
```

### Selezionare tutti i corsi di laurea con i relativi corsi e insegnanti

```SQL
SELECT `degrees`.name as degree_name, `courses`.name AS course_name, `teachers`.name AS teacher_name, `teachers`.surname AS teacher_surname
FROM `degrees`
JOIN `courses`
ON `degrees`.id = `courses`.degree_id
JOIN `course_teacher`
ON `courses`.id = `course_teacher`.course_id
JOIN `teachers`
ON `course_teacher`.teacher_id = `teachers`.id
ORDER BY degree_name ASC;
```

### Selezionare tutti i docenti che insegnano nel Dipartimento di Matematica (54)

```SQL
SELECT DISTINCT `teachers`.name AS teacher_name, `teachers`.surname AS teacher_surname, `departments`.name AS department_name
FROM `teachers`
JOIN `course_teacher`
ON `teachers`.id = `course_teacher`.teacher_id
JOIN `courses`
ON `course_teacher`.course_id = `courses`.id
JOIN `degrees`
ON `courses`.degree_id = `degrees`.id
JOIN `departments`
ON `degrees`.department_id = `departments`.id
WHERE `departments`.name = 'dipartimento di matematica' /*OPPURE TRAMITE `departments`.id = 5*/
ORDER BY teacher_surname ASC, teacher_name ASC;
```

### BONUS: Selezionare per ogni studente il numero di tentativi sostenuti per ogni esame, stampando anche il voto massimo. Successivamente, filtrare i tentativi con voto minimo 18

```SQL

```
