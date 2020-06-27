# UNIX - Comandos básicos

## Vídeos

All comands were explained, in a hands on approach, in my channel [QaOps](http://videos.qa-ops.com/youtube
). 

* [Playlist de UNIX](https://www.youtube.com/playlist?list=PLhJTa4U57yUsKBcqWbGaAQ7QpcgzKakVe)

## Referências

* https://en.wikipedia.org/wiki/Shell_script

## Comandos

* `man [COMMAND]` -> shows the manual of the given command
* `pwd` -> shows the current directory
* `mkdir [FOLDER]` -> creates the given directory
* `mkdir -v [FOLDER]` -> creates the given directory along with the intermediate directories
* `cd [FOLDER]` -> navigate to the given directory 
* `cd ..` -> escapes the current directory by 1 level
* `cd ../..` -> escapes the current directory by 2 levels
* `cd -` -> goes back to the previous accessed directory
* `touch [FILE]` -> creates a file
* `rm [FILE]` -> deletes a file
* `rm -rf [FOLDER]` -> removes directory along with its internal hierarchy without asking permission
* `echo '[TEXT]' > [FILE]` -> writes text in a file, always overwriting the file 
* `echo '[TEXT]' >> [FILE]` -> writes text to the end of f file, always appending
* `cat [FILE]` -> prints the content of a file in the terminal
* `history` -> shows the history of the executed commands
* `history | grep [SEARCHED_CONTENT]` -> searches in the history 
* `history | grep --color [SEARCHED_CONTENT]` -> searches the history and hightlights the found content
* `cat [FILE] | grep [SEARCHED_CONTENT]` -> searches text in a file 
* `grep [SEARCHED_CONTENT] [FILE]` -> searches text in a file
* `cp [SOURCE_FILE] [COPY_NAME]` -> creates a copy of a file
* `cp -r [SOURCE_FOLDER] [COPY_NAME]` -> creates a copy of a directory
* `mv [SOURCE_CONTENT] [TARGET_PATH]` -> moves files and directories. Also used for renaming files an directories

## Hints

* use the TAB key to autocomplete directories and files