A collaborative **note-taking app** built with **Spring Boot (server)** and **JavaFX (client)**, featuring markdown support, collections, file attachments, multi-server setups, and full keyboard navigation.

# FULL APP TUTORIAL
## Markdown Basics

All of the notes have markdown. To use the features:

### Italics
To italicize text, wrap it in single asterisks (*)
*This is italicized text.*

### Bold
To bold text, wrap it in double asterisks (**)
**This is bold text.**

### Headers
Use # followed by a space to create headers. 
Add more # for smaller headers:
# Header 1 
## Header 2 
### Header 3

### Tags
Use # to create tags in your notes. 
Example: #Important or #Todo

### Note Links
Use double square brackets `[[noteName]]` to refer to another note. 
Example: `[[MeetingNotes]]` will create a link to the note titled "MeetingNotes".

---

## Keybord Shortcuts

The app is fully navigatable using only the Keybord. For full navigations the user must use the arrows ←↑↓→.
If he wants to press a button or open a dropdown menu the user can do that by pressing ENTER ↵.

Here are the shortcuts for fast navigation:
- ESC puts focus on the search bar
- C puts focus on the collection dropdown menu (If you are not currently typing in the descirption box or editing a note name)
- = or + create a new note/collection (depending on the scene you are currently on)(Does not work when in all collections)
- DELETE (␡ button not backspace) deletes the selected note/collection (depending on the scene you are currently on) (Does not work when in all collections)
- CTRL + Z undoes the last operation

You can clear tags using only the keyboard. Navigate to the first dropdown tag menu. Click one time the right arrow ->. After that press enter.


## BUTTONS TUTORIAL

### Note Scene
- 📝 creates a new note called Untilted Note + an index if there is a note with the same Note
- 🗑 Deletes the selected note
- ⮝ Moves the selected note a position up (to prioritize more important notes)
- ⮟ Moves the selected note a position down (to move notes which are not that important to the bottom)
- ⎌ Opens a popup with all of the last operations. Double clicking on an option will undo all actions above it and the selected action. The trash bin button that appears in this menu can be used to delete all previous operations. Up to 30 operations are stored and this feature supports 7 undo action types.
- ⮫ Opens a scene with all of the collections. Double clicking a collection will move the selected note to the selected collection
- 📎 Lets you attach files
- 📂 Opens / Closes a menu with all files in the selected note. They can be renamed, deleted or moved to a different note from here
- 🎨 Lets you change the color layout of the file
- Double clicking on a note allows you to rename it

### Collections scene
- +Adds a new collection
- -Deletes the seelected collection
- Save - saves changes 

## How to start/create new servers

- To start more that one server you have to create another configuration in intelij. 
- Every configuration should include the port specified in the form of -Dserver.port=8080 and the profile name which should be equal to the name from properties file. ex server1, server2, server3
- To create a new server add it to the servers.txt file  in commons an create a new configuration following the format of the already created ones.
For every server the new configuration is needed: like application-server1.properties: the file should include the port and the name of the server in the configuration file
- For the first three servers the property files are already included and the only needed thing is to create the right intelliJ configuration with VM variables and active profile name.


## Usability:

We have implemented 20+ warnings/errors, some harder to get than others but they are there. 
Some Examples are: 
- Trying to clear tags when there are none.
- Trying to add notes while you are filtering by tag
- Trying to delete/Move to a different collection without having selected a note
- Trying to move notes up and down while searching
- Much more

Multivisualisation elemets:

- status bar for 3+ features at least
- Collection status update in collection scene (All changes saved/Unsaved chnaged)
- Flags for each language when you click on the languge menuButton 
- Search bar icon next to searchBar

We have implemented a lot of informational popups:

- a status bar on top of the note that presents colored text when you create/delete/move up down to the other collection a note and when you swith a colelction
- When you replace a reference it gives you an information popup
- some more informational popups

We have also implemented confirmation popups:

- trying to delete a note or collection
- Trying to move a note to a different collection
- Trying to move a note with the same name to a collection where the name already exists

## WebView color:
We have implemented the option for the user to include his own CSS for webview.
User can specify his intended CSS for webview in client/user.css file.
This CSS will be used for the webview only.
If the user will leave this file empty, the style will be automatically set to the scene's style.
