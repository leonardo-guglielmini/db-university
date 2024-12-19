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

```

### Selezionare tutti i corsi di laurea con i relativi corsi e insegnanti

```SQL

```

### Selezionare tutti i docenti che insegnano nel Dipartimento di Matematica (54)

```SQL

```

### BONUS: Selezionare per ogni studente il numero di tentativi sostenuti per ogni esame, stampando anche il voto massimo. Successivamente, filtrare i tentativi con voto minimo 18

```SQL

```
