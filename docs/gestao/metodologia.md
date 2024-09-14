# Metodologia de Trabalho da Equipe

## Introdução

Para as fases inicias do projeto, foi adotada a metodologia de Lean Inception, que foi abordada em mais detalhes na aba homônima, iniciada no [Dia 1](../lean/dia1.md).

Nossa equipe adotou uma metodologia de desevolvimento híbrida baseada em Scrum e práticas do Extreme Programming (XP), Kanban e PMBOK para garantir um desenvolvimento ágil e eficiente. Este documento detalha os processos e ferramentas que utilizamos para organizar e comunicar nosso trabalho.

## Framework Scrum

### 1. Sprints

- O Scrum traz uma abordagem que ocorre ao longo sprints, que são esses períodos de tempo (geralmente uma semana), dentro dos quais são planejadas metas de trabalho a serem realizados.

### 2. Planning

- **Objetivo:** Definir as metas e tarefas para o próximo ciclo de desenvolvimento.
- **Frequência:** Toda segunda 21h após reunião com cliente
- **Participantes:** Toda a equipe
- **Atividades:**
  - Revisar o backlog de produto
  - Estimar as tarefas utilizando métodos como Planning Poker
  - Definir as prioridades e selecionar as tarefas para o sprint

### 3. Standup meeting

- **Objetivo:** Alinhar o progresso e identificar impedimentos.
- **Frequência:** Terças e quintas entre aulas
- **Participantes:** Toda a equipe
- **Atividades:**
  - Novas atividades podem ser repassadas
  - Cada membro responde às perguntas:
    - O que estou fazendo?
    - Há algum impedimento no meu caminho?

### 4. Review

- **Objetivo:** Apresentar o trabalho realizado durante a sprint e validar com o PO.
- **Frequência:** Toda segunda 20h em reunião com cliente
- **Participantes:** Toda a equipe, incluindo stakeholders
- **Atividades:**
  - Demonstração das funcionalidades desenvolvidas
  - Feedback dos stakeholders
  - Atualização do backlog com base no feedback recebido

### 5. Retrospectiva

- **Objetivo:** Refletir sobre o sprint passado e identificar melhorias para os próximos sprints.
- **Frequência:** Toda sexta-feira às 16h
- **Participantes:** Toda a equipe
- **Atividades:**
  - Discussão sobre o que funcionou bem e o que pode ser melhorado
  - Definição de ações para melhorias contínuas

### 6. Papéis

- O Scrum sugere os papéis de **Product Owner** e **Scrum Master**. Neste trabalho, os representantes do SINDPOL-DF (Matheus Amaral e Davi Mendonça) tiveram uma atuação semelhante a proposta de um Product Owner, representando as necessidades do cliente. Enquanto isso, os estudantes de EPS puderam assumir o papel de Scrum Master, gerenciando, treinando e orientando a **Equipe de Desenvolvimento** (estudantes de MDS e, em dados momentos, EPS) para cumprir as regras de Scrum e entregar os resultados.

## Práticas do Extreme Programming (XP)

### 1. Programação em Pares

- **Objetivo:** Melhorar a qualidade do código e promover o compartilhamento de conhecimento.
- **Como funciona:** Dois desenvolvedores trabalham juntos no mesmo código, alternando entre os papéis de “Driver” e “Observer”. Neste trabalho, houveram momentos em que a programação envolvia inclusive mais de duas pessoas, em momentos críticos e quando códigos eram debugados. Além disso, o time realizou duas reuniões extraordinárias com a presença de todos integrantes para codar num ambiente em que o grupo como um todo poderia se apoiar e parear conforme necessidade.

### 2. Integração Contínua (CI/CD)

- **Objetivo:** Assegurar que o código está sempre em um estado funcional.
- **Como funciona:** O código é integrado e testado automaticamente no SonarQube, permitindo coletar métricas do código rapidamente.

### 3. Proximidade com o Usuário

- **Objetivo:** Garantir que o desenvolvimento está alinhado com as necessidades e expectativas do usuário.
- **Como funciona:** Envolvimento constante do usuário final durante o processo de desenvolvimento, com feedback frequente e ajustes conforme necessário.

### 4. Cadência Rápida de Entregas

