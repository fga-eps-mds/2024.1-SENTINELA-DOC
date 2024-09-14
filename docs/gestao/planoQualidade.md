# Plano de Qualidade

## Introdução

De acordo com a ISO 25010, a qualidade de um produto de software é definida pelo grau em que ele atende aos requisitos de seus usuários, agregando valor. Esses requisitos, que incluem funcionalidade, desempenho, segurança, manutenibilidade, entre outros, são representados no modelo de qualidade, que categoriza a qualidade do produto em características e subcaracterísticas. Para alcançar esses requisitos, é essencial desenvolver e monitorar métricas de forma contínua. O objetivo do planejamento de qualidade é descrever como esse monitoramento foi realizado durante o projeto.

## Processo de Qualidade

O processo de qualidade foi orientado pela validação das US com o cliente, utilizando protótipos e critérios de aceitação, seguido pela implementação contínua de melhorias. Após o desenvolvimento, as funcionalidades passam pelos testes de aceitação conduzidos pelo cliente, assegurando que ajustes e aperfeiçoamentos sejam aplicados. Caso novas melhorias sejam identificadas, elas são incorporadas ao processo de desenvolvimento, reforçando a qualidade do produto. Para garantir a qualidade do projeto, integramos cada serviço desenvolvido com a ferramenta SonarQube, utilizando a interface SonarCloud para uma melhor vizualização do monitoramento das métricas de qualidade ocorrido ao longo do projeto.

<p align="center">
  <img src="https://github.com/user-attachments/assets/bd21595f-81ea-46ab-ba02-123a3e4f390f" alt="eps qualidade">
</p>

## Métricas Monitoradas:

- Cobertura de Código
- Duplicação de Código
- Vulnerabilidades e Bugs
- Integração com CI/CD: Configuração do SonarCloud com pipelines de integração contínua.
- Alertas e Relatórios: Configuração de thresholds para alertas automáticos e geração de relatórios.

## Políticas de Código e Revisão

- Pull Requests e Code Review: Processo de revisão de código e melhores práticas para garantir qualidade.
- Padrões de Codificação: Ferramentas e regras aplicadas para padronização do código.
- Merge Guidelines: Critérios para fusão de branches e deploy.

## Ferramentas de Teste

**Jest**: Framework de testes completo para JavaScript, amplamente usado para testes de unidade, integração e ponta a ponta. Oferece suporte a mocks, snapshots, e uma interface fácil de usar.

**Vitest**: Framework de testes rápido e leve, projetado para o ecossistema JavaScript, com foco em integração com Vite. Suporta mocks, TypeScript e testes ESM, acelerando o desenvolvimento front-end.

**SonarCloud**: plataforma de análise de código que identifica bugs, vulnerabilidades e code smells. Oferece suporte a várias linguagens, integrando-se facilmente ao fluxo CI/CD para garantir a qualidade do código.

**ZenHub**: ferramenta de gerenciamento de projetos que se integra ao GitHub, oferecendo recursos como quadros kanban e relatórios de produtividade

# Modelo de Qualidade do Q-Rapids


De acordo com o site do projeto Q-Rapids (2024), o projeto possui três objetivos estratégicos gerais (GO1-GO3), focados no impacto, e quatro objetivos científicos (SO1-SO4), derivados dos objetivos estratégicos para garantir o sucesso do projeto.

Objetivos estratégicos gerais
- Melhorar os níveis de qualidade do software
- Aumentar a produtividade no ciclo de vida do software
- Reduzir o tempo de lançamento do software no mercado

Objetivos cientificos
- Coletar e analisar dados de tempo de execução e de tempo de design
- Definir o ciclo de vida do software integrando requisitos de qualidade e requisitos funcionais
- Elaborar indicadores-chave estratégicos para os tomadores de decisão gerirem o processo de desenvolvimento
- Fornecer suporte de ferramentas para um ciclo de vida do software voltado para a qualidade

 SonarCloud, plataforma de apoio para monitoramento de métricas de integração contínua, integra diferentes fontes de informação para gerar relatórios e dashboards que oferecem uma visão detalhada sobre a saúde do projeto. Contribuindo para a execução dos objetivos definidos no modelo Q-rapids.

Os fatores e métricas de qualidade são critérios usados para avaliar a eficiência, desempenho e confiabilidade de um produto de software, seu processo de desenvolvimento e a organização como um todo. Esses fatores, como manutenibilidade, confiabilidade, usabilidade e eficiência, ajudam a medir quão bem o software atende aos requisitos técnicos e às expectativas dos usuários. As métricas associadas fornecem dados quantitativos que permitem monitorar e melhorar a qualidade continuamente. Utilizá-las é essencial para identificar problemas precocemente, aumentar a satisfação do cliente, reduzir custos com retrabalho e garantir o alinhamento do produto com os objetivos estratégicos da organização.

### Métricas

As métricas definidas para o Sentinela foram:

