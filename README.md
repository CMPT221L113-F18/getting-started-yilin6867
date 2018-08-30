# Getting Started

*Goals:* Acquaint yourself with BASH, Git, text editors, and the HTML5 Family of technologies.

*Prerequisites:* Basic understanding of and ability to use a Web browser, graphical desktop environment, and file/folder hierarchy.

*References:*

- [Git Documentation](https://git-scm.com/doc)
- [Introduction to the Linux Terminal](https://www.digitalocean.com/community/tutorials/an-introduction-to-the-linux-terminal)
- [MDN: Getting Started with the Web](https://developer.mozilla.org/en-US/docs/Learn/Getting_started_with_the_web)

## Cloning the lab repository

*In a Web browser:*

These instructions assume that you are looking at the GitHub page for this repository within a Web browser.

1. From the GitHub page for this repository, click on the green "Clone or Download" button to reveal the repository URL.
2. Copy this URL.

*In a BASH terminal:*

1. Clone the Lab repository by entering the following command, replacing *PATH_TO_REPO* by pasting the URL you copied above. `git clone PATH_TO_REPO SD2-Lab01`
2. Enter the newly created repository folder by *changing your working directory* (i.e., "going into the folder"). `cd SD2-Lab01`
3. List the contents of your working directory to see what is already in this repository. `ls -a`

Notes:

- In the git-clone command above, we provided a folder name after the repository URL. This optional *command argument* indicates the desired folder name that git will create. Without that optional argument, git will use the last part of the URL itself as the folder name, which is normally what we want to do as developers. Here I simply wanted to ensure uniform folder names to simplify the instructions.
- When listing the directory contents, we used a *command option* `-a` to ensure that all files are shown. Without that option, files whose names begin with a `.` (called "dot-files") are hidden from view. We note here that a "git repository" is simply a folder that contains appropriate meta-data contained in a `.git` subfolder.

## Create a simple Web app

Making a super-simple interactive Web page will allow us not only to dip our toes into the HTML5 Family of Web technologies, but also to practice using a text editor and the Git version control system.

To this end, we'll make a "Heat Index Calculator" that accepts the temperature (in Fahrenheit) and relative humidity (as a percentage between 0 and 100) and computes the index according to the following formula: `index = -42.379 + 2.04901523 * temp + 10.14333127 * relhum - 0.22475541 * temp * relhum - 0.00683783 * temp^2 - 0.05481717 * relhum^2 + 0.00122874 * temp^2 * relhum + 0.00085282 * temp * relhum^2 - 0.00000199 * temp2 * relhum^2`

Your app should be an interactive HTML5 Web page stored in a file named "heatindex.html" that meets the following requirements:

- uses valid, semantic HTML5 ([see the W3C Validator](https://validator.w3.org/))
- employs a top-level heading and paragraph to introduce the app
- employs a form element with input boxes, labels, a button, and an output element
- embeds JavaScript event handlers to manage the user interaction and compute the result
- embeds a CSS stylesheet to make it less ugly

If you are entirely new to HTML5, CSS, and JavaScript, please see the sample HTML5 Web app that is included in this repository. Also, feel free to get help from classmates and use the references at the top of this README file.

You may use any suitable text editor that is available on the lab computers or on your personal laptop. Absolutely do _not_ edit the code directly on GitHub in the browser. This is terrible practice. Write your code locally, and then use Git from the BASH terminal to record and publish your work to the repository.

## Recording your changes with Git

Let's assume you've done the work described above, or at least gotten started and have some code written. You will want to not only save your file locally (on the lab computer or laptop in front of you), but you should also let Git know about the changes you've made and publish this record of your changes to GitHub.

**Important:** See [First-Time Git Setup](https://git-scm.com/book/en/v2/Getting-Started-First-Time-Git-Setup) for instructions on how to make sure that Git knows who you are before making commits. Do _not_ skip this!

Once you have done the first-time setup...

0. In the BASH terminal, make sure that SD2-Lab01 is your working directory.
1. Stage your changes: `git add heatindex.html`
2. Commit your changes: `git commit -m "Wrote simple web app for Lab 01."`
3. Push your changes: `git push`
4. In your Web browser, visit the GitHub page for your repository and see that your changes are reflected in the history.

## Notes on editing plain-text files

Source code files are simply plain-text files that contain code written in a particular computer language. THe names of these files typically have handy *filename extensions* at the end to help indicate what sort of code is contained in the file and to give a hint to the OS about how to handle the file. **Important note:** Extensions do not determine the type of file. There is nothing to prevent me from naming a PDF file as "Exam1.jpg" or a C++ source file as "Project.java". Still, it's important not to bork up your filenames by accidentally giving them the wrong extension, because it's just confusing - to people and maybe to the OS.

To write or edit source code, you need a tool that can edit plain-text files. Preferably, this tool is smart enough to know what you are doing so that it can help you out. This sort of text editor is often called a *programmer's editor*. If it has enough bells and whistles, we might even call it an *IDE* (Integrated Development Environment), because then it's really much more than an editor.

Here are some valuable features that you should not live without in a modern programmer's editor. If your favorite editor cannot do these things, then find a new favorite editor. If you know it can do them, but you don't know how, then find out how.

* Undo/Redo - your editor should support many levels of undo; we make mistakes, and it should be easy to revert them.
* Spaces vs Tabs - your editor should allow you to control the level of indentation per level of block nesting as well as choose how to handle indentation (tabs or spaces - always use spaces!). Good ones can even convert all tabs to spaces in a file that has been coded by a fool.
* Syntax highlighting - the editor adjusts font styles and colors for different parts of the code to enhance readability.
* Bracket matching - the editor can visually indicate each matched pair of brackets/braces/parentheses to help programmer's find omissions or mismatches.
* Block commenting - you should be able to select a block of code/lines and have the editor (un)comment the entire block at once.
* Automatic indentation - the editor keeps track of code blocks and automatically indents as needed when starting a new line.
* Code formatting - beyond simple auto-indentation, powerful editors can also reformat your entire source file according to a set of pre-defined rules; your editor should allow you to customize these rules - if it doesn't, then find a new one; please use this feature to ensure consistent coding style.
* Autocompletion - your editor knows the names of variables and functions you've declared and can autocomplete at the touch of a key if you've given it enough to go on; for example, assuming my program has the relevant function declared, I might start typing "rend..." and then pressing the autocomplete key will fill in "renderToContext".
* Suggestions - similar to autocompletion, this feature can save you time by reducing the amount of typing you need to do; but in this case the editor has deeper knowledge of the language, modules/libraries, your other code, etc. and can present a list of suggestions automatically without even being asked; this feature can also be a huge bother and even slow down your coding.

