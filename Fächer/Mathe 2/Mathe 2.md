---
typ: Fach
notetoolbar: Fach
Professor: 
Semester: 2
Schlussnote:
---


```ad-Test

```



```dataview
Table without ID file.link as Hausaufgaben,
Tasks.text as "To-Do",
Abgabedatum

From [[]]

Where Abgeschlossen = false

flatten list(file.tasks) as Tasks
```
---
![[Picture2-1.png|432x93]]
```dataview
Table without ID file.link as Themen,
Beschreibung,
Meisterung

From [[]]

where typ = "Wissen"


flatten list(file.tasks) as Tasks


```

---
###### Abgeschlossene Hausaufgaben

```dataview
Table without ID file.link as "Abgeschlossene Hausaufgaben",
Abgabedatum,
Abschlussdatum

From [[]]

Where Abgeschlossen = true
```

