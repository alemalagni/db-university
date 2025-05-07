## 1. Selezionare tutti gli studenti iscritti al Corso di Laurea in Economia
```
SELECT *
FROM `students`
INNER JOIN `degrees`
WHERE degrees.name = "Corso di Laurea in Economia";
```
----

## 2. Selezionare tutti i Corsi di Laurea Magistrale del Dipartimento di Neuroscienze
```
SELECT *
FROM `degrees`
INNER JOIN `departments`
ON departments.id = degrees.department_id
WHERE departments.name = "Dipartimento di Neuroscienze";
```
----

## 3. Selezionare tutti i corsi in cui insegna Fulvio Amato (id=44)
```
SELECT *
FROM `courses`
INNER JOIN `course_teacher`
WHERE `teacher_id` = "44";
```
----

## 4. Selezionare tutti gli studenti con i dati relativi al corso di laurea a cui sono iscritti e il relativo dipartimento, in ordine alfabetico per cognome e nome
```
SELECT *
FROM `students`
INNER JOIN `degrees`
ON degrees.id = students.degree_id
INNER JOIN `departments`
ON departments.id = degrees.department_id
ORDER BY `surname` ASC;
```
----