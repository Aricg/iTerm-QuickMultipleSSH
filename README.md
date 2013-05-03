Modified this script to take arguments passed on the command line. Creates a bookmarking system simmilar to what konsole or clusterssh has. 
Uses command completion on files populated with hostnames in ~/.quickssh/ to spawn ssh connections in multiple iterm(2) tabs

#Stuff to make it work. 

    mkdir ~/.quickssh/
    cp iTermQuickMultipleSSH.applescript ~/.quickssh/.quickssh.applescript
    sudo sh -c 'echo "/usr/bin/osascript ~/.quickssh/.quickssh.applescript "$@"" >  /usr/local/bin/quickssh && sudo chmod +x /usr/local/bin/quickssh'
    echo "complete -W "$(ls ~/.quickssh/)" quickssh" >> ~/.profile

#Finally, Phew.

Add files with lists of hostnames into ~/.quickssh
start a new terminal and type quickssh [tab] [tab]
you will see all of the files in ~/.quickssh avaliable for completion
when you run quickssh it will open all of the hostnames as diffrent ssh sessions, assumes ssh root@


--- FROM OLD README ---

## LICENSE

Just feel free to use it and modify it! 

## THANKS 

 - [Daniel Aguilar] (http://twitter.com/protozoo), who developed an original script that allowed me to improve it. 
 - [Applescript] (http://en.wikipedia.org/wiki/AppleScript), that old-crappy language widely bad documented in a lot of 90's websites.
