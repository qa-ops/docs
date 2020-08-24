# UNIX - Comandos básicos

## Vídeos

All comands were explained, in a hands on approach, in my channel QaOps(http://videos.qa-ops.com/youtube
). 

* Playlist de UNIX(https://www.youtube.com/playlist?list=PLhJTa4U57yUsKBcqWbGaAQ7QpcgzKakVe)

## Referências

* https://en.wikipedia.org/wiki/Shell_script
* https://www.tutorialspoint.com/unix/unix-file-permission.htm
* https://en.wikipedia.org/wiki/Bash_(Unix_shell)

## Commands

## Dealing with files and directories

* `man COMMAND` -> show the manual of the given command
* `pwd` -> show the current directory
* `ls` -> list directory content
* `ls -l` -> list directory content in a list format
* `ls -lh` -> list directory content in a list format and sizes as Byte, Kilobyte, Megabyte, Gigabyte, Terabyte and Petabyte
* `ls -lha` -> the same as previous command, plus show all hidden files (files that start with dot)
* `mkdir FOLDER` -> create the given directory
* `mkdir -v FOLDER` -> create the given directory along with the intermediate directories
* `cd FOLDER` -> navigate to the given directory 
* `cd ..` -> escape the current directory by 1 level
* `cd ../..` -> escape the current directory by 2 levels
* `cd -` -> go back to the previous accessed directory
* `touch FILE` -> create a file
* `rm FILE` -> delete a file
* `rm -rf FOLDER` -> remove directory along with its internal hierarchy without asking permission
* `echo 'TEXT' > FILE` -> write text in a file, always overwriting the file 
* `echo 'TEXT' >> FILE` -> write text to the end of f file, always appending
* `cat FILE` -> print the content of a file in the terminal
* `history` -> show the history of the executed commands
* `history | grep SEARCHED_CONTENT` -> search in the history 
* `history | grep --color SEARCHED_CONTENT` -> search the history and hightlights the found content
* `cat FILE | grep SEARCHED_CONTENT` -> search text in a file 
* `grep SEARCHED_CONTENT FILE` -> search text in a file
* `cp SOURCE_FILE COPY_NAME` -> create a copy of a file
* `cp -r SOURCE_FOLDER COPY_NAME` -> create a copy of a directory
* `mv SOURCE_CONTENT TARGET_PATH` -> move files and directories. Also used for renaming files an directories
* `egrep "REGEXP"` -> use extended regexp
* `egrep -V "REGEXP"` -> inverts the search, meaning that it will return everything that does not match that REGEXP
* `xargs` -> ler espaços, tabs, nova linha, e transforma em uma única string separada por um único espaço
* `git branch | egrep -v "(master|\*)" | xargs git branch -D` -> acha todas as branches que não são a 'master' ou é ativa('*'), transforma em uma única linha e passa como argumento para o 'git branch -D' para serem deletadas

### Alias and bash profile

Create a file `.bashrc` in your $HOME for your terminal setup. This file can be executed differently:
 
1. When you open a terminal, either a new window a new tab
1. By running the command `source $HOME/.bashrc`

* `alias ll='ls -lh` -> create a shortcut 'll' for the command 'ls -lh' 
* `alias grep='grep --color'` -> overwrite the 'grep' for it to always have the '--color' option
* `alias resource='source $HOME/.bashrc'` -> create a shortcut 'resource' to reload the file '.bashrc' of your $HOME.
* `alias qaops='cd $HOME/Documents/Personal/code/qaops'` -> create alias to enter a directory

### Cut e AWK

* `cat FILE | grep FILTER | cut -d DELIMITER -f1` -> Splits the String by the DELIMITER and shows the field 1
* `cat FILE | grep FILTER | cut -d DELIMITER -f2` -> Splits the String by the DELIMITER and shows the field 2
* `cat FILE | grep FILTER | cut -d DELIMITER -f2-` -> Splits the String by the DELIMITER and shows all fiels starting from the field 2
* `cat FILE | grep FILTER | awk -F DELIMITER '{print $1}'` -> Splits the String by the DELIMITER and shows the first column
* `cat FILE | grep FILTER | awk -F DELIMITER '{print $2}'` -> Splits the String by the DELIMITER and shows the second column
* `cat FILE | grep FILTER | awk -F DELIMITER '{print "First - " $1 "\nSecond-" $2 "}'` -> Splits the String by the DELIMITER and and changes how the values are displayed

### Bash Script

* `$#` -> number de arguments
* `$@` -> all arguments
* `${@:2}` -> all arguments starting from the 2º argument
* `$1` -> first argument
* `${2:-default_value}` -> use the second argument if it exists, otherwise, uses value `default_value`
* `[[ -e ARQUIVO ]]` -> verify if file exists
* `[[ STRING == STRING ]]` -> compare two strings

### Dealing with remote server

* `ssh USER@HOST` - access the HOST on port 22
* `ssh -p 2222 USER@HOST` - access the HOST on port 2222
* `ssh -o PubkeyAuthentication=no USER@HOST` - access the HOST forcing password autentication
* `scp LOCAL_FILE USER@HOST:/home/user` - copy LOCAL_FILE to the directory /home/user do servidor
* `scp USER@HOST:/home/user/file.txt .` - copy the /home/user/file.txt from the server to the current local directory
* `du -sh *` - show the total size of all files and directory where the command was executed
* `df -h` - show the disk utilization

### Terminal hints

* `TAB` - use to autocomplete directories and files
* `seta para cima | seta para baixo` - navigate through the previously executed commands
* `ctrl + r` - search for the previously executed commands
* `ctrl + a` - place the cursor at the beginning of the line
* `ctrl + b` - place the cursor at the end of the line
* `!COMMAND` - re-execute the last COMMAND
* `!HISTORY_NUMBER` - re-execute the command based on the history number