---
notetoolbar: Neues Fach Hinzufügen
cssclasses:
  - cards
---


```dataview
table
OffeneHausaufgaben.text

FROM "Fächer"

where typ = "Fach"

FLATTEN list(flat(file.inlinks.file.tasks)) as AlleHausaufgaben
FLATTEN list(filter(AlleHausaufgaben, (task) => !task.completed)) as OffeneHausaufgaben
```

