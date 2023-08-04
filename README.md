# Repositorio-GetStarted-(K1-T1)

Nesse repositório irei estruturar um CheatSheet para facilitar o estudo de Git.

## CheatSheet de Comandos Básicos
PS: Todas as informações entre colchetes [] são informações variáveis.

##### Configurações Locais

Configurar nome
```
    git config --global user.name "nome"
```

Configurar email
```
    git config --global user.email "[email]"
```

Visualizar lista de configurações
```
    git config --list
```

Trocar nome da branch principal no default
```
    git config --global init.defaultBranch [nome_da_branch]
```

Trocar o Vim como editor padrão para o VSCode
```
    git config --global core.editor "code --wait"
```

Trocar o Vim como editor padrão para o Sublime Text
```
    git config --global core.editor "subl --wait"
```

#### Iniciar um Repositório Local

Inicializa um repositório na pasta que está
```
    git init
```

Clona um repositório remoto para seu PC
```
    git clone [link_do_repositorio]
```

Clona um repositório local para outro repositório local
```
    git clone [nome_do_repositorio_local] [nome_do_novo_repositorio_local]
```

#### Adicionar e Remover Arquivos no Controle do Repositório

Adicionar um arquivo especifico
```
    git add [nome_arquivo]
```

Adicionar todos arquivos
```
    git add --all
    git add -a
    git add .
```

Remover um arquivo especifico
```
    git rm --cached [nome_arquivo]
```

Remover todos os arquivos
```
    git rm --cached -r .
```

#### Commitar Arquivos

Faz um commit dos arquivos adicionados
```
    git commit -m "[titulo_do_commit]"
```

Altera o título do último commit
```
    git commit --amend -m "[novo_titulo_do_commit]"
```

Commita os arquivos que faltaram utilizando o mesmo texto do commit anterior
```
    git commit --amend --no-edit
```

Abre o Vim para editar o título do commit
```
    git commit --amend
```

#### Verificando Diferenças nos Arquivos entre as Alterações

Mostra a diferença dos arquivos antes e depois das alterações feitas 
```
    git diff
```

Mostra a diferença entre arquivos staged
```
    git diff --cached
    git diff --staged
```

#### Histórico

Listagem dos commits feitos
```
    git log
```

Listagem dos commits feitos de maneira concisa
```
    git log --oneline
```

Listagem de determinada quantidade de commits
```
    git log -[quantidade]
    git log --oneline -[quantidade]
```

Listagem do histórico de alterações
```
    git log --patch
    git log -p
    git log -p -[quantidade]
```

Listagem do histórico e dos arquivos que foram alterados
```
    git log --stat
```

Listagem do histórico com a quantidade dos arquivos que foram alterados
```
    git log --shortstat
```

Listagem dos commits feitos em uma branch especifica
```
    git log [nome_da_branch]
```

#### Branch e Merge

Listagem das branches do repositório
```
    git branch
```

Cria uma nova branch
```
    git branch [nome_branch]
```

Muda de branch
```
    git checkout [nome_branch]
    git switch [nome_branch]
```

Cria uma nova branch e muda para ela
```
    git checkout -b [nome_branch]
    git switch -c [nome_branch]
```

Renomeia a branch atual
```
    git branch -m [novo_nome]
```

Renomeia uma branch
```
    git branch -m [nome_antigo] [novo_nome]
```

Mescla os arquivos de uma branch especifica com sua branch atual 
```
    git merge [nome_branch]
```

#### Pull e Push

Traz as alterações feitas no repositório remoto para seu repositório local
```
    git pull
```

Envia as alterações feitas no repositório local para o repositório remoto
```
    git push
```

#### Stash

Salva o que está sendo feito na branch atual no stash
```
    git stash
```

Lista todos os stashes que você tem salvos
```
    git stash list
```

Traz o que você havia deixado salvo no stash
```
    git stash apply
```

Traz o que você havia deixado salvo no stash e remove ele do stash
```
    git stash pop
```

Remove do stash
```
    git stash drop
```