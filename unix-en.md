# UNIX - Comandos básicos

## Vídeos

All comands were explained, in a hands on approach, in my channel [QaOps](http://videos.qa-ops.com/youtube
). 

* [Playlist de UNIX](https://www.youtube.com/playlist?list=PLhJTa4U57yUsKBcqWbGaAQ7QpcgzKakVe)

## Referências

* https://en.wikipedia.org/wiki/Shell_script
* https://www.tutorialspoint.com/unix/unix-file-permission.htm
* https://en.wikipedia.org/wiki/Bash_(Unix_shell)

## Comandos

## Dealing with files and directories

* `man [COMMAND]` -> show the manual of the given command
* `pwd` -> show the current directory
* `ls` -> list directory content
* `ls -l` -> list directory content in a list format
* `ls -lh` -> list directory content in a list format and sizes as Byte, Kilobyte, Megabyte, Gigabyte, Terabyte and Petabyte
* `ls -lha` -> the same as previous command, plus show all hidden files (files that start with dot)
* `mkdir [FOLDER]` -> create the given directory
* `mkdir -v [FOLDER]` -> create the given directory along with the intermediate directories
* `cd [FOLDER]` -> navigate to the given directory 
* `cd ..` -> escape the current directory by 1 level
* `cd ../..` -> escape the current directory by 2 levels
* `cd -` -> go back to the previous accessed directory
* `touch [FILE]` -> create a file
* `rm [FILE]` -> delete a file
* `rm -rf [FOLDER]` -> remove directory along with its internal hierarchy without asking permission
* `echo '[TEXT]' > [FILE]` -> write text in a file, always overwriting the file 
* `echo '[TEXT]' >> [FILE]` -> write text to the end of f file, always appending
* `cat [FILE]` -> print the content of a file in the terminal
* `history` -> show the history of the executed commands
* `history | grep [SEARCHED_CONTENT]` -> search in the history 
* `history | grep --color [SEARCHED_CONTENT]` -> search the history and hightlights the found content
* `cat [FILE] | grep [SEARCHED_CONTENT]` -> search text in a file 
* `grep [SEARCHED_CONTENT] [FILE]` -> search text in a file
* `cp [SOURCE_FILE] [COPY_NAME]` -> create a copy of a file
* `cp -r [SOURCE_FOLDER] [COPY_NAME]` -> create a copy of a directory
* `mv [SOURCE_CONTENT] [TARGET_PATH]` -> move files and directories. Also used for renaming files an directories

### Alias and bash profile

Create a file `.bashrc` in your $HOME for your terminal setup. This file can be executed differently:
 
1. When you open a terminal, either a new window a new tab
1. By running the command `source $HOME/.bashrc`

* `alias ll='ls -lh` -> create a shortcut 'll' for the command 'ls -lh' 
* `alias grep='grep --color'` -> overwrite the 'grep' for it to always have the '--color' option
* `alias resource='source $HOME/.bashrc'` -> create a shortcut 'resource' to reload the file '.bashrc' of your $HOME.
* `alias qaops='cd $HOME/Documents/Personal/code/qaops'` -> create alias to enter a directory


## Hints

* use the TAB key to autocomplete directories and files