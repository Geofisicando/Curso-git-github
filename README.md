# Curso-git-github

> Material de apoio do curso de Git e Github do canal Geofisicando no youtube

## Comandos básicos do Git
> Resumo dos principais comandos do Git para rápida iniciação _(quick start)_

### Configurando o GIT

* Configurando o usuário global

```shell
git config --global user.name "Nome do Usuário"

git config --gloal user.email "rodolfo_profissional@hotmail.com"
```

* Configurando o usuário local

```shell
git config user.name "Nome do Usuário"

git config user.email "rodolfo_profissional@hotmail.com"
```

```shell
git config --list # Exibir lista de variáveis configuradas
```

### Resetando os commits feitos

* Reset suave (Retorna os arquivos para a stagged area)

```shell
git reset --soft <commit>
```


* Reset misto (Retorna os arquivos para antes da stagged area)

```shell
git reset --mixed <commit>
```
* Reset forte (Apaga o commit atual e retorna para o penúltimo commit)

```shell
git reset --hard <commit>
```
* Retornar versão anterior de um arquivo

```shell
git checkout HEAD -- <file>
```

### Visualizar branch

* Atualizar branch local com branch remoto 

```shell
git pull origin <branch>
```

* Exibir os commits em uma coluna

```shell
git log --pretty=oneline
```

* Enviar atualizações do branch local para o remoto

```shell
git push origin <branch>
```

### Remover branch

* Remover branch no repositório remoto

```shell
git push origin :<branch>
```
* Remover branch no repositório local

```shell
git branch -D <branch>
```

### Adicionar tags ao commit

* Mostrar todas as tags cadastradas no repositório local

```shell
git tag
```

* Adicionar nova tag v0.1 ao commit atual

```shell
git tag -a v0.1 -m "Mensagem da tag"
```

* Mostrar tag v0.1

```shell
git show v0.1
```

* Enviar tags do repositório local para o repositório remoto

```shell
git push --tags
```

### Repositórios remotos

* Visualizar repositórios remotos atribuídos ao repositório local

```shell
git remote -v
```

* Trocar de repositório remoto HTTP para SSH. 

Após criar uma chave SSH para a sua máquina, e adicioná-la a sua
conta no github, você precisa trocar os remotos para HTTP. 
Exemplo, a saída do comando git remote -v deverá mostrar seus remotos com a comunicação via
protocolo HTTP. Assim:

```shell
git remote -v
origin	https://github.com/<User>/<remoto>.git (fetch)
origin	https://github.com/<User>/<remoto>.git (push)
```
Basta setar os remotos para protocolo SSH:

```shell
git remote set-url origin git@github.com:<User>/<remoto>.git
```

A nova saída será:

```shell
git remote -v
origin	git@github.com:<User>/<remoto>.git (fetch)
origin	git@github.com:<User>/<remoto>.git (push)
```

### Adicionar repositório local ao Github

* Depois de criar um repositório remoto vazio no site do Github com o mesmo nome do seu repositório local. 
Adicione o repositório local ao remoto com os seguintes comandos

```shell
git remote add origin https://github.com/Dirack/<nome pasta repositório>.git
git push -u origin master
```
