---
Abgeschlossen: false
Abgabedatum: 
typ: Hausaufgabe
---
[Fach:: [[<% tp.file.folder()%>]]]
[Aufgabe:: <% tp.system.prompt("Aufgabe:") %>] 

<%*

const fullPath = tp.file.path(true);
const Fachname = fullPath.split("/").slice(0, -1).join("/");
const HausaufgabenFolder = Fachname + "/Hausaufgaben";
const folder = app.vault.getAbstractFileByPath(HausaufgabenFolder);
if (!folder) {
  await app.vault.createFolder(HausaufgabenFolder);
}
const today = tp.date.now('YYYY-MM-DD');
let HausaufgabenNumber = 1;
const updatedFolder = app.vault.getAbstractFileByPath(HausaufgabenFolder);
const todaysHausaufgabenNotes = updatedFolder.children.filter(child =>
  child instanceof tp.obsidian.TFile && child.basename.startsWith(`${today}`)
);
if (todaysHausaufgabenNotes.length) {
  todaysHausaufgabenNotes.sort((a, b) => a.path < b.path ? 1 : -1);
  const latestHausaufgabenNote = todaysHausaufgabenNotes[0];
  const match = latestHausaufgabenNote.basename.match(/\d+$/);
  if (match) {
    HausaufgabenNumber = parseInt(match[0], 10) + 1;
  }
}
const HausaufgabenName = `${today} No. ${HausaufgabenNumber}`;
const newPath = `${HausaufgabenFolder}/${HausaufgabenName}`;

await tp.file.rename(HausaufgabenName)
await tp.file.move(newPath)

-%>