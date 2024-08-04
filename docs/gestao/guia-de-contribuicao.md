# Guia de Contribuição

Este é o guia de contribuição para o projeto **2024.1-SENTINELA**. Antes de iniciar qualquer desenvolvimento que contribua para esse projeto, ler esse documento é essencial para o entendimento das regras.

As contribuições podem ser iniciadas a partir das [issues](https://github.com/fga-eps-mds/2024.1-SENTINELA-DOC/issues) já definidas.

## Como contribuir

Índice:

1. [Como criar uma issue](#politica-de-issues)
2. [Como criar sua branch](#politica-de-branches)
3. [Regras de commits](#politica-de-commits)
4. [Regras de um PR](#politica-de-pull-requests)

## Politica de issues

As issues devem ser criadas no [repositório de documentação do projeto](https://github.com/fga-eps-mds/2024.1-SENTINELA-DOC).

As issues do projetos devem ser completas e explicativas, seguindo o template de issue do repositório.

As issues devem conter:

- Um título conciso e descritivo;
- Uma descrição que deve incluir uma descrição completa da issue e suas tarefas;
- Em caso de História de Usuário, descrever de maneira clara e detalhadas os criterios de aceitação, assim como adicionar o prótitpo navegável do fluxo em questão;
- Ao menos um _Assignee_ responsável pela issue;
- [_Labels_](#labels);
- _Milestone_ (sprint) em que a issue espera ser concluiída;
- _Estimated_ (pontuação) atribuida a issue;

### Labels

Na criação de uma issue, devem ser usados os rótulos abaixo para classifcá-la:

- Bug: indica um problema ou comportamento inesperados
- UX: indica que a issue é referente a práticas de _User Experience_
- Treinamento: indica que a issue é sobre treinamentos (dojos)
- Hotfix (cor #d73a4a): indica uma correção de defeitos críticos
- Docs (cor #0075ca): indica a aplicação de melhorias ou adições à documentação do projeto
- Feature (cor #094EF2): indica a introdução de uma funcionalidade nova US (cor #BE71F6): indica que a issue é uma história de usuário (user story)
- Frontend (cor #56384A): Indica que está relacionada ao frontend da aplicação
- Backend (cor #95BDC7): Indica que está relacionada ao backend da aplicação
- Arq (cor #0D5571): indica mudanças na arquitetura da aplicação ou de um de seus módulos ou serviços
- Devops (cor #9014A0): indica mudanças na esteira de integração e disponibilização contínua
- Analytics (cor #12477F): indica mudanças nos analisadores estáticos
- Easy (cor #C5DEF5): indica que a issue tem uma dificuldade baixa
- Medium (cor #BFD4F2): indica que a issue possui um grau médio de dificuldade
- Hard (cor #D4C5F9): indica que a issue possui um alto grau de dificuldade
- EPS #006633: indica que a issue será trabalhado por alunos da disciplina de Engenharia de Produto de Software (EPS)
- MDS (cor #0068b4): indica que a issue será trabalhado por alunos da disciplina de Métodos de Desenvolvimento de Software (MDS)

## Politica de branches

### Repositórios de desenvolvimento

Nos repositórios a **devel** é a branch padrão que está sempre atualizada. A branch **main** comporta as Releases lançadas do projeto, sendo a branch mais estável.

#### main

A branch **main** deve ser a branch mais estável do projeto, que estará em produção. Essa branch é protegida de commits e para o desenvolvimento de novas funcionalidades, deve receber Pull Requests (PRs).

#### development

A branch **devel** deve ser a branch de desenvolvomento do projeto, que estará em produção. Essa branch também é protegida de commits e para o desenvolvimento de novas funcionalidades, deve receber Pull Requests assim como a **main**(PRs). Uma vez que todas as funcionalidades da sprint são testadas e mescladas na branch de desenvolvimento podemos mesclar com a branch principal, a **main**.

#### Novas branches

As branches para o desenvolvimento de novas features devem ser criadas a partir da branch **devel** e devem seguir o padrão **x-nome-da-issue**, onde x é o número da issue que será resolvida na branch, acompanhado pelo nome da issue.

Os Pull Requests das novas branches devem ser feitos para a branch **devel**.

### Repositório de documentação

No repositório de documentação temos as branches **main** e **gh-pages**. Onde na **main** está o código da página de documentação do github pages e na branch **gh-pages** está o site compilado e em produção.

Assim como nos repositórios de desenvolvimento do projeto, no repositório de documentação a branch **main** está protegida e só deve aceitar modificações por Pull Requests..

As novas branches, assim como nos repositórios de desenvolvimento devem seguir a estrutura **x-nome-da-issue**.

## Politica de commits

Os commits durante o desenvolvimento do código devem frequentes, descritivos e concisos.

Os commits devem ser feitos em inglês utilizando os verbos no imperativo.

Os commits podem ser feitos utilizando o parametro **-s** para ter a assinatura do autor do commit. Caso o commit tenha sido feito em pareamento, deve constar no commit os co-autores.

O commit deve começar com `[y:x] -`, sendo x o número da issue que está sendo desenvolvida. e y a categoria do commit (feat, fix, hotfix, ...)

Exemplos de commit:

```
git commit -sm "[feat:7] - Add contributing guide

Co-authored-by: Nome da dupla <emaildadupla@email.com>"

git commit -sm "[fix:7] - Add contributing guide

Co-authored-by: Nome da dupla <emaildadupla@email.com>"

git commit -sm "[docs:7] - Add contributing guide
```

## Politica de pull requests

Os PRs devem ser feitos a branch **devel**.

Os Pull Requests devem ser feitos seguindo o template:

```
**Issue:** closes #X (sendo #x o link para a issue x)

## Descrição
Descrição completa do que foi feito

```

Onde só deve ser utilizado o _closes_ antes do link da issue, caso o PR resolva completamente a issue citada.

Caso o PR seja feito em um dos repositórios de desenvolvimento (backend de x, frontend,...), o link para a issue do repositório de documentação é feito da seguinte forma: `fga-eps-mds/2024.1-SENTINELA-DOC#x`, onde x é o número da issue. E no lugar de _closes_ deve ser utilizado **_resolves_**.

Em casos de PRs em que ainda estão sendo desenvolvidos, deve ser acrescentado a sigla **WIP** antes do título do PR.

Os PRs devem conter:

- Um título conciso e descritivo;
- Um _Assignee_ responsável pelo PR;
- Um _Reviewer_ responsável pela revisão do PR;
- _Labels_ significativas;
- Uma issue associada;
- Uma descrição, seguindo o template do repositório, que deve incluir uma descrição completa do que foi feito e a issue relacionada.

Os PRs só serão aceitos após passarem pelo CI estabelecido e por duas revisões.

## Histórico de versão

| Alteração                   | Data     | Autor        |
| --------------------------- | -------- | ------------ |
| Criação do documento        |          | Victor Yukio |
| Atualização                 |          | Ingrid       |
| Revisão e adição das labels | 03/08/24 | Sara Campos  |
