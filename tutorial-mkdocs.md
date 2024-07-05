# Tutorial MKDOCS

para instalar o mkdocs é preciso ter python e pip instalado

## Instalação

$ pip install mkdocs

## Adiconar no PATH

$ nano ~/.zshrc ou $ nano ~/.zshrc 

adicionar em .bashrc ou .zshrc:

> export PATH="$HOME/.local/bin:$PATH"

$ source ~/.zshrc

## instalar thema material:

$ pip install mkdocs-material

### alternativamente:

| $ python3 -m venv venv

| $ source venv/bin/activate

| $ pip3 install -r requirements.txt 

| $ mkdocs serve

após testar e terminar:

| CTRL + C | para fechar o servidor local mkdocs,

| $ deactivate | para sair do ambiente python


## Como usar

dentro do arquivo mkdocs.yml o "nav" é a barra de navegação para do github pages. Crie um arquivo .md e refencie na nav. exemplo:

~~~
nav:
    - Home: index.md
    - Documentação:
      - Home: home.md
    - Sprints:
    - About: about.md
~~~

a partir na pasta "docs" você pode referênciar os arquivos em markdown.

## como buildar

$ mkdocs build
$ mkdocs serve

## sobre

Para mais informações de customização e estrutura do mkdocs visite:

- https://www.mkdocs.org/
- https://squidfunk.github.io/mkdocs-material/getting-started/
- https://github.com/mkdocs/catalog