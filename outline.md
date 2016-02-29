# Outline
This workshop is designed to help you set up your laptop so that you can more easily participate in code workshops. To this end, we’re going to cover:

1. Text Editors
2. The Command Line (the basics)
3. Programming Languages
4. Environment Variables
5. Virtual Environments

We’ll be using an fictional example throughout the workshop; for our purposes, our example character will be Elizabeth Bennet (from Jane Austen’s Pride and Prejudice). Because we like Jane Austen, and her writings are off copyright :)

## Intro:
* Who are you?
* Who are we?
* What are we all doing here?

## Getting the workshop files on your computer

1. Go to the workshop GitHub repository at [https://github.com/mkudzia/c4l-workshop-2016](https://github.com/mkudzia/c4l-workshop-2016). (Files will be available on a flash drive in case there are problems with the Internet connection at the workshop.)
2. Click "Download ZIP" to download the files. 
3. Unzip the files to a folder on your desktop or another location that's easy for you to find and type. You can rename the folder or keep it named "c4l-workshop-2016".

## Pre-installation check
Is my operating system 32-bit or 64-bit? 

### Windows 7:
	1. Open System by clicking the Start button, right-clicking "Computer," and then clicking "Properties"
	2. The Properties sceen will show "System type: 64-bit operating system" or "32-bit operating system."
### Mac OS (this should be less relevant for Mac users, but just in case):
	1. Click on the Apple logo in the top menu and open "About this Mac"
	2. Click "System Report" or "More Info"
	3. In the "Hardware Overview" section you should see a processor listed -- unless you have an Intel Core Solo or an Intel Core Duo, you have a 64-bit OS.
	
## Text Editors:

### Install Sublime Text (as opposed to TextEdit or Notepad):

1. Open a web browser and go to [https://www.sublimetext.com](https://www.sublimetext.com)
2. Scroll down to the button that says "Download for (your operating system)". Make sure you're installing version 3 of Sublime Text. If you don't see a button, click the "Download" link at the top of the page.

#### Mac OS

1. Click to download the Sublime Text .dmg file
2. Double-click on the .dmg file to start installation
3. When the Sublime Text window opens, drag the Sublime Text logo into the Applications folder
4. After closing the window and ejecting the disk image from your desktop, go to your Applications folder and open Sublime Text 3

#### Windows 7

1. Click "Save file" to download the Sublime Text .exe file.
2. Double-click on the .exe file to run it and begin the installation process.
3. When you get to the screen "Select Destination Location" make a note of where Sublime Text 3 is being installed (e.g., ```C:\Program Files\Sublime Text 3```)
4. Complete installation using the install wizard.
5. To open, go to Start > All Programs > Sublime Text 3.

### Everybody: Open a Markdown (.md) file in your text editor

Mac:

Windows:
1. In the ```c4l-workshop-2016``` workshop files directory, right click on "outline.md" and select "Open with Sublime Text."


## The Command Line

Note: these instructions will say to "enter" commands. This means to type the command and then press the Enter button.

Command Line "Cheatsheets"
* Mac:
* Windows: http://www1.cs.columbia.edu/~sedwards/classes/2015/1102-fall/Command%20Prompt%20Cheatsheet.pdf

### Mac Command Line

1. Open the command line interface (CLI)
  * Use Launchpad, or open a Finder window and choose "Applications," then locate the program called "Terminal" (you should find it under "Utilities")

2. The command prompt
  * Each time you see the command prompt, it lets you know that you can give your computer instructions. Text without a command prompt is "output" (the responses from your computer).
  * In MacOS, the command prompt will look like: `megans-computer:~ username$` 

3. Find where you are (your current path) in the file system (the hierarchy of all the files on your computer)
  * Enter ```pwd``` (for "print working directory").
  * This will print your current directory.
  * Enter ```ls```. This will list everything that's in your currrent directory (files and other directories).
  
4. Navigate to the workshop folder (if you saved it on yoru Desktop)
  * Type "cd Desktop" to change the current directory to the Desktop. Your file path and command prompt will update to `megans-computer:Desktop username$`
  * View a list of directories on your desktop by entering "ls" again.
  * Continue to the workshop sample files directory by entering "cd gr4ww"
  
  Navigation Tips:
  * If you don't want to type the whole name of a directory, type a few characters and press the Tab button to autocomplete a unique file name.
  * To move up several directories, type `cd Desktop/your_folder_name`
  * If your directory or file name has spaces in it, you will get an error if you include the space as-is. 
    * You can "escape" the space (tell the computer to ignore it) by adding a backslash in front of the space: `cd Desktop/Your\ Folder/`. 
	* Alternatively, you can enclose the folder name in double quotes: `cd Desktop/"Your Folder"/`
  * To re-use a command you just typed, hit the up arrow to cycle back through previously typed commands. 
  * To auto-complete a directory or filename, hit Tab after you've typed part of the name.
  * To go back to the "top" or left-most directory in the path, type `cd` with nothing after it
  * To go back "up" one directory, type `cd ..`
  
5. Create a new directory
  * In the gr4ww directory, enter `mkdir letters`.
  * Check for your directory by entering `ls`.

6. Move files to your new directory
  * Change to the excerpts directory by typing `cd excerpts`
  * Move the first letter file into the letters directory by entering `mv letter01.txt ..\letters\`
    * The backslash at the end of "letters" tells the computer that you are moving the file into a sub-directory.
    * The two periods direct the computer to move up one directory before looking for the directory you specify.
    * You can also copy a file instead of moving it. Enter `cp letter02.txt ..\letters\`

7. Rename a file
  * There's an underscore in the "letter_03.txt" file name, which isn't consistent with the other files. Let's rename it!
  * In the excerpts directory, enter 

8. Read a file in the command line
  * In the excerpts directory, enter `cat letter06.txt`
  * The text of the letter will display as output on the command line and your prompt will return.

9. Open a file in a text editor from the command line
  * Type `nano letter06.txt`
  * Use the arrow keys to navigate the file; make changes **TODO: text files from Robin**
  * To save and exit, type "ctrl + x" and then hit "enter"

### Windows Command Line

1. Open the command line interface (CLI)
  * Click the Start Button. 
  * In the search box, enter `cmd`

2. The command prompt
  * Each time you see the command prompt, it lets you know that you can give your computer instructions. Text without a command prompt is "output" (the responses from your computer).
  * In Windows, the initial command prompt will look like "C:\Users\Elizabeth>" (where "Elizabeth" is your Windows user name). When you open the command line interface, you will start in your "home directory." 

3. Find where you are (your current path) in the file system (the hierarchy of all the files on your computer)
  * Enter `echo %cd%`.
  * This will print the path of your current directory.
  * Enter `dir`. This will list everything that's in your currrent directory (files and other directories).

4. Navigate through folders (directories)
  * Enter `cd Desktop` to change the current directory to the Desktop. Your file path and command prompt will update to "C:\Users\Username\Desktop."
  * View a list of directories on your desktop by entering `dir` again.
  * Continue to the workshop sample files directory by entering `cd gr4ww`
  * If you don't want to type the whole name of a directory, type a few characters and press the `Tab` button to autocomplete a unique file name.

5. Create a new directory
  * In the gr4ww directory, enter `mkdir letters`.
  * Check for your directory by typing `dir`.

6. Move files to your new directory
  * Change to the excerpts directory by entering `cd excerpts`
  * Move the first letter file into the letters directory by entering `move letter01.txt ..\letters\`
    * The backslash at the end of "letters" tells the computer that you are moving the file into a sub-directory.
    * The two periods direct the computer to move up one directory before looking for the directory you specify.
    * You can also copy a file instead of moving it. Enter `copy letter02.txt ..\letters\`

7. Rename a file
  * There's an underscore in the "letter_03.txt" file name, which isn't consistent with the other files. Let's rename it!
  * In the excerpts directory, enter `ren letter_03.txt letter03.txt`

8. Read a file in the command line
  * In the excerpts directory, enter `type letter06.txt`
  * The text of the letter will display as output on the command line and your prompt will return.

9. Open a file in a text editor from the command line
  * To open a text file in your default text editor, enter only the file name: `letter06.txt`

## Installing a Programming Language: Python 3.5.1
### Everbody:
1. Open a web browser and go to [https://www.python.org/downloads/](https://www.python.org/downloads/)
2. Click "Download Python 3.5.1"
3. Save the .pkg (mac) or .exe (windows) file to someplace you'll be able to find it (i.e. Downloads, Desktop)

### Mac:
4. 
5. Verify that you've installed python: open the command line and type `python --version`
5. Advanced step: installing pip?

### Windows:
4. **TODO: Robin what are these steps?**
5. Verify that you've installed python: open the command line and type `python --version`
5. Advanced step: installing Ruby or JDK? **TODO: What about installing Git, nano, or pip?**

## Environment Variables:
### Mac: Adding JDK to PATH **TODO: Megan change? Amend instructions so that JDK stuff is optional (because they may not have it), and have them just update their path for Python3***
1. Open a Terminal window (if you want to open a new one, you can click on it in your dock and hold until a menu pops up, then choose "New Window")
2. Type `echo $JAVA_HOME` to find out where the "home" directory of your JDK version is. It will probably look something like:

```
/Library/Java/JavaVirtualMachines/jdk1.8.0_60.jdk/Contents/Home
```
3. Copy and paste that line of text into a text editor, or write it down
4. Type `cat ~/.bash_profile` to see if you already have a .bash_profile set up. 
	* If you do, you should see what's in it
	* If you don't, that's ok! Type `touch ~/.bash_profile` to create one, then type `sudo nano ~/.bash_profile` to edit it (you'll need to enter your computer password when prompted)
5. To add that location to your PATH, type this into your bash profile:

```
export JAVA_HOME="$(/usr/libexec/java_home -v 1.8)"
```
NOTE: the number after the -v should match the number after jdk that you copied and pasted from the previous command
### Mac bonus: Updating your PATH to include Python 3.5
1. Open a Terminal window (if you want to open a new one, you can click on it in your dock and hold until a menu pops up, then choose "New Window")
2. Assuming you have a .bash_profile from the last step, type: `sudo nano ~/.bash_profile`
3. You may see something like: "export JAVA_HOME=$(/usr/libexec/java_home)" -- if so:
	* Copy what you find
	* Exit (type "ctrl-x" and then hit enter)
	* Type `touch .bash_profile.pysave` and then paste the copied message from your original bash profile 
	* Exit the pysave bash profile (type "ctrl-x" and then hit enter)
4. Go back to .bash_profile (`sudo nano ~/.bash_profile`) and add the following text:
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
