# Outline
This workshop is designed to help you set up your laptop so that you can more easily participate in code workshops. To this end, we’re going to cover:

1. Text Editors
2. The Command Line (the basics)
3. Programming Languages
4. Environment Variables
5. Virtual Environments

**TODO: maybe remove? it seems like we don't need this?** We’ll be using an fictional example throughout the workshop; for our purposes, our example character will be Elizabeth Bennet (from Jane Austen’s Pride and Prejudice). Because we like Jane Austen, and her writings are off copyright :)

## Intro:
* Who are you?
* Who are we?
* What are we all doing here?

## Text Editors:
Installing Sublime Text (as opposed to TextEdit or Notepad):

1. Open a web browser and go to [https://www.sublimetext.com](https://www.sublimetext.com)
2. You should be able to scroll down to find a blue button that's labeled "Download for (your operating system)"
3. If you don't see a button, click the "Download" link at the top of the page
4. If you're on a Mac, choose the "OS X" link; if you're on a Windows machine, choose the relevant windows link.
	* If you're not sure whether you need the 64-bit version, **TODO: Robin help**

## The Command Line:
To start working with the command line: **TODO: update based on Robin's sample directories**
### Mac:
1. Use Launchpad, or open a Finder window and choose "Applications," then locate the program called "Terminal" (you should find it under "Utilities")
2. To find out what directory you're in, type ```pwd```
3. To find out what's _in_ that directory (i.e. where you can go from here), type ```ls``` (for "list")
4. To move to another directory:
	* If you just want to move up one directory, type ```cd Desktop``` and then type ```ls``` again
	* If you want to move up several directories, type ```cd Desktop/your_folder_name```
	* IMPORTANT SAFETY TIP: If your directory or file name has spaces in it, Terminal will not let you navigate to or open it.
5. If you want to re-use a command you just typed, hit the up arrow to cycle back through previously typed commands
6. If you want to auto-complete a directory or filename, hit tab after you've typed part of the name
7. If you want to go back to the "bottom" directory, type ```cd``` with nothing after it
8. If you just want to go back "down" one directory, type ``` cd ..```
9. To make a new directory, type ```mkdir directory_name```
10. To move a file into the directory, move down one directory using ```cd ..``` and then type ```cp copy_file directory_name/copy_file```
11. To read the contents of a file without editing it, type ```cat filename```
12. To edit a file:
	* Type ```nano filename```
	* Use the arrow keys to navigate the file; make changes **TODO: text files from Robin**
	* To save and exit, type "ctrl + x" and then hit "enter"

### Windows:

## Installing a Programming Language: Python 3.5.1

1. Open a web browser and go to [https://www.python.org/downloads/](https://www.python.org/downloads/)
2. Click "Download Python 3.5.1"
3. Save the .pkg (mac) or .exe (windows) file to someplace you'll be able to find it (i.e. Downloads, Desktop)

### Mac:
4. **TODO: Get mac volunteer**
5. Advanced step: installing Blacklight? Angular?

### Windows:
4. **TODO: Robin what are these steps?**
5. Advanced step: installing Ruby or JDK?

## Environment Variables:
### Mac: Adding Python 3.5 to PATH
### Windows: Adding Python 3.5 to PATH

### Mac bonus: Adding JDK to PATH
### Windows bonus: Adding Sublime text to PATH

## Running a Virtual Environment in VirtualBox:
**TODO Megan for serious get cracking**
Catmandu stuff?

## Wrap-Up:
* You can do it! Go forth and code workshop!

/var/lib/tomcat7/webapps/fedoragsearch/WEB-INF/classes/fgsconfigGinal/index/FgsIndex