| Métrica                  | Descrição                                           |
| ------------------------ | --------------------------------------------------- |
| Files                    | Quantidade de arquivos de código                    |
| Functions                | Quantidade de funções no código                     |
| Complexity               | Complexidade cognitiva                              |
| Comment Lines Density    | Densidade (%) de linhas comentadas                  |
| Duplicated Lines density | Densidade (%) de linhas duplicadas                  |
| Coverage                 | Cobertura de código pelos testes                    |
| Ncloc                    | Quantidade de linhas de código                      |
| Tests                    | Testes unitários e de integração                    |
| Test Errors              | Testes que possuem erros                            |
| Test Failures            | Testes que falharam                                 |
| Test Execution Time      | Tempo de execução dos testes                        |
| Security Rating          | Avaliação de segurança de falhas e vulnerabilidades |

### Métricas para o produto

O uso de métricas permite identificar subcaracterísticas associadas e avaliar a qualidade do produto. Essa análise também possibilita medir a produtividade do projeto, gerando resultados que influenciam as decisões de desenvolvimento. Com base nas métricas especificadas no SonarCloud e Q-Rapids, além dos dados coletados, foram definidos os valores mínimos aceitáveis para cada métrica no projeto Sentinela, conforme mostrado nas tabelas abaixo. Os dados referêntes a satisfação do usuário foram coletados a partir do [formulário](https://docs.google.com/forms/d/e/1FAIpQLSd1qZnT252QaJrbh8GwZZIOw2DFZUn0R2ZtrhHWqRdw0mqlhA/viewform) fornecido aos POs, que visa quantificar em escala de 1 a 5 qual o nível de satisfação do cliente quanto ao trabalho realizado e entregue pelo grupo Sentinela 2024/1, baseado nos modelos CSAT e NPS.

#### Repositório do Frontend

| Métrica                      | Valor referência | Valor alcançado ao final do projeto |
| ---------------------------- | ---------------- | --------------- |
| Complexity                   | até 10           | 9               |
| Comment Lines Density (%)    | até 30%          | 1,9%            |
| Duplicated Lines Density (%) | até 5%           | 7%              |
| Coverage                     | acima de 80%     | 78,1%           |
| Test Failures                | 0                | 0               |
| Test Errors                  | 0                | 0               |
| Security Rating              | 0 (A)            | 0 (A)           |
| Satisfação do usuário        | acima de 3       | 5               |

#### Repositório do Backend - Usuários

| Métrica                      | Valor referência | Valor alcançado ao final do projeto  |
| ---------------------------- | ---------------- | --------------- |
| Complexity                   | até 10           | 3               |
| Comment Lines Density (%)    | até 30%          | 4,7%            |
| Duplicated Lines Density (%) | até 5%           | 0,0%            |
| Coverage                     | acima de 80%     | 78,2            |
| Test Failures                | 0                | 0               |
| Test Errors                  | 0                | 0               |
| Security Rating              | 0 (A)            | 0 (A)           |
| Satisfação do usuário        | acima de 3       | 5               |

#### Repositório do Backend - Financeiro

| Métrica                      | Valor referência | Valor alcançado ao final do projeto  |
| ---------------------------- | ---------------- | --------------- |
| Complexity                   | até 10           | 1               |
| Comment Lines Density (%)    | até 30%          | 5,5%            |
| Duplicated Lines Density (%) | até 5%           | 0,0%            |
| Coverage                     | acima de 80%     | 86,5%           |
| Test Failures                | 0                | 0               |
| Test Errors                  | 0                | 0               |
| Security Rating              | 0 (A)            | 0 (A)           |
| Satisfação do usuário        | acima de 3       | 5               |

#### Repositório do Backend - Benefícios

| Métrica                      | Valor referência | Valor alcançado ao final do projeto  |
| ---------------------------- | ---------------- | --------------- |
| Complexity                   | até 10           | 2               |
| Comment Lines Density (%)    | até 30%          | 4,7%            |
| Duplicated Lines Density (%) | até 5%           | 0,0%            |
| Coverage                     | acima de 80%     | 78%             |
| Test Failures                | 0                | 0               |
| Test Errors                  | 0                | 0               |
| Security Rating              | 0 (A)            | 1 (E)           |
| Satisfação do usuário        | acima de 3       | 5               |

## Histórico de Versões

| Alteração                    | Data       | Autor           |
| ---------------------------- | ---------- | --------------- |
| Criação do documento         | 28/07/24   | Ingrid Carvalho |
| Atualizações sobre o sonar   | 31/08/2024 | Ingrid Carvalho |
| Atualizações com as métricas | 08/09/2024 | Ingrid Carvalho |
| Revisão                      | 08/09/2024 | Sara Campos     |

## Referências

[ISO/IEC 25010](https://iso25000.com/index.php/en/iso-25000-standards/iso-25010)

[Q-rapids](https://www.q-rapids.eu/about)
