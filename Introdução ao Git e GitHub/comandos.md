# Comandos Básicos:

- Iniciar repositorio em branco -> git init
(dentro da pasta do projeto)

- ver o status de situação dos arquivos no índice
   git status

-  incluir arquivos ao repositorio git
    git add <file>

- incluir todos os arquivos, diretorios e subdiretorios dentro do indice
   git add .

- incluir todos os arquivos .php por exemplo
    git add *.php
- retirar um arquivo do índice
    git rm --cached <file>

- comitar
    git commit -m "sua mensagem aqui"

- ver todos os commits que ja foram realizados nesse projeto
    git log

- Desfazer alterações no arquivo
    git checkout -- <file>
- Tirar um arquivo do índice
    git reset HEAD <file>

- voltar com o commit
   git reset HEAD ~1 --hard (para voltar 1 versão e retirar o commit)

- Mostra todos os commites que ja foram realizados,
 inclusive os que foram 'arrancados com o --hard'
   git reflog

- recuperar o commit 'arrancado'
  git merge <SHA1 do commit>

- voltar com o commit para o índice
    git reset HEAD~1 --soft

- Ignorar (incluir no .gitignore)
    vim .gitignore

     - ignorando arquivos
       *.php (exemplo) *.txt

     - ignorando pastas
        teste/*

- Forçar a adição mesmo estando no .gitignore
    git add <file> -f

- O que fazer com o .gitignore?
    git add .gitignore git commit -m "Adicionando o ignore"
    Remover permanentemente todos os untracked files
   git clean -f

- Listar todos os branch
 git branch

- novo branch
  git checkout -b <nome_do_branch> 

- alternar entre os branch
   git checkout <nome do branch>

- Mandar de um branch para o master
    git rebase <nome do branch> (dentro do master)  

- Remover um branch
   git branch -d <nome do branch>

- Adicionar automaticamente os modificados e dá o commit
  git commit -a -m "Sua mensagem aki"

- Forma visual de trabalhar com o git
    gitk & 

- Mostrar todos os branch de form visual
 gitk --all &

- pegar todos os commits de um branch e agrupar em apenas um no master.
    git merge <branch> --squash (no master)

- Deleta o branch mesmo se ele estiver diferente do master
    git branch -D

- 'Remendar' o ultimo commit realizado com outras alterações
    git commit -m "sua mensagem aki" --amend

- Gerar uma tag
 git tag add <nome da tag>

-  Adicionar repositorio remoto
    git remote add origin <caminho>
    Gerar as chaves publicas e privadas
    ssh-keygen -t rsa

- Empurrar os dados para o repositorio central
    git push

- Pegar todas as atualizaçoes do repositorio
    git pull origin

- Repositorio remoto central
    git init --bare

- Clonar o repositorio central
  (dentro da pasta de destino vc digita)
    git clone c:/caminho/

## Diferença de quando usar rebase ou merge
   rebase = use no repositorio local
   merge = use no repositorio remoto 

## Configurações iniciais (Global - para todos os repositórios)

 git config --global user.name "seu nome"
 git config --global user.email "email@example.com"

## Exibir conteudo do arquivo de configuração
 cat ~/.gitconfig

## Comandos auxiliares:

- listar diretorios -> ls

- listar todos os diretorios(inclusive os ocultos) -> ls -la

- limpar a tela -> clear 

- editar um arquivo -> vim <nome do arquivo> ou vi <nome do arquivo>

- ir pelos diretorios -> cd

- saber o caminho de onde esta -> pwd
## Dicas e helps

  git help

 git <comando> --help
