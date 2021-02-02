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