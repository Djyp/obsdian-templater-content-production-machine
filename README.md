# Content Production Machine

This is my small contribution to the Obsidian Community.

Inspired by [August Bradley's PPV System](https://www.yearzero.io/notion-life-design) where he presents his [Content Production Machine](https://www.youtube.com/watch?v=sZ-NRA3C3_I).

I needed that for my projects. I'd need more than that actually to give me a more broad point of view over all projects.

## Plugins
- [Columns](https://github.com/tnichols217/obsidian-columns)
- [Dataview](https://blacksmithgu.github.io/obsidian-dataview/)
- [DB Folder](https://rafaelgb.github.io/obsidian-db-folder/)
- [Full Calendar](https://github.com/obsidian-community/obsidian-full-calendar)
- [Templater](https://silentvoid13.github.io/Templater/)
- Not mandatory : [Folder Notes](https://lostpaul.github.io/obsidian-folder-notes/)

You can also avoid using **Columns** by changing the **Folder Note Template**.
It is not yet visible but I aslo use the [Tasks](https://publish.obsidian.md/tasks) plugin. Scheduled tasks are used in the "Next Action Date" column.

## Vocabulary
- **template** : this whole project or a single file
- **folder note** : the file at the root of your machine, named the sameway as the machine

## Goal & Features
The template is useful to create multiple Content Production Machines. If you need only one, you can download the files and adapt them as you'd like. I consider the whole folder as a single template.

It gives you a database of all your projects. They are stored in the Productions folder. You can see all your projects as a table in the file suffixed `-Table.md`. You get a calendar view in the folder note.

Using DB Folder features, you can sort and filter through your productions to get a better view of your next task and plan your work.

## How it works
Place the folder named "Content Production Machine" under `Extra/Templates`.
A whole machine is set up using **ONLY** `Content Production Folder Note Template`.

- Create a new folder where your machine will be set
- Name it like you want to name your machine
- Create an empty file named just like the folder. You can also use the "Create markdown folder note" command from Folder Note
- Type `Alt + E` to get the Templater modal
- Choose "Content Production Folder Note Template"
- It creates
   - the content of your folder note
   - an empty Productions folder
   - a file named just like your machine, suffixed with " Table"
- Congrats, your machine is set
- Now get to the table view
- Click on the + to create a new file
- The prompt will ask for a file name and to select a template
- Make sure the template is the right one : Extra/Templates/Content Production Machine/Content Production Template.md
- It creates a new production, with all the basics properties and a structure to organize your production

Once installed and used once, you get something like that :
```shell
Extra
   ╰─ Templates
      ╰─ Content Production Machine
         ╰─ Productions (this folder is not that useful though)
         ╰─ Content Production Folder Note Template.md
         ╰─ Content Production Table Template.md
         ╰─ Content Production Template.md
Path/To/Project Content Production
   ╰─ Productions
      ╰─ … production files you have created
   ╰─ Project Content Production.md
   ╰─ Project Content Production Table.md
```

## Improvements
- Improve the calendar view with publication dates and scheduled tasks
- Test if you can create a folder note named differently from the folder it is in
- Decide to delete the useless Productions folder in the templates
- Find a shorter name and choose better words to make it more clear
- Make it so it fits anyone's file structure
- Better labels for the colums
- Avoid the frenghlish content to a complete english template

## Personal choices
I used Folder Notes to have less files in the file explorer. And having the folder to be clickable makes it more like a starting point.

The colors are based on [Catpuccin Mocha](https://catppuccin.com/palette) to fit with my own environment. They are the ones I've set in the DB Folder (Table file) when you select a status.
