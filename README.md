#Before you start. Stop. Use tmux. 

Modified this script to take arguments passed on the command line. Creates a bookmarking system simmilar to what konsole or clusterssh has. 
Uses command completion on files populated with hostnames in ~/.quickssh/ to spawn ssh connections in multiple iterm(2) tabs

#Stuff to make it work. 

    mkdir ~/.quickssh/
    cp iTermQuickMultipleSSH.applescript ~/.quickssh/.quickssh.applescript
    sudo sh -c 'echo "/usr/bin/osascript ~/.quickssh/.quickssh.applescript "$@"" >  /usr/local/bin/quickssh && sudo chmod +x /usr/local/bin/quickssh'
    echo "complete -W "$(ls ~/.quickssh/)" quickssh" >> ~/.profile

#Finally, Phew.

1) Add files with lists of hostnames into ~/.quickssh. 
2) Start a new terminal and type 
    quickssh [tab] [tab]

you will see all of the files in ~/.quickssh avaliable for completion. When you run quickssh it will open all of the hostnames as diffrent ssh sessions, assumes ssh root@



## LICENSE

Free to use and modify.

## THANKS 

 - [Daniel Aguilar] (http://twitter.com/protozoo)
 - [Applescript] (http://en.wikipedia.org/wiki/AppleScript)
 - [tiagoh] (https://github.com/tiagoh)
