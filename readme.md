# Terminal 101

Below is a list of terminal commands and tips I've gathered over the last little while. I will keep updating the list as I learn more. If you have any great resources or tips to add just shot me a message.

***

#### Table of Contents

- General Tips
    - Autocomplete

***

### General Tips

***

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

##### Remove the username + computer name from your terminal prompt:

1. Open up your .bashrc file sudo nano /etc/bashrc
2. edit your PS1 to be PS1='\w \$ '

The elements appended to the commands are called flags. Ex. -a, -g, -f

##### Navigation Map

```
/ Root
./ Current folder
../ Previous Folder
```

To chain multiple commands simply seperate then with a semi collon. Ex. (ls; mkdir folder)
Instead of semi collons you can also use && in between your commands.





***

### Commonly Used Commands

***

```
mkdir [folder name]
```
Create a directory

ls
    Get a listing of the files from the current folder you're inside of

ls -a
    Geta listing of the files from the current folder you're inside of + hidden files

ls -la
    Detailed listing of the files from the current folder you're inside of + hidden files

touch [file name]
    Create a file

rm [file name]
    Remove a file

rm -r [folder name]
    Remove a folder
    
mv [file or folder name] [location]
    This will move a folder or file to a desired location.

cat [file location]
    Will allow you to read the contents of a file.
    
    
    
    
    
Editing Files in Terminal

nano [filename]
    Launches nano text editor. ctrl+x to quit if you get stuck.
    If the file exists it will open the file in Nano Editor. If the file does not
    exist it will create it and launch the Nano Editor.

control + G
    Pulls up the nano help file

control + O
    saves the file without closing it

control + X
    closes the file, will ask you to save the file

control + T
    while naming your file when beign saved hitting control+T will
    bring up a file browser that will allow you to overwrite files & navigate
    through your folder structure.

control + \
    Find and replace.
    
control + W
    Search
    
control + C
    Find out what line the cursor is currently on.
    
control + _
    Move to a specific line.
    control + _ control + Y Move to the top of the file
    control + _ control + V Move to the bottom of the file
    
control + K
    Erase entire line. Or cut line.
    
control + U
    Paste the cut line.
    
control + A
    Move to the beginning of the line

control + E
    Move to the end of the line    
    
control + Y
    Move up a page.
    
control + V
    Move down a page.
    
control + R control + T
    Allows you to open another file and insert it's contents into
    the file you currently have open. This will insert the new file
    in the position your indicator is placed.
    
    
    

Less Common Commands

history
    Displays a history of your previously inputed commands.

history -c
    Clears your history.

!!
    Run the last inputed command.

which [program name]
    This will get you the location fo the program relative to the user's path.

whoami
    Shows your user name

man [terminal command]
    Read the manual on any particular command. Ex. man mkdir would bring up the manual for the
    create a directory command. To exit a manual simply hit the Q key.

open [file or url]
    Will open a file or url in your default browser.

open -a [application name]
    Launches an application from terminal. Doesn't seem to be case sensitive. Eg. open -a finder

mkfile [file size in k, m, g] [file name]
    Create a file with any desired file size for testing.
    Eg. mkfile 1g test.txt - this would create a text file that's 1gb in size

tail -f [file location]
    This will constantly monitor a file and output it's contents whenever changes are
    made to your terminal window.

ipconfig getifaddr en0
    Get your network ip address.

curl ipecho.net/plain; echo
    Get your external IP address.

vim [filename] (ex. vim index.html)
    Launches VIM editor. For vim specific commands please see this list.
    If you get stuck just hit shift+z+z, that will exit the vim editor.

:q to quit
:q! to quit without saving
:wq to write and quit
:qa to quit all

zip [zip name] [file or folder to zip]
    Zip a file or folder

zip -e [zip name] [file or folder to zip]
    Zip a file or folder and password protect it.

unzip [file name]
    Unzip a file

killall [application name]
    This will force quit an application. Ex. killall Safari This will force quit Safari.
    This command is case sensitive, so if you typed safari instead of Safari it wouldn't work.
    If an application has multiple words simple put the name in quotes like so killall "Microsoft Lync".
    You can also kill multiple processes simple by seperating them with
    spaces killall Tower Terminal (This would close down the Tower.app and the Terminal.app)

open [application path]
    Opens an application
    Example of a path open /Applications/Firefox.app
    This is case sensitive, and don't forget to add the .app to the end

chmod +x [file name]
    Turns a file into a executable.

sudo halt
    Shuts down your computer.

sudo reboot
    Reboots your computer.

sudo shutdown -h 05:00
    This will schedule your computer to shut down at 5am.
    The time is calculated in military time.

sudo shutdown -r 05:00
    This will shedule your computer to reboot at 5am.
    The time is calculated in military time.

top
    View CPU usage

top -o cpu
    View CPU usage sorted with the highest usage first.

uptime
    Shows you how long your computer has been turned on.

bc
    Launches calculator
    To exit the calculator type quit

date
    Shows you the current date

cal
    Shows ou a monthly calendar.

cal -y
    Shows you a yearly calendar.

cal -j
    Shows you the calendar with the days numbered from Jan 1st

cal -y -j
    Shows you a yearly calndar with the days numbered from Jan 1st.

afplay [audio file name]
    Will play an audio file through Terminal.
    Press ctrl+c to stop

say [anything you want your computer to say]
    Will get your computer to say something

say -f [file name]
    Will speak the contents of that file

say -v ?
    View the available voices

say -v [voice name]
    Will speak whatever you write in that particular voice
    To exit hit ctrl+c

file [file or folder name]
    This will tell you the format of a file/folder.

ftp [url or ip]
    Will connect you to a FTP.
    To disconnect type quit

lcd [local path]
    Will change the local directory once you're connected to a FTP
    Example ~/Desktop will change your local directory to your desktop

get [file name]
    This will download a file from your FTP to your local directory

put [file name]
    Transfer a file from your local directory to the FTP

mdelete [file name]
    Delete a file from the FTP.

curl [link to a file on the internet]
    Allows you to view a file from the internet.

curl [link to a file on the internet] > [file name]
    Save a file from the internet.

mdfind [any file name or text] -onlyin [location]
    Look for a file within a specific location on your computer

alias [function name]='[commands]'
    This will create a function. To call it simply type the function name.
    Ex. alias a='mkdir testing'; Now everytime you type a and hit enter
    it will create a directory called testing.

unalias [function name]
    Will remove the function.




Creating Custom Terminal Commands (Permanent Aliases)

If you can't find a command to do something specifit you can create your own.

1. Open up .bashrc with a text editor or within nano - nano /~etc/bashrc
2. Go to the bottom of the file and insert a comment using the hash tag and create your own function.

Example
# Make a directory and directly go into it
mkgo(){
    mkdir $1 && cd $1
}




Additional Resources

https://www.youtube.com/user/allthingseducational/videos

http://computers.tutsplus.com/tutorials/40-terminal-tips-and-tricks-you-never-thought-you-needed--mac-51192

http://www.commandlinefu.com/commands/browse
