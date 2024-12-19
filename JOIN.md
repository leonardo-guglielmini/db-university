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

```

### Selezionare tutti i corsi in cui insegna Fulvio Amato (id=44)

```SQL

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
