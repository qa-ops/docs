# UNIX - Comandos básicos

## Vídeos

Todos esses comandos foram explicados, na prática, no meu canal [QaOps](http://videos.qa-ops.com/youtube
). 

* [Playlist de UNIX](https://www.youtube.com/playlist?list=PLhJTa4U57yUsKBcqWbGaAQ7QpcgzKakVe)

## Referências

* https://en.wikipedia.org/wiki/Shell_script
* https://www.tutorialspoint.com/unix/unix-file-permission.htm
* https://en.wikipedia.org/wiki/Bash_(Unix_shell)

## Comandos

### Lidando com arquivos e diretórios

* `man [COMANDO]` -> mostra o manual do comando passado
* `pwd` -> mostra o diretório atual
* `ls` -> lista conteúdo de diretório
* `ls -l` -> lista conteúdo de diretório em formato de lista
* `ls -lh` -> lista conteúdo de diretório em formato de lista e com tamanhos em Byte, Kilobyte, Megabyte, Gigabyte, Terabyte and Petabyte
* `ls -lha` -> mesma coisa do comando anterior, mais lista arquivos ocultos (arquivos com começam com ponto)
* `mkdir [DIRETÓRIO]` -> cria o diretório passado por parâmetro
* `mkdir -v [DIRETÓRIO]` -> cria o diretório passado e todas os diretórios intermediários
* `cd [DIRETÓRIO]` -> navega para o diretório passado
* `cd ..` -> sai (escapa) do diretório atual em 1 nível
* `cd ../..` -> sai (escapa) do diretório atual em 2 níveis
* `cd -` -> retorna para o último diretório acessado
* `touch [ARQUIVO]` -> cria o arquivo passado por parâmetro
* `rm [ARQUIVO]` -> deleta o arquivo passado por parâmetro
* `rm -rf [DIRETÓRIO]` -> deleta diretório com toda sua hierarquia interna sem perdir confirmação
* `echo '[TEXTO]' > [ARQUIVO]` -> escreve texto dentro do arquivo, sempre sobrescrevendo todo o arquivo 
* `echo '[TEXTO]' >> [ARQUIVO]` -> escreve texto ao final arquivo, sempre adicionando
* `cat [ARQUIVO]` -> imprime conteúdo do arquivo no terminal
* `history` -> mostra o histórico dos comandos executados
* `history | grep [CONTEÚDO_A_PROCURAR]` -> procura no histórico 
* `history | grep --color [CONTEÚDO_A_PROCURAR]` -> procura no histórico e destaca o conteúdo achado
* `cat [ARQUIVO] | grep [CONTEÚDO_A_PROCURAR]` -> procura no conteúdo de um arquivo 
* `grep [CONTEÚDO_A_PROCURAR] [ARQUIVO]` -> procura no conteúdo de um arquivo
* `cp [ARQUIVO_ORIGINAL] [NOME_DA_CÓPIA]` -> cria uma cópia do arquivo
* `cp -r [DIRETÓRIO_ORIGINAL] [NOME_DA_CÓPIA]` -> cria uma cópia do diretório
* `mv [CONTEÚDO_ORIGINAL] [CAMINHO_DESTINO]` -> move arquivos e diretórios. Também é usado para renomeiar pastas e arquivos

### Alias e bash profile

Criar o arquivo `.bashrc` dentro do seu $HOME para colocar suas configurações do terminal. Esse arquivo será executado de duas formas:
 
1. Toda vez que entrar no terminal, seja uma nova janela ou nova aba.
1. Executando o comando `source $HOME/.bashrc`

* `alias ll='ls -lh` -> cria um atalho 'll' para o comando 'ls -lh' 
* `alias grep='grep --color'` -> sobescreve o 'grep' para que ele sempre tenha a opcção '--color'
* `alias resource='source $HOME/.bashrc'` -> cria um atalho 'resource' para recarregar o arquivo '.bashrc' do $HOME.
* `alias qaops='cd $HOME/Documents/Personal/code/qaops'` -> criar alias para entrar em um diretório

## Dicas

* use a tecla TAB para autocompletar diretórios e arquivos
