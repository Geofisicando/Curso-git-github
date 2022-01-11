# Curso de Git e Gihub
## Geofisicando (Rodolfo Dirack)

### Lista de aulas - [Vídeos do curso](https://www.youtube.com/watch?v=ZZLnlAbSDrI&list=PLLCFxfe9wkl_URgxXbZzRnhBH6neoBFjG)

Aula 01 - Como instalar o git e como fazer o primeiro commit - Olá mundo, git!  
Aula 02 - Entendendo como o git funciona e revisando alterações com git diff  
Aula 03 - Como visualizar o histórico de commits com git log  
Aula 04 - Mais opções de visualização do git log (graph, oneline, author, grep)  
Aula 05 - Criando novas branchs e fazendo merge entre elas com git branch e git merge  
Aula 06 - Como configurar seu nome de usuário e email nos commits - git config  
Aula 07 - Criar atalhos para os comandos do git e do shell no repositório git  
Aula 08 - Git commit --amend (Pt.1): Como editar uma mensagem de commit incorreta no Git  
Aula 09 - Amend e Co-authored-by (Pt.2): Corrigir conteúdo e adicionar coautores  
Aula 10 - Git rebase (Pt.1): Editar o histórico de commits no modo iterativo  
Aula 11 - Git rebase (Pt.2): Comprimir vários commits em um só com squash  
Aula 12 - Como criar uma conta no Github  
Aula 13 - Como criar um repositório no Github  
Aula 14 - Git clone: Como clonar repositórios do github para sua máquina  
Aula 15 - Criar arquivos e pastas em repositório diretamente no Github  
Aula 16 - Criar branches diretamente no Github  
Aula 17 - Oque são os três estágios do git?: working tree, staging area e HEAD  
Aula 18 - Oque são as branches do git? Oque é origin/master?  
Aula 19 - Como utilizar as tags de commits no git (Parte 1)  
Aula 20 - Como utilizar as tags de commits no git (Parte 2)  
Aula 21 - Como enviar as suas modificações e tags para o github com git push  
Aula 22 - Como baixar as suas modificações do repositório no github com git pull  
Aula 23 - Git fetch, baixar alterações do remoto sem incorporar ao branch atual  
Aula 24 - Como criar commits padronizados com commit template  
Aula 25 - Como utilizar as github issues para gerenciar seus projetos no github  
Aula 26 - Como criar novas releases no seu repositório no github (Parte 1)  
Aula 27 - Como criar novas releases no seu repositório no github (Parte 2)  
Aula 28 - Como criar um README bonitão para o seu portifólio no Github (Parte 1)  
Aula 29 - Como criar um README bonitão para o seu portifólio no Github (Parte 2)  
Aula 30 - Como hospedar o seu site pelo Github Pages?  
Aula 31 - Documentação profissional com Github Wiki (Parte 1)  
Aula 32 - Documentação profissional com Github Wiki (Parte 2)  
Aula 33 - Documentação profissional com Github Wiki (Parte 3)  
Aula 34 - Documentação profissional com Github Wiki (Parte 4)  

## Markdown

### Texto em itálico

_Estudos sobre Git e Github_  

### Texto em negrito

**Estudos sobre Git e Github**

### Texto em destaque

> Texto em destaque

> Mais um texto em destaque

### Lista não ordenada

* Item 1
* Item 2
* Item 3

### Lista não ordenada com sublistas

* Item 1
  - Sub-item 1
  - Sub-item 2
  - Sub-item 3
* Item 2
* Item 3

### Link externo

Ir para a página do [Google](https://www.google.com)

### Imagem

![Imagem do Github](https://github.com/betopinheiro1005/curso-git-github-/blob/main/github_social.png)

### Imagem com tag HTML

<img src="https://github.com/betopinheiro1005/curso-git-github-/blob/main/github_social.png" width="500">

### Lista com checkbox
#### Funções para implementar

- [ ] função somar
- [x] função subtrair
- [ ] função multiplicar

### Escrever código

#### Em linguagem C

```c
int main(void){
  printf("Hello world\n")
}
```

#### Em Python

```py
print("Hello world")
```

#### Em shell

```sh
echo "Hello world"
```

### Criar tabela

Nome | E-mail | Cargo |
---|---|---|
Roberto Pinheiro | betopinheiro1005@yahoo.com.br | Developer PHP |



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