- **Objetivo:** Entregar incrementos de valor ao cliente de forma contínua e rápida.
- **Como funciona:** Entregas frequentes e menores, focando na entrega contínua de valor ao cliente por meio de releases (versões do produto). Com a definição de três releases major no período da disciplina, foram planejadas as entregas de cada uma, de forma que, o trabalho dentro das sprints do Scrum era executado a fim de atingir essas metas.

### 5. Testes

- **Objetivo:** Essa prática viabiliza a integração contínua e busca monitorar a qualidade do produto, garantindo que seu comportamento seja condizente com o esperado.
- **Como funciona:** No código fonte são realizados testes unitáios desenvolvidos pela Equipe de Desenvolvimento, enquanto no ambiente de produção são feitos testes de aceitação/testes manuais realizados pelos P.Os e pela Equipe de Desenvolvimento.

## Kanban

### Uso do Quadro Kanban

- **Objetivo:** Visualizar o fluxo de trabalho e limitar o trabalho em progresso.
- **Como funciona:** As tarefas são movidas através de colunas no quadro, representando diferentes estágios do fluxo de trabalho (Ex.: Backlog, Em Progresso, Em Revisão, Concluído). Foi usado o Zenhub criar essa visualização de progresso das atividades e, ao passo que foi notado gargalo de trabalho em andamento, os Scrum Masters tomaram decisão de não iniciar novas histórias e focar em finalizar entregas de qualidade do que estava _In Progress_.

## PMBOK

### Gestão de Projetos

- **Objetivo:** Integrar práticas de gerenciamento de projetos para melhor organização e controle.
- **Como funciona:** Utiliza-se as áreas de conhecimento do PMBOK, como gerenciamento de escopo, tempo, custo e qualidade, adaptando-as ao contexto ágil da equipe. O escopo foi gerenciado pelos Srum Masters com acompanhamento dos P.Os ao longo do semestre, considerando o que havia sido planejado inicialmente e a viabilidade conforme o andamento do trabalho. O custo também foi monitorado por meio de documentos como [Custo](./custo.md), com acompanhamento semanal/total do custo, e [EVM](./evm.md), com os resultados de Valor Agregado e Valor Planejado. O documento de [Riscos](./riscos.md) demonstra o relato semanal/por sprint dos riscos identificados e seus respectivos graus de probabilidade e impacto, bem como os planejamentos de respostas a cada um deles.

### Grupos de processos

- **Objetivo:** Definir o ciclo de vida do projeto.
- **Como funciona:** Apesar de discordar um pouco da visão ágil nesse sentido, o PMBOK traz um conjunto de fases pelas quais o projeto passa dentro do seu cronograma de execução. Essa visão foi trazida na [EAP](./eap.md), onde tem-se os grupos de processos Iniciação, Planejamento, Execução e Encerramento. Essa visão é uma abstração do método, visto que, as atividades nem sempre são resumidas apenas a um grupo de processos, como é a proposta do ágil.

## Conclusão

Adotando essa combinação de Scrum, XP, Kanban e PMBOK, visamos a maximização da produtividade e a qualidade do nosso produto final. As ferramentas escolhidas suportam nossas necessidades de comunicação e organização, facilitando a colaboração e a transparência em todas as fases do desenvolvimento.

## Histórico de versão

| Alteração                                      | Data     | Autor        |
| ---------------------------------------------- | -------- | ------------ |
| Criação do documento                           |          | Victor Yukio |
| Revisão                                        | 18/07/24 | Sara Campos  |
| Revisão                                        | 03/08/24 | Sara Campos  |
| Revisão conforme apontamentos da Release Final | 14/09/24 | Sara Campos  |

## Referências

[Scrum: Como fazer mais em menos tempo](https://orcestra.com.br/2020/06/06/scrum-como-fazer-mais-em-menos-tempo/?gad_source=1&gclid=CjwKCAjw6JS3BhBAEiwAO9waF1QmvKD0d5RGdt0TxxIxM8wP_k4xo6Wtz4Mpx77qtBOFNqZfArqxvhoC1ycQAvD_BwE). Acessado em 14/09/2024.
[Práticas em XP: Extreme Programming](https://www.devmedia.com.br/praticas-em-xp-extreme-programming/29330). Acessado em 14/09/2024.
