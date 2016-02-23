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

## Pre-installation checks

1. Is my operating system 32-bit or 64-bit? 

* Windows 7:
	1. Open System by clicking the Start button, right-clicking "Computer," and then clicking "Properties"
	2. The Properties sceen will show "System type: 64-bit operating system" or "32-bit operating system."
* Mac OS (this should be less relevant for Mac users, but just in case):
	1. Click on the Apple logo in the top menu and open "About this Mac"
	2. Click "System Report" or "More Info"
	3. In the "Hardware Overview" section you should see a processor listed -- unless you have an Intel Core Solo or an Intel Core Duo, you have a 64-bit OS.
	
## Text Editors:

### Install Sublime Text (as opposed to TextEdit or Notepad):

1. Open a web browser and go to [https://www.sublimetext.com](https://www.sublimetext.com)
2. Scroll down to the button that says "Download for (your operating system)". Make sure you're installing version 3 of Sublime Text. If you don't see a button, click the "Download" link at the top of the page.

* Windows 7

1. Click "Save file" to download the Sublime Text .exe file.
2. Double-click on the .exe file to run it and begin the installation process.
3. When you get to the screen "Select Destination Location" make a note of where Sublime Text 3 is being installed (e.g., ```C:\Program Files\Sublime Text 3```)
4. Complete installation using the install wizard.
5. To open, go to Start > All Programs > Sublime Text 3.

* Mac OS

1. Click to download the Sublime Text .dmg file
2. Double-click on the .dmg file to start installation
3. When the Sublime Text window opens, drag the Sublime Text logo into the Applications folder
4. After closing the window and ejecting the disk image from your desktop, go to your Applications folder and open Sublime Text 3

### Open a Markdown (.md) file in your text editor

1. Go to the workshop GitHub repository at [https://github.com/mkudzia/c4l-workshop-2016](https://github.com/mkudzia/c4l-workshop-2016). (Files will be available on a flash drive in case there are problems with the Internet connection at the workshop.)
2. Click "Download ZIP" to download the files. 
3. Unzip the files to a folder on your desktop or another location that's easy for you to find and type. We'll refer to this folder as the "workshop files directory."
4. In the workshop files directory, right click on "outline.md" and select "Open with Sublime Text."


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
10. To move a file into the directory, move down one directory using ```cd ..``` and then type:
```
cp copy_file directory_name/copy_file
```
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
4. 
5. Verify that you've installed python: open the command line and type ```python --version```
5. Advanced step: installing pip?

### Windows:
4. **TODO: Robin what are these steps?**
5. Verify that you've installed python: open the command line and type ```python --version```
5. Advanced step: installing Ruby or JDK? **TODO: What about installing Git, nano, or pip?**

## Environment Variables:
### Mac: Adding JDK to PATH **TODO: Megan change? Amend instructions so that JDK stuff is optional (because they may not have it), and have them just update their path for Python3***
1. Open a Terminal window (if you want to open a new one, you can click on it in your dock and hold until a menu pops up, then choose "New Window")
2. Type ```echo $JAVA_HOME``` to find out where the "home" directory of your JDK version is. It will probably look something like:

```
/Library/Java/JavaVirtualMachines/jdk1.8.0_60.jdk/Contents/Home
```
3. Copy and paste that line of text into a text editor, or write it down
4. Type ```cat ~/.bash_profile``` to see if you already have a .bash_profile set up. 
	* If you do, you should see what's in it
	* If you don't, that's ok! Type ```touch ~/.bash_profile``` to create one, then type ```sudo nano ~/.bash_profile``` to edit it (you'll need to enter your computer password when prompted)
5. To add that location to your PATH, type this into your bash profile:

```
export JAVA_HOME="$(/usr/libexec/java_home -v 1.8)"
```
NOTE: the number after the -v should match the number after jdk that you copied and pasted from the previous command
### Mac bonus: Updating your PATH to include Python 3.5
1. Open a Terminal window (if you want to open a new one, you can click on it in your dock and hold until a menu pops up, then choose "New Window")
2. Assuming you have a .bash_profile from the last step, type ```sudo nano ~/.bash_profile``` 
3. You may see something like: "export JAVA_HOME=$(/usr/libexec/java_home)" -- if so:
	* Copy what you find
	* Exit (type "ctrl-x" and then hit enter)
	* Type ```touch .bash_profile.pysave``` and then paste the copied message from your original bash profile 
	* Exit the pysave bash profile (type "ctrl-x" and then hit enter)
4. Go back to .bash_profile (```sudo nano ~/.bash_profile```) and add the following text:
```
# Setting PATH for Python 3.5
# The original version is saved in .bash_profile.pysave
PATH="/Library/Frameworks/Python.framework/Versions/3.5/bin:${PATH}"
export PATH
```
5. Exit using "ctrl-x"
6. That's it!

### Windows: Adding Sublime text to PATH

### Windows bonus: Updating your PATH to include Python 3.5

## Running a Virtual Environment in VirtualBox:
### Mac
1. Install VirtualBox -- see the following link: [https://www.virtualbox.org/wiki/Downloads](https://www.virtualbox.org/wiki/Downloads)
2. Choose the option for "VirtualBox 5.0.14 for OS X hosts" and click the link that says "amd64" to download
3. Save the .dmg file somewhere you'll be able to find it again (Desktop, Downloads, etc.)
4. Double-click the file when it's finished downloading to start the install process
5. In the pop-up window, follow the instructions and double-click on the .pkg icon
6. Follow the install wizard steps and input your password when it asks for one
7. Close the installer window and eject the "VirtualBox" drive image you see on your desktop (you want to run the version you installed in your "Applications" folder just now)

### Windows
1. Install VirtualBox -- see the following link: [https://www.virtualbox.org/wiki/Downloads](https://www.virtualbox.org/wiki/Downloads)
2. Choose the option for "VirtualBox 5.0.14 for Windows hosts" and click the link that says "x86/amd64" to download
3. Save the .exe file somewhere you'll be able to find it again (Desktop, Downloads, etc.)
4. Double-click the file when it's finished downloading to start the install process
5. **TODO: Robin flesh out**

## Wrap-Up:
* You can do it! Go forth and code workshop!
