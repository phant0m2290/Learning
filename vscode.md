# Visual Studio Code
Just for clarity when i say vscode i mean visual studio code

Visual Studio Code (VSCode) is an so called IDE (Integrated Development Environment) AKA our code editor.\
You can install it from their website [here](https://code.visualstudio.com) or from their [github](https://github.com/Microsoft/vscode/). Do'nt forget to select the `add code to path` box.

## Running VSCode
There are multiple ways of opening vscode

### From the windows start menu
This is like how you open any other program but when you start it you wont be in your project folder.\
So click on `file > open folder` and select your project folder

### From the terminal
If you have not yet go follow the [Terminal](./terminal.md) tutorial.

Go to the directory of your project and run `code .`. This will open vscode at the directory you ran the command in.\

## The interface
![vscode interface](https://code.visualstudio.com/assets/docs/getstarted/userinterface/hero.png)\
(Image from official visual code website)

### A - The activity bar
There are a few icons in the activity bar.\
The one that looks like files opens the file explorer (not the windows one but the one from vscode). Here you can open, create, rename, delete your files.\
The magnifying glass allows you search for text trough all your files.\
The icons (old and new icon) listed below are the extensions tab. You can manage and install extensions from there.\
Old icon: ![old icon](./images/vscode-extentions-icon-old.PNG)\
New icon: ![new icon](./images/vscode-extentions-icon.PNG)

### B - The side bar
Depending what you opened from the activity bar you can see multiple things here.\
The files of your project, the search menu or other stuff.

### C - Editor
The editor is the place where you can see and edit your code. Click on files in the file explorer to open files and edit them.

### D - Panel
This is mainly used for the terminal. You can open a terminal by pressing `ctrl` + `shift` + `~`

### E - Status bar
This shows you information about your code. On the left you have the amount of errors and warnings. On the right you have the cursor position, indents size (tab size), text format, end of line sequence (nothing really important) and the current language your editing

## Useful extensions
Here are some useful extensions you can use in vscode.
| Name                    | Type              | URL                                                                                       |
|:-----------------------:|:-----------------:|:-----------------------------------------------------------------------------------------:|
| Code Spell Checker      | Spell check       | https://marketplace.visualstudio.com/items?itemName=streetsidesoftware.code-spell-checker |
| Material icon theme     | Icon pack         | https://marketplace.visualstudio.com/items?itemName=PKief.material-icon-theme             |
| Github Markdown Preview | Markdown overhaul | https://marketplace.visualstudio.com/items?itemName=bierner.github-markdown-preview       |
| Deno                    | Language support  | https://marketplace.visualstudio.com/items?itemName=denoland.vscode-deno                  |