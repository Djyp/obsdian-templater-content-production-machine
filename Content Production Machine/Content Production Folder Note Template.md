<%*
// Récupérer le nom du projet
const projectName = tp.file.folder()
const productionsDir = tp.file.folder(true) + "/Productions"

// Créer le dossier de Productions
app.vault.createFolder(productionsDir)

// Créer le DB Folder
const tableTemplateFile = await tp.file.find_tfile('Content Production Table Template')
await tp.file.create_new(tableTemplateFile, tp.file.folder(true) + "/" + projectName +" Table")
%>---
cssclasses:
  - wide-page
  - NoProps
---

````col
```col-md
# 🏭 <%* tR += projectName %>
```
```col-md
# [[<%* tR += projectName %> Table|🗃 Vue en tableau]]
```
````
```dataviewjs
this.container.style.minHeight = "620px";
const { renderCalendar } = app.plugins.plugins["obsidian-full-calendar"];
const tasks = dv.pages('"' + dv.current().file.folder + '/Productions"').file

let calendar = renderCalendar(this.container, tasks.map(
function(task) {
	return {
	start: new Date(task.frontmatter.createdAt),
	id: task.link,
	title: task.name,
	};
}
));
calendar.render();
window.setTimeout(_ => {calendar.changeView('dayGridMonth');}, 1);
```
