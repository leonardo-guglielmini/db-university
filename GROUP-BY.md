### Contare quanti iscritti ci sono stati ogni anno

```SQL
SELECT COUNT(id) as total_students, YEAR(enrolment_date) as year
FROM `students`
GROUP BY YEAR(enrolment_date);
```

### Contare gli insegnanti che hanno l'ufficio nello stesso edificio

```SQL
SELECT COUNT(id) as total_teachers, office_address
FROM `teachers`
GROUP BY office_address
ORDER BY office_address ASC;
```

### Calcolare la media dei voti di ogni appello d'esame

```SQL

```

### Contare quanti corsi di laurea ci sono per ogni dipartimento

```SQL

```
