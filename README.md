WORKING DIRECTORY - Diretório onde estou trabalhando

STAGGING AREA/INDEX - Cópia criada após o git add 

OBJECT AREA - Diretório criado após o git commit

COMANDOS:

# Configurar usuário global
```
git config --global user.name "Fulano de tal"
```

# Configurar email global
```
git config --global user.email "fulano@hotmail.com"
```

# Inicializar repositório vazio
```
git init 
```

# Adicionar modificações para stagging area
```
git add 
```
# Adicionar modificações ao objeto
**Aqui é criado um ID para cada commit que é um hash**
*Ex.: 513141d98ccd1bd886b4445c3189cdd14275d04b*
```
    git commit -m "blabla"
```

# Verificar arquivos que foram adicionados
**Aqui é verificado arquivos que foram adicionados do working directory para a stagging area/index**

```
    git status
```

# Comando para criar branch

```
    git branch my-first-branch
```

# Comando para criar branch e se redirecionar para ela
```
    git checkout -b my-first-branch
```
```
    git switch -c my-first-branch
```

# Comando para listar branchs
```
    git branch
```

# Comando para trocar de branch
```
    git switch my-first-branch
```
```
    git checkout my-first-branch
```

# Comando para merge entre branchs
*Supondo que você esteja na branch master, as coisas que estão em my-first-branch são mescladas na master*
```
    git merge my-first-branch
```

# Comando para merge e commitar ao mesmo tempo
```
    git merge my-first-branch -m "Merge branch 'add-thurs-menu'”
```

# Comando para deletar branch
```
    git branch -d my-first-branch
```

# Comando para listar commits
*Com id do commit completo*
```
    git log
```
*Com id abreviado*
```
    git log --abbrev-commit
```
*Commit de forma resumida em uma linha só*
```
    git log --pretty=oneline
```
*Comando para ver commits em apenas uma linha com ID abreviado*
```
    git log --pretty=oneline --abbrev-commit
```
*ou apenas o shortcut*
```
    git log --oneline
```
*Arvore de commits*
```
    git log --oneline --all --graph
```

# Comando para ver diferenças entre branchs, commits, diretorios de trabalhos e etc
```
    git diff
```
*Mostra exatamente o trecho que está diferente*
```
    git diff --word-diff
```
*Comando para comparar o último commit(object db) com o index/stagging are*
```
    git diff --cached
```

# Comando para restaurar o que tá no index/stagging para o working directory

```
    git restore .
```

# Comando para restaurar o que está no index para o que está no object database
```
    git restore --staged .
```

# Comandos para deletar e renomear arquivos
*Deletar*
```
    git rm nome-do-arquivo.py
```
*Renomear*
```
    git mv nome-do-arquivo.py novo-nome-do-arquivo.py
```

# Comando para editar mensagem do ultimo commit

```
    git commit --amend -m "new message"
```

# Comando para renomear branch

```
    git branch -m new-name
```

# Comando para resetar para um commit anterior

```
    git reset "primeiros 7 numeros do hash do commit"
```
*Ou*
```
    git reset HEAD~1 ou 2 ou 3...
```

# Comando para voltar o working directory e o index/staggin para ficar igual ao object database

```
    git reset --soft
```

# Comando para voltar o que está no object database para apenas o index

```
    git reset --mixed 
```

# Comando para resetar o que está no index/stagging para o working directory e deixar os trÊs diretorios iguais

```
    git reset --hard
```

# Comando para resetar para um commit anterior
```
    git revert <nome do commit> ou HEAD
```
# Nome do repositório remoto
```
    git remote
```

# Subir branch local para repositório remoto
```
    git push -u origin local-branch
```
*Ou*
```
    git push --set-upstream origin local-branch
```

# Comando para sincronizar branches
```
    git fetch
```

# Comando para sincronizar branches e apagar as apagadas
```
    git fetch -p ou --prune
```