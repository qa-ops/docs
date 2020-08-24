# UNIX - Comandos básicos

## Vídeos

Todos esses comandos foram explicados, na prática, no meu canal QaOps(http://videos.qa-ops.com/youtube
). 

* Playlist de UNIX(https://www.youtube.com/playlist?list=PLhJTa4U57yUsKBcqWbGaAQ7QpcgzKakVe)

## Referências

* https://en.wikipedia.org/wiki/Shell_script
* https://www.tutorialspoint.com/unix/unix-file-permission.htm
* https://en.wikipedia.org/wiki/Bash_(Unix_shell)

## Comandos

### Lidando com arquivos e diretórios

* `man COMANDO` -> mostra o manual do comando passado
* `pwd` -> mostra o diretório atual
* `ls` -> lista conteúdo de diretório
* `ls -l` -> lista conteúdo de diretório em formato de lista
* `ls -lh` -> lista conteúdo de diretório em formato de lista e com tamanhos em Byte, Kilobyte, Megabyte, Gigabyte, Terabyte and Petabyte
* `ls -lha` -> mesma coisa do comando anterior, mais lista arquivos ocultos (arquivos com começam com ponto)
* `mkdir DIRETÓRIO` -> cria o diretório passado por parâmetro
* `mkdir -v DIRETÓRIO` -> cria o diretório passado e todas os diretórios intermediários
* `cd DIRETÓRIO` -> navega para o diretório passado
* `cd ..` -> sai (escapa) do diretório atual em 1 nível
* `cd ../..` -> sai (escapa) do diretório atual em 2 níveis
* `cd -` -> retorna para o último diretório acessado
* `touch ARQUIVO` -> cria o arquivo passado por parâmetro
* `rm ARQUIVO` -> deleta o arquivo passado por parâmetro
* `rm -rf DIRETÓRIO` -> deleta diretório com toda sua hierarquia interna sem perdir confirmação
* `echo 'TEXTO' > ARQUIVO` -> escreve texto dentro do arquivo, sempre sobrescrevendo todo o arquivo 
* `echo 'TEXTO' >> ARQUIVO` -> escreve texto ao final arquivo, sempre adicionando
* `cat ARQUIVO` -> imprime conteúdo do arquivo no terminal
* `history` -> mostra o histórico dos comandos executados
* `history | grep CONTEÚDO_A_PROCURAR` -> procura no histórico 
* `history | grep --color CONTEÚDO_A_PROCURAR` -> procura no histórico e destaca o conteúdo achado
* `cat ARQUIVO | grep CONTEÚDO_A_PROCURAR` -> procura no conteúdo de um arquivo 
* `grep CONTEÚDO_A_PROCURAR ARQUIVO` -> procura no conteúdo de um arquivo
* `cp ARQUIVO_ORIGINAL NOME_DA_CÓPIA` -> cria uma cópia do arquivo
* `cp -r DIRETÓRIO_ORIGINAL NOME_DA_CÓPIA` -> cria uma cópia do diretório
* `mv CONTEÚDO_ORIGINAL CAMINHO_DESTINO` -> move arquivos e diretórios. Também é usado para renomeiar pastas e arquivos
* `egrep "REGEXP"` -> usa regexp estendida
* `egrep -V "REGEXP"` -> inverte a pesquisa, ou seja, irá retornar tudo que não foi achado pela REGEXP
* `xargs` -> reads space, tab, newline and end-of-file delimited strings and transforms it into a single string separated by single space
* `git branch | egrep -v "(master|\*)" | xargs git branch -D` -> get all branches that are not 'master' or is an active branch ('*'), transforms the return into a single line and pass that as argumento to 'git branch -D' in order to delete all those branches

### Alias e bash profile

Criar o arquivo `.bashrc` dentro do seu $HOME para colocar suas configurações do terminal. Esse arquivo será executado de duas formas:
 
1. Toda vez que entrar no terminal, seja uma nova janela ou nova aba.
1. Executando o comando `source $HOME/.bashrc`

* `alias ll='ls -lh` -> cria um atalho 'll' para o comando 'ls -lh' 
* `alias grep='grep --color'` -> sobescreve o 'grep' para que ele sempre tenha a opcção '--color'
* `alias resource='source $HOME/.bashrc'` -> cria um atalho 'resource' para recarregar o arquivo '.bashrc' do $HOME.
* `alias qaops='cd $HOME/Documents/Personal/code/qaops'` -> criar alias para entrar em um diretório

### Cut e AWK

* `cat ARQUIVO | grep FILTRO | cut -d DELIMITADOR -f1` -> Separa a String pelo DELIMITADOR e mostra o campo 1
* `cat ARQUIVO | grep FILTRO | cut -d DELIMITADOR -f2` -> Separa a String pelo DELIMITADOR e mostra o campo 2
* `cat ARQUIVO | grep FILTRO | cut -d DELIMITADOR -f2-` -> Separa a String pelo DELIMITADOR e mostra todos os campos a partir do campo 2
* `cat ARQUIVO | grep FILTRO | awk -F DELIMITADOR '{print $1}'` -> Separa a String pelo DELIMITADOR e imprime a coluna 1
* `cat ARQUIVO | grep FILTRO | awk -F DELIMITADOR '{print $2}'` -> Separa a String pelo DELIMITADOR e imprime a coluna 2
* `cat ARQUIVO | grep FILTRO | awk -F DELIMITADOR '{print "First - " $1 "\nSecond-" $2 "}'` -> Separa a String pelo DELIMITADOR e modifica como os valores serão mostrados

### Bash Script

* `$#` -> número de argumentos
* `$@` -> todos os argumentos
* `${@:2}` -> todos os argumentos a partir do 2º argumento
* `$1` -> primeiro argumento
* `${2:-valor_padrao}` -> usa segundo argumento caso ele existe, senão, usar o valor `valor_padrao`
* `[[ -e ARQUIVO ]]` -> verifica se arquivo existe

### Lidando servidor remoto

* `ssh USER@HOST` - acessa o HOST na porta 22
* `ssh -p 2222 USER@HOST` - acessa o HOST na porta 2222
* `ssh -o PubkeyAuthentication=no USER@HOST` - acessa o HOST forçando que a autenticação por senha
* `scp ARQUIVO_LOCAL USER@HOST:/home/user` - copia o ARQUIVO_LOCAL para o diretório /home/user do servidor
* `scp USER@HOST:/home/user/arquivo.txt .` - copia o /home/user/arquivo.txt do servidor para o diretório atual local
* `du -sh *` - mostra o tamanho total de todos os arquivos e diretórios da pasta onde o comando foi executando
* `df -h` - mostra a utilização do disco.

### Dicas Terminal

* `TAB` - use para autocompletar diretórios e arquivos
* `seta para cima | seta para baixo` - navega pelos comandos previamente executados
* `ctrl + r` - pesquisa pelos comandos previamente executados
* `ctrl + a` - coloca o cursor no início da linha
* `ctrl + b` - coloca o cursor no final da linha
* `!COMANDO` - re-executa o último COMANDO
* `!NÚMERO_DO_HISTÓRICO` - re-executa o comando baseado na número da linha
