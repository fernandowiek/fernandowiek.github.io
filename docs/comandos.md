Comandos
========

Git conta com vários comandos, a lista completa se encontra em
/lib/git-core.

Para mais detalhes do que como cada um opera pode utilizar

```
man git commando
git commando --help

```

Init
----

Para inicializar um projeto git

São criados arquivos na pasta .git com os
dados versionados.

```
git init $DIRETORIO

```

Para uma lista dos arquivos criados pelo git:

```
cd /tmp
git init foo
find .
```

Add
---

Git add adiciona arquivos a uma área temporária
para compor um commit (staging).

```
git add $ARQUIVO|$DIRETORIO
```


Git tem 3 áreas de armazenamento.

 - Staging (index)
 - Repositório Local
 - Repositório Remoto

![Comandos de trasporte e áreas de armazenamento](git-transport.png)

Commit
------

Cada mudança no histórico de um projeto é representado por um
commit. `git show` mostra o  último commit.

Para uma lista completa dos commits use: `git log`.

```
git commit
```

O commit transfere as informações para o repositório local.

Patch
-----

Patches são mudanças que podem ser transferidas de um repositório
para outro:

Para criar um patch do último commit:

```
git format-patch master

```

Para aplicar um patch:

```
curl -L https://goo.gl/p1LEc7 -o 0001-historia.patch
git apply 0001-historia.patch
```

Branches
--------

Uma branch é uma linha de trabalho independente. Podem ser usadas para
diversos propósitos.

Pode-se ter uma branch para:
 - experimentar uma tecnologia nova
 - uma branch para um bug-fix
 - outra para o trabalho do sprint


A branch padrão no git é a `master`


```
git branch #comando para gerenciar branches
```

```
git commit "informações sobre branches no master"
git checkout -b "recursos_adicionais"
git "recursos_adicionais"
touch docs/recursos_adicionais.md
```


