# UNIX - Comandos básicos

## Vídeos

Todos esses comandos foram explicados, na prática, no meu canal [QaOps](http://videos.qa-ops.com/youtube
). 

* [Playlist de UNIX](https://www.youtube.com/playlist?list=PLhJTa4U57yUsKBcqWbGaAQ7QpcgzKakVe)

## Referências

* https://en.wikipedia.org/wiki/Shell_script

## Comandos

* `man [COMANDO]` -> mostra o manual do comando passado
* `pwd` -> mostra o diretório atual
* `mkdir [PASTA]` -> cria a pasta passada por parâmetro
* `mkdir ->v [PASTA]` -> cria a pasta passada e todas as pastas intermediárias
* `cd [PASTA]` -> navega para a pasta passada 
* `cd ..` -> sai (escapa) da pasta atual em 1 nível
* `cd ../..` -> sai (escapa) da pasta atual em 2 níveis
* `cd -` -> retorna para a 
* `touch [ARQUIVO]` -> cria o arquivo passado por parâmetro
* `rm [ARQUIVO]` -> deleta o arquivo passado por parâmetro
* `rm -rf [PASTA]` -> deleta pasta e todas suas subpastas sem perdir confirmação
* `echo '[TEXTO]' > [ARQUIVO]` -> escreve texto dentro do arquivo, sempre sobrescrevendo todo o arquivo 
* `echo '[TEXTO]' >> [ARQUIVO]` -> escreve texto ao final arquivo, sempre adicionando
* `cat [ARQUIVO]` -> imprime conteúdo do arquivo no terminal
* `history` -> mostra o histórico dos comandos executados
* `history | grep [CONTEÚDO_A_PROCURAR]` -> procura no histórico 
* `history | grep --color [CONTEÚDO_A_PROCURAR]` -> procura no histórico e destaca o conteúdo achado
* `cat [ARQUIVO] | grep [CONTEÚDO_A_PROCURAR]` -> procura no conteúdo de um arquivo 
* `grep [CONTEÚDO_A_PROCURAR] [ARQUIVO]` -> procura no conteúdo de um arquivo
* `cp [ARQUIVO_ORIGINAL] [NOME_DA_CÓPIA]` -> cria uma cópia do arquivo
* `cp -r [PASTA_ORIGINAL] [NOME_DA_CÓPIA]` -> cria uma cópia da pasta
* `mv [CONTEÚDO_ORIGINAL] [CAMINHO_DESTINO]` -> move arquivos e pastas. Também é usado para renomeiar pastas e arquivos

## Dicas

* use a tecla TAB para autocompletar pastas e arquivos