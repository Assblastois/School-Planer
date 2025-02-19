---
typ: Fach
notetoolbar: Fach
Professor: 
Semester: 1
Schlussnote: 
card-cover: "![[image.png]]"
---

```ad-Test
02.06.2025 - Lineare Gleichungen
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

