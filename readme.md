# Terminal Cheatsheet

Shortcut to access this file: [LearnTerminal.com](http:/learnterminal.com)

Below is a list of terminal commands and tips I've gathered over the last little while. I will keep updating the list as I learn more. If you have any great resources or tips to add just shot me a message.

<br>

#### Table of Contents

- [General Tips](#general-tips)
- [Listing Directories & Reading Files](#listing-directories--reading-files)
- [Navigating The File System](#navigating-the-file-system)
- [Create & Delete Files & Folders](#create--delete-files--folders)
- [Move & Copy Files & Folders](#move--copy-files--folders)
- [Manipulating Files](#manipulating-files)
- [Using FTP](#using-ftp)
- [Zipping Files](#zipping-files)
- [Text to Speech & Audio](#text-to-speech--audio)
- [Computer & IP Info](#computer--ip-info)
- [Calendars & Dates](#calendars--dates)
- [Reboot or Shutdown Computer](#reboot-or-shutdown-computer)
- [Nano Editor](#nano-editor)
- [Less Common Commands](#less-common-commands)
- [Creating Custom Terminal Commands](#custom-terminal-commands--tweaks)
- Additional Resources
  - [Videos](#videos)
  - [Articles](#articles)

<br>

## General Tips

##### Autocomplete

When you start typing the name of a file of folder to autocomplete just hit the [TAB] key and it will autocomplete the name for you (as long as the file or folder exists). EX. You have a folder named 'images' and you begin typing 'ima' then hit [TAB] it will autocomplete 'images' for you.


##### Switching Between Tabs

```
Command + Shift + [
Command + Shift + ]
```


##### Placing the cursor in a specific position using mouse click:

```
option + click
```

##### Flags

The elements appended to the commands are called flags. Ex. -a, -g, -f

##### Chaining Commands

To chain multiple commands simply seperate then with a semi collon. Ex. (ls; mkdir folder)
Instead of semi collons you can also use && in between your commands.

<br>

## Listing Directories & Reading Files

Key/Command | Description
:---|:---
`cat [file]` | *Will allow you to read the contents of a file.*
`ls` | *Get a listing of the files from the current folder you're inside of*
`ls -a` | *Get a listing of the files from the current folder you're inside of + hidden files*
`ls -la` | *Detailed listing of the files from the current folder you're inside of + hidden files*
`history` | *Displays a history of your previously inputed commands.*
`history -c` | *Clears your history.*
`mdfind [file or text] -onlyin [dir]` | *Look for a file within a specific location on your computer*

<br>

## Navigating The File System

Key/Command | Description
:---|:---
`cd [folder]` |  *Change directory*
`cd ~` | *Home Directory*
`cd /` |  *Takes you to the root of your computer*
`cd ..` | *Takes you one folder back*

<br>

## Create & Delete Files & Folders

Key/Command | Description
:---|:---
`mkdir [dir]` | *Create a directory -* `[dir] [dir]` *will create multiple folders*
`touch [file]` | *Create a file*
`rm [file]` | *Remove a file*
`rm -r [dir]` | *Remove a folder*
`mv [file] [target file]` | *Rename a file*

<br>

## Move & Copy Files & Folders

Key/Command | Description
:---|:---
`mv [file or dir] [target dir]` | *This will move a folder or file to a desired location.*
`cp [dir] [target dir] -r` | *This will copy a directory to a target dir. The* `-r` *flag means recursive, or "this folder and everything in it"*

<br>

## Manipulating Files

Key/Command | Description
:---|:---
`mkfile [file size in k, m, g] [file name]` | *Create a file with any desired file size for testing. Eg.* `mkfile 1g test.txt` *- this would create a text file that's 1gb in size*
`chmod +x [file]` | *Turns a file into a executable.*

<br>

## Using FTP

Key/Command | Description
:---|:---
`ftp [url or ip]` | *Will connect you to a FTP.  To disconnect type quit*
`lcd [dir]` | *Will change the local directory once you're connected to a FTP  Example ~/Desktop will change your local directory to your desktop*
`get [file]` | *This will download a file from your FTP to your local directory*
`put [file]` | *Transfer a file from your local directory to the FTP*
`mdelete [file]` | *Delete a file from the FTP.*

<br>

## Zipping Files

Key/Command | Description
:---|:---
`zip [file or dir] [file or folder to zip]` | *Zip a file or folder*
`zip -e [file or dir] [file or folder to zip]` | *Zip a file or folder and password protect it.*
`unzip [file]` | *Unzip a file*

<br>

## Text to Speech & Audio

Key/Command | Description
:---|:---
`afplay [file]` | *Will play an audio file through Terminal.  Press* `ctrl+c` *to stop*
`say [text]` | **Will get your computer to say something*
`say -f [file]` | *Will speak the contents of that file*
`say -v ?` | *View the available voices*
`say -v [voice name]` | *Will speak whatever you write in that particular voice  To exit hit* `ctrl+c`

<br>

## Computer & IP Info

Key/Command | Description
:---|:---
`whoami` | *Shows your user name*

<br>

## Calendars & Dates

Key/Command | Description
:---|:---
`date` | *Shows you the current date*
`cal` | *Shows ou a monthly calendar.*
`cal -y` | *Shows you a yearly calendar.*
`cal -j` | *Shows you the calendar with the days numbered from Jan 1st*
`cal -y -j` | *Shows you a yearly calendar with the days numbered from Jan 1st.*

<br>

## Reboot or Shutdown Computer

Key/Command | Description
:---|:---
`sudo halt` | *Shuts down your computer.*
`sudo reboot` | *Reboots your computer.*
`sudo shutdown -h 05:00` | *This will schedule your computer to shut down at 5am.  The time is calculated in military time.*
`sudo shutdown -r 05:00` | *This will shedule your computer to reboot at 5am.  The time is calculated in military time.*

<br>

## Nano Editor

Below are some of the more common commands that you will use quite often. For a full list of commands:
- `control + G` while inside of the nano file editor
- `man nano` while inside of temrinal
- or read the [Nano Command Manual](http://www.nano-editor.org/dist/v2.2/nano.html)
<br>

Key/Command | Description
:---|:---
`nano [file]` | *Launches nano text editor. If the file exists it will open the file in Nano Editor. If the file does not exist it will create it and launch the Nano Editor.*
`control + G` | *Pulls up the nano help file*
`control + O` | *saves the file without closing it*
`control + X` | *closes the file, will ask you to save the file*
`control + T` | *while naming your file when beign saved hitting* `control + T` *will bring up a file browser that will allow you to overwrite files & navigate through your folder structure.*
`control + \` | *Find and replace.*
`control + W` | *Search*
`control + _` | *Move to a specific line.*
`control + _ control + Y` | *Move to the top of the file*
`control + _ control + V` | *Move to the bottom of the file*
`control + K` | *Erase entire line. Or cut line.*
`control + U` | *Paste the cut line.*
`control + A` | *Move to the beginning of the line*
`control + E` | *Move to the end of the line*
`control + Y` | *Move up a page.*
`control + V` | *Move down a page.*
`control + R control + T` | *Allows you to open another file and insert it's contents into the file you currently have open. This will insert the new file in the position your indicator is placed.*
    
<br>
    
## Less Common Commands

Key/Command | Description
:---|:---
`!!` | *Run the last inputed command.*
`which [app]` | *This will get you the location fo the program relative to the user's path.*
`man [command]` | *Read the manual on any particular command. Ex. man mkdir would bring up the manual for the create a directory command. To exit a manual simply hit the Q key.*
`open [file or url]` | *Will open a file or url in your default browser.*
`open -a [app]` | *Launches an application from terminal. Doesn't seem to be case sensitive. Eg. open -a finder*
`tail -f [dir]` | *This will constantly monitor a file and output it's contents whenever changes are made to your terminal window.*
`curl ipecho.net/plain; echo` | *Get your external IP address.*
`vim [file] (ex. vim index.html)` | *Launches VIM editor. For vim specific commands please see this list. If you get stuck just hit shift+z+z, that will exit the vim editor. :q to quit :q! to quit without saving :wq to write and quit :qa to quit all*
`killall [app]` | *This will force quit an application. Ex. killall Safari This will force quit Safari.  This command is case sensitive, so if you typed safari instead of Safari it wouldn't work.  If an application has multiple words simple put the name in quotes like so killall "Microsoft Lync".  You can also kill multiple processes simple by seperating them with  spaces killall Tower Terminal (This would close down the Tower.app and the Terminal.app)*
`open [dir + app]` | *Opens an application  Example of a path open /Applications/Firefox.app  This is case sensitive, and don't forget to add the .app to the end*
`top` | *View CPU usage*
`top -o cpu` | *View CPU usage sorted with the highest usage first.*
`uptime` | *Shows you how long your computer has been turned on.*
`bc` | *Launches calculator  To exit the calculator type quit*
`file [file or dir]` | *This will tell you the format of a file/folder.*
`curl [link to a file on the internet]` | *Allows you to view a file from the internet.*
`curl [link to a file on the internet] > [file name]` | *Save a file from the internet.*
`alias [function name]='[commands]'` | *This will create a function. To call it simply type the function name.  Ex. alias a='mkdir testing'; Now everytime you type a and hit enter it will create a directory called testing.*
`unalias [function name]` | *Will remove the function.*

<br>


## Custom Terminal Commands & Tweaks

If you can't find a command to do something specifit you can create your own.

1. Open up `.bashrc` with a text editor or within nano - `nano /~etc/bashrc`
2. Go to the bottom of the file and insert a comment using the hash tag and create your own function.

##### Example
###### Make a directory and directly go into it
```
mkgo(){
    mkdir $1 && cd $1
}
```

##### Remove the username + computer name from your terminal prompt:

1. Open up your `.bashrc` file by typing `sudo nano /etc/bashrc`
2. edit PS1 to be PS1='\w \$ '
3. hit `control + X' to close the file, when asked to save hit `Y` then hit enter to keep the file name the same.

<br>

## Additional Resources

### Videos

- [23 Part Video Lesson](https://www.youtube.com/user/allthingseducational/videos)
- [Navigating the Terminal: A Gentle Introduction](http://computers.tutsplus.com/tutorials/navigating-the-terminal-a-gentle-introduction--mac-3855)

### Articles

- [40 Terminal Tips and Tricks You Never Thought You Needed](http://computers.tutsplus.com/tutorials/40-terminal-tips-and-tricks-you-never-thought-you-needed--mac-51192)
- [Terminal Cheatsheet](https://github.com/0nn0/terminal-mac-cheatsheet/wiki/Terminal-Cheatsheet-for-Mac-(-basics-))
- [Command Line Fu](http://www.commandlinefu.com/commands/browse)
