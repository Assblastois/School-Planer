---
notetoolbar: Neues Fach Hinzufügen
cssclasses:
  - cards
---


````tabs
tab: Aktuelles Semester

```dataview
table
card-cover,
OffeneHausaufgaben.text

FROM "Fächer"

where typ = "Fach"
where Semester = 1

FLATTEN list(flat(file.inlinks.file.tasks)) as AlleHausaufgaben
FLATTEN list(filter(AlleHausaufgaben, (task) => !task.completed)) as OffeneHausaufgaben
```


tab: Alle Semester

Semester 1
```dataview
table
OffeneHausaufgaben.text

FROM "Fächer"

where typ = "Fach"
where Semester = 1

FLATTEN list(flat(file.inlinks.file.tasks)) as AlleHausaufgaben
FLATTEN list(filter(AlleHausaufgaben, (task) => !task.completed)) as OffeneHausaufgaben
```
Semester 2
```dataview
table
OffeneHausaufgaben.text

FROM "Fächer"

where typ = "Fach"
where Semester = 2

FLATTEN list(flat(file.inlinks.file.tasks)) as AlleHausaufgaben
FLATTEN list(filter(AlleHausaufgaben, (task) => !task.completed)) as OffeneHausaufgaben
```
Semester 3

```dataview
table
OffeneHausaufgaben.text

FROM "Fächer"

where typ = "Fach"
where Semester = 3

FLATTEN list(flat(file.inlinks.file.tasks)) as AlleHausaufgaben
FLATTEN list(filter(AlleHausaufgaben, (task) => !task.completed)) as OffeneHausaufgaben
```

Semester 4

```dataview
table
OffeneHausaufgaben.text

FROM "Fächer"

where typ = "Fach"
where Semester = 4

FLATTEN list(flat(file.inlinks.file.tasks)) as AlleHausaufgaben
FLATTEN list(filter(AlleHausaufgaben, (task) => !task.completed)) as OffeneHausaufgaben
```


Semester 5

```dataview
table
OffeneHausaufgaben.text

FROM "Fächer"

where typ = "Fach"
where Semester = 5

FLATTEN list(flat(file.inlinks.file.tasks)) as AlleHausaufgaben
FLATTEN list(filter(AlleHausaufgaben, (task) => !task.completed)) as OffeneHausaufgaben
```


Semester 6
```dataview
table
OffeneHausaufgaben.text

FROM "Fächer"

where typ = "Fach"
where Semester = 6

FLATTEN list(flat(file.inlinks.file.tasks)) as AlleHausaufgaben
FLATTEN list(filter(AlleHausaufgaben, (task) => !task.completed)) as OffeneHausaufgaben
```
tab: Offene Hausaufgaben

```dataview
table
Fach as Fach,
Abgabedatum as Abgabedatum,
Aufgabe as Aufgabe
From "Fächer"
where Abgeschlossen = false


```

````

