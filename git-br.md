# GIT CLI

## Vídeos

All comands were explained, in a hands on approach, in my channel QaOps(http://videos.qa-ops.com/youtube
). 

* Playlist de UNIX(https://www.youtube.com/playlist?list=PLhJTa4U57yUsKBcqWbGaAQ7QpcgzKakVe)

## Referências

* https://git-scm.com/docs

## Comandos

* `git clone <repo_url>` - clonar Repositório.    
* `git add <arquivo>` - adiciona arquivo no índice (staging) para o próximo commit. 
* `git add -all` - adiciona todos os arquivos encontrados na árvore de trabalho ao índice (staging).
* `git add -p` - interativamente adiciona pedaços das alterações ao índice (staging).    
* `git commit` -  cria um novo commit com o conteúdo do índice (staging) com uma mensagem de descrição.
* `git commit -m 'mensagem de commit'` - cria um commit já com a mensagem.
* `git status` - mostra o estado da árvore de trabalho.     
* `git push` - atualiza o repositório remoto com todos os commits locais. 
* `git pull` - pega as modificações no repositório remoto.
* `git branch` - lista todos os branches locais.
* `git branch <nome>` - cria um novo branch.
* `git checkout` - alterna entre os branches ou restaura arquivos da árvore de trabalho.
* `git checkout -b {branch}` - cria um novo branch e já alterna para ele.
* `git diff` - mostra diferenças entre commits, árvores de trabalho e etc. 
* `git revert` - reverte um commit. 
* `git log` - mostra o histórico de commits.
* `git log --grep='<descrição>'` - pesquisa commits pela descrição.
* `git merge <branch>` - faz o merge da branch atual com a branch passada como parâmetro
