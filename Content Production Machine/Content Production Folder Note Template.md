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
const productionsDir = '"' + dv.current().file.folder + '/Productions"';
const productions = dv.pages(productionsDir).file
let events = [];

// List of publish dates
const publishDateColor = '#B4BEFE';
productions.forEach(p => {
	if (p.frontmatter.publishedAt != undefined) {
		events.push([{
			start: new Date(p.frontmatter.publishedAt),
			id: p.link,
			title: p.name,
			textColor: publishDateColor
			}]);
	}
});
// List of tasks
const taskColor = '#fab387';
const tasks = dv.pages(productionsDir)
	.file.tasks
	.where(t => !t.completed)
	.where(t => t.status == ' ')
	.where(t => {
		if (typeof(t.scheduled) == 'object') {
			return t.scheduled <= dv.date('today')
		} else if (typeof(t.due) == 'object') {
			return t.due <= dv.date('today')
		}
		return false
	})
	.map((t) => {
		if (typeof(t.scheduled) == 'object') {
			t.due = t.scheduled
		}
		return t;
	});
tasks.map((
	function(task) {
		events.push([{
		start: new Date(task.due),
		id: task.link,
		title: task.text,
		color: taskColor
		}])
	}
))
let calendar = renderCalendar(this.container, events);
calendar.render();
window.setTimeout(_ => {calendar.changeView('dayGridMonth');}, 1);
```
