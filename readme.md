# Configuração de usuário

## Nome de usuário
```bash
$ git config --global user.name "Luiz Filipy"
```

## Email do usuário
```bash
$ git config --global user.email "luizfilipy.aa@outlook.com"
```

## Listando as configurações do git
```bash
$ git config --list
```

# Historico dos commits

```bash
$ git log --oneline
```

# Vendo commits anteriores

```bash
$ git checkout <id-do-commit>
```

### Para voltar no ultimo commit
```bash
$ git checkout master
```

### Para voltar no ultimo commit (arquivo - serve tambem caso o arquivo tenha sido excluido acidentalmente)
```bash
$ git checkout <arquivo>
```

### Para voltar no ultimo commit (todos os arquivos de uma só vez - serve tambem caso os arquivos tenham sido excluidos acidentalmente)
```bash
$ git reset --hard
```

# arquivos não rastreados

### Removendo arquivos não rastreados
```bash
$ git clean -f
```

# Definindo um alias
```bash
$ git config --global alias.<alias-escolhido> <comando>
```

## Removendo um alias
```bash
$ git config --global --unset alias.<alias-escolhido>
```

# Ver todas as urls dos repositorios
```bash
$ git remote -v
```

# Manipulando branches

## Listando todas as branches
```bash
$ git branch
```

## Criando uma branch
```bash
$ git branch <branch>
```

## Trocando de branch
```bash
$ git checkout <branch>
```

## Criando uma branch e trocando para a mesma simultaneamente
```bash
$ git checkout -b <branch>
```

## Enviando uma brach para o servidor
> **\<branch\>** a branch precisa ser cria no servidor para poder então envia-la da máquina local para o servidor 

```bash
$ git push --set-upstream origin <branch>
```

##### Versão reduzida
```bash
$ git push -u origin <branch>
```

## Atualizando o repositorio local com as alterações que estão no sevidor
```bash
$ git pull
```

## Removendo branch (localmente)

> Não é possivel apagar a branch ativa

```bash
$ git branch -d <branch>
```

##### Forçando a exclusão da branch
```bash
$ git checkout -D <branch>
```

## Removendo branch (no servidor)
```bash
$ git push --delete origin <branch>
```

## Renomeando branch

```bash
$ git branch -m <branch-alvo> <branch-novo-nome>
```
<br>

> Irá renomear sua branch que está ativa

```bash
$ git branch -m <branch>
```

> Para "renomear" no servidor é preciso apagar (antes disso verificar se a branch a ser apagada sofreu alterações) a branch com o nome antigo, criar a branch com o novo nome e enviar a branch com o novo nome para o servidor.

## Mesclando branch

> Irá trazer as mudanças da **\<branch\>** para a branch atual.

```bash
$ git merge <branch>
```

# Tags

## Criando tags
```bash
$ git tag -a <tag> -m "<mensagem>"
```

## Listando tags
```bash
$ git tag
```

## Enviando tag para o repositorio remoto
```bash
$ git push origin <tag>
```

## Usando tag
```bash
$ git checkout <tag>
```

## Removendo tag

#### Localmente
```bash
$ git tag -d <tag>
```

#### No servidor
```bash
$ git push --delete origin <tag>
```

## Criando tag em commit especifico

> Para criar uma tag em um commit especifico use `git checkout` e depois crie a tag.

```bash
$ git tag -a <tag> -m "<mensagem>"
```

##### Outra forma
```bash
$ git tag -a <tag> <sha-commit>
```

# Guardando mudanças na memoria

```bash
$ git stash
```

##### ou
```bash
$ git stash save "<mensagem>"
```

## Listando as mudancas

```bash
$ git stash list
```

## Usando stash

> `git stash apply` sempre pega o stash mais recente

```bash
$ git stash apply
```

> Pega o mais recente stash e o remove

```bash
$ git stash pop
```

> Pega um stash especifico e o remove

```bash
$ git stash pop stash@{<numero-stash>}
```

## Removendo stash
```bash
$ git stash drop stash@{<numero-stash>}
```
